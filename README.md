# My Web Security Learning process on PortSwigger and my solution of their labs.

## SQL Injection
| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | SQL injection vulnerability in WHERE clause allowing retrieval of hidden data                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-vulnerability-in-where-clause-allowing-retrieval-of-hidden-data)       |
| Apprentice       | SQL injection vulnerability allowing login bypass                                             | [Solved](SQL_injection/README.md#lab-sql-injection-vulnerability-allowing-login-bypass)       |
| Practitioner     | SQL injection attack, querying the database type and version on Oracle                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-attack-querying-the-database-type-and-version-on-oracle) |
| Practitioner     | SQL injection attack, querying the database type and version on MySQL and Microsoft           | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-attack-querying-the-database-type-and-version-on-mysql-and-microsoft)       |
| Practitioner     | SQL injection attack, listing the database contents on non-Oracle databases                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-attack-listing-the-database-contents-on-non-oracle-databases)      |
| Practitioner     | SQL injection attack, listing the database contents on Oracle                                 | Not Solved   |
| Practitioner     | SQL injection UNION attack, determining the number of columns returned by the query           | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-union-attack-determining-the-number-of-columns-returned-by-the-query)      |
| Practitioner     | SQL injection UNION attack, finding a column containing text                                  | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-union-attack-finding-a-column-containing-text)   |
| Practitioner     | SQL injection UNION attack, retrieving data from other tables                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-union-attack-retrieving-data-from-other-tables)    |
| Practitioner     | SQL injection UNION attack, retrieving multiple values in a single column                     | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-union-attack-retrieving-multiple-values-in-a-single-column)       |
| Practitioner     | Blind SQL injection with conditional responses                                                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-lab-blind-sql-injection-with-conditional-responses)     |
| Practitioner     | Blind SQL injection with conditional errors                                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-blind-sql-injection-with-conditional-errors)     |
| Practitioner     | Visible error-based SQL injection                                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-visible-error-based-sql-injection)   |
| Practitioner     | Blind SQL injection with time delays                                                          | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-blind-sql-injection-with-time-delays)   |
| Practitioner     | Blind SQL injection with time delays and information retrieval                                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-blind-sql-injection-with-time-delays-and-information-retrieval)   |
| Practitioner     | Blind SQL injection with out-of-band interaction                                              | Not Solved   |
| Practitioner     | Blind SQL injection with out-of-band data exfiltration                                        | Not Solved   |
| Practitioner     | SQL injection with filter bypass via XML encoding                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SQL_injection#lab-sql-injection-with-filter-bypass-via-xml-encoding)   |




## Access Control Vulnerabilities

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Unprotected admin functionality                                                              | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-unprotected-admin-functionality)       |
| Apprentice       | Unprotected admin functionality with unpredictable URL                                       | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-unprotected-admin-functionality-with-unpredictable-url)       |
| Apprentice       | User role controlled by request parameter                                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-role-controlled-by-request-parameter)       |
| Apprentice       | User role can be modified in user profile                                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-lab-user-role-can-be-modified-in-user-profile)       |
| Apprentice       | User ID controlled by request parameter                                                      | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter)       |
| Apprentice       | User ID controlled by request parameter, with unpredictable user IDs                         | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter-with-unpredictable-user-ids)       |
| Apprentice       | User ID controlled by request parameter with data leakage in redirect                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter-with-data-leakage-in-redirect)       |
| Apprentice       | User ID controlled by request parameter with password disclosure                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter-with-password-disclosure)       |
| Apprentice       | Insecure direct object references                                                            | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-insecure-direct-object-references-idor)       |
| Practitioner     | URL-based access control can be circumvented                                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-lab-url-based-access-control-can-be-circumvented)       |
| Practitioner     | Method-based access control can be circumvented                                              | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-lab-method-based-access-control-can-be-circumvented)       |
| Practitioner     | Multi-step process with no access control on one step                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-multi-step-process-with-no-access-control-on-one-step)       |
| Practitioner     | Referer-based access control                                                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-referer-based-access-control)   |



## Path Traversal

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | File path traversal, simple case                                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Path_Traversal#lab-file-path-traversal-simple-case)       |
| Practitioner     | File path traversal, traversal sequences blocked with absolute path bypass                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Path_Traversal#lab-file-path-traversal-traversal-sequences-blocked-with-absolute-path-bypass)       |
| Practitioner     | File path traversal, traversal sequences stripped non-recursively                            | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Path_Traversal#lab-file-path-traversal-traversal-sequences-stripped-non-recursively)       |
| Practitioner     | File path traversal, traversal sequences stripped with superfluous URL-decode                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Path_Traversal#lab-file-path-traversal-traversal-sequences-stripped-with-superfluous-url-decode)       |
| Practitioner     | File path traversal, validation of start of path                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Path_Traversal#lab-file-path-traversal-validation-of-start-of-path)       |
| Practitioner     | File path traversal, validation of file extension with null byte bypass                      | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Path_Traversal#lab-file-path-traversal-validation-of-file-extension-with-null-byte-bypass)       |



## Access Control Vulnerabilities

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Unprotected admin functionality                                                              | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-unprotected-admin-functionality)       |
| Apprentice       | Unprotected admin functionality with unpredictable URL                                       | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-unprotected-admin-functionality-with-unpredictable-url)       |
| Apprentice       | User role controlled by request parameter                                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-role-controlled-by-request-parameter)       |
| Apprentice       | User role can be modified in user profile                                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-lab-user-role-can-be-modified-in-user-profile)       |
| Apprentice       | User ID controlled by request parameter                                                      | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter)       |
| Apprentice       | User ID controlled by request parameter, with unpredictable user IDs                         | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter-with-unpredictable-user-ids)       |
| Apprentice       | User ID controlled by request parameter with data leakage in redirect                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter-with-data-leakage-in-redirect)       |
| Apprentice       | User ID controlled by request parameter with password disclosure                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-user-id-controlled-by-request-parameter-with-password-disclosure)       |
| Apprentice       | Insecure direct object references                                                            | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-insecure-direct-object-references-idor)       |
| Practitioner     | URL-based access control can be circumvented                                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-lab-url-based-access-control-can-be-circumvented)       |
| Practitioner     | Method-based access control can be circumvented                                              | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-lab-method-based-access-control-can-be-circumvented)       |
| Practitioner     | Multi-step process with no access control on one step                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-multi-step-process-with-no-access-control-on-one-step)       |
| Practitioner     | Referer-based access control                                                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Access_control#lab-referer-based-access-control)   |



## Information Disclosure

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Information disclosure in error messages                                                     | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Information_Disclosure#lab-information-disclosure-in-error-messages)       |
| Apprentice       | Information disclosure on debug page                                                         | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Information_Disclosure#lab-information-disclosure-on-debug-page)       |
| Apprentice       | Source code disclosure via backup files                                                      | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Information_Disclosure#lab-source-code-disclosure-via-backup-files)       |
| Apprentice       | Authentication bypass via information disclosure                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Information_Disclosure#lab-authentication-bypass-via-information-disclosure)       |
| Practitioner     | Information disclosure in version control history                                            | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Information_Disclosure#lab-information-disclosure-in-version-control-history)       |



## OS Command Injection

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | OS command injection, simple case                                                            | [Solved](https://github.com/proochicken/PortSwigger/tree/main/OS_Command_Injection#lab-os-command-injection-simple-case)       |
| Practitioner     | Blind OS command injection with time delays                                                  | [Solved](https://github.com/proochicken/PortSwigger/tree/main/OS_Command_Injection#lab-blind-os-command-injection-with-time-delays)       |
| Practitioner     | Blind OS command injection with output redirection                                           | [Solved](https://github.com/proochicken/PortSwigger/tree/main/OS_Command_Injection#lab-blind-os-command-injection-with-output-redirection)       |
| Practitioner     | Blind OS command injection with out-of-band interaction                                      | [Solved](https://github.com/proochicken/PortSwigger/tree/main/OS_Command_Injection#lab-blind-os-command-injection-with-out-of-band-interaction)       |
| Practitioner     | Blind OS command injection with out-of-band data exfiltration                                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/OS_Command_Injection#lab-blind-os-command-injection-with-out-of-band-data-exfiltration)       |


## File Upload Vulnerabilities

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Remote code execution via web shell upload                                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/File_Upload#lab-remote-code-execution-via-web-shell-upload)       |
| Apprentice       | Web shell upload via Content-Type restriction bypass                                         | [Solved](https://github.com/proochicken/PortSwigger/tree/main/File_Upload#lab-web-shell-upload-via-content-type-restriction-bypass)       |
| Practitioner     | Web shell upload via path traversal                                                          | [Solved](https://github.com/proochicken/PortSwigger/tree/main/File_Upload#lab-web-shell-upload-via-path-traversal)       |
| Practitioner     | Web shell upload via extension blacklist bypass                                              | [Solved](https://github.com/proochicken/PortSwigger/tree/main/File_Upload#lab-web-shell-upload-via-extension-blacklist-bypass)       |
| Practitioner     | Web shell upload via obfuscated file extension                                               | [Solved](https://github.com/proochicken/PortSwigger/tree/main/File_Upload#lab-web-shell-upload-via-obfuscated-file-extension)       |
| Practitioner     | Remote code execution via polyglot web shell upload                                          | [Solved](https://github.com/proochicken/PortSwigger/tree/main/File_Upload#lab-remote-code-execution-via-polyglot-web-shell-upload)       |
| Expert           | Web shell upload via race condition                                                          | Not Solved       |


## NoSQL Injection

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Detecting NoSQL injection                                                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/NoSQL_Injection#lab-detecting-nosql-injection)       |
| Apprentice       | Exploiting NoSQL operator injection to bypass authentication                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/NoSQL_Injection#lab-exploiting-nosql-operator-injection-to-bypass-authentication)       |
| Practitioner     | Exploiting NoSQL injection to extract data                                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/NoSQL_Injection#lab-exploiting-nosql-injection-to-extract-data)       |
| Practitioner     | Exploiting NoSQL operator injection to extract unknown fields                                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/NoSQL_Injection#lab-exploiting-nosql-operator-injection-to-extract-unknown-fields)       |



## Authentication

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Username enumeration via different responses                                                  | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-username-enumeration-via-different-responses)       |
| Apprentice       | 2FA simple bypass                                                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-2fa-simple-bypass)       |
| Apprentice       | Password reset broken logic                                                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-password-reset-broken-logic)       |
| Practitioner     | Username enumeration via subtly different responses                                          | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-username-enumeration-via-subtly-different-responses)       |
| Practitioner     | Username enumeration via response timing                                                     | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-username-enumeration-via-response-timing)       |
| Practitioner     | Broken brute-force protection, IP block                                                      | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-broken-brute-force-protection-ip-block)       |
| Practitioner     | Username enumeration via account lock                                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-username-enumeration-via-account-lock)       |
| Practitioner     | 2FA broken logic                                                                             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-2fa-broken-logic)       |
| Practitioner     | Brute-forcing a stay-logged-in cookie                                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-brute-forcing-a-stay-logged-in-cookie)       |
| Practitioner     | Offline password cracking                                                                    | [Solved]()       |
| Practitioner     | Password reset poisoning via middleware                                                      | Not solved       |
| Practitioner     | Password brute-force via password change                                                     | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-password-brute-force-via-password-change)       |
| Expert           | Broken brute-force protection, multiple credentials per request                              | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-broken-brute-force-protection-multiple-credentials-per-request)       |
| Expert           | 2FA bypass using a brute-force attack                                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Authentication_vul#lab-2fa-bypass-using-a-brute-force-attack)       |



## Race Conditions

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Limit overrun race conditions                                                                 | [Solved](https://github.com/nglong05/PortSwigger/blob/main/Race%20Conditions.md#lab-limit-overrun-race-conditions) |
| Practitioner     | Bypassing rate limits via race conditions                                                     | [Solved](https://github.com/nglong05/PortSwigger/blob/main/Race%20Conditions.md#lab-bypassing-rate-limits-via-race-conditions) |
| Practitioner     | Multi-endpoint race conditions                                                                | [Solved](https://github.com/nglong05/PortSwigger/blob/main/Race%20Conditions.md#lab-multi-endpoint-race-conditions) |
| Practitioner     | Single-endpoint race conditions                                                               | [Solved](https://github.com/nglong05/PortSwigger/blob/main/Race%20Conditions.md#lab-single-endpoint-race-conditions) |
| Practitioner     | Exploiting time-sensitive vulnerabilities                                                     | [Solved](https://github.com/nglong05/PortSwigger/blob/main/Race%20Conditions.md#lab-exploiting-time-sensitive-vulnerabilities) |
| Expert           | Partial construction race conditions                                                          | Not solved |


## Race Conditions

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Limit overrun race conditions                                                                 | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Race_Condition#lab-limit-overrun-race-conditions) |
| Practitioner     | Bypassing rate limits via race conditions                                                     | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Race_Condition#lab-bypassing-rate-limits-via-race-conditions) |
| Practitioner     | Multi-endpoint race conditions                                                                | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Race_Condition#lab-multi-endpoint-race-conditions) |
| Practitioner     | Single-endpoint race conditions                                                               | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Race_Condition#lab-single-endpoint-race-conditions) |
| Practitioner     | Exploiting time-sensitive vulnerabilities                                                     | [Solved](https://github.com/proochicken/PortSwigger/tree/main/Race_Condition#lab-exploiting-time-sensitive-vulnerabilities) |
| Expert           | Partial construction race conditions                                                          | Not solved |



## Server-side request forgery (SSRF)

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Basic SSRF against the local server                                                           | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-basic-ssrf-against-the-local-server) |
| Apprentice       | Basic SSRF against another back-end system                                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-basic-ssrf-against-another-back-end-system) |
| Practitioner     | Blind SSRF with out-of-band detection                                                         | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-blind-ssrf-with-out-of-band-detection) |
| Practitioner     | SSRF with blacklist-based input filter                                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-ssrf-with-blacklist-based-input-filter) |
| Practitioner     | SSRF with filter bypass via open redirection vulnerability                                    | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-ssrf-with-filter-bypass-via-open-redirection-vulnerability) |
| Expert           | Blind SSRF with Shellshock exploitation                                                       | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-blind-ssrf-with-shellshock-exploitation) |
| Expert           | SSRF with whitelist-based input filter                                                        | [Solved](https://github.com/proochicken/PortSwigger/tree/main/SSRF#lab-ssrf-with-whitelist-based-input-filter) |


## API Testing

| **Difficulty**   | **Title**                                                                                     | **Status**   |
|------------------|-----------------------------------------------------------------------------------------------|--------------|
| Apprentice       | Exploiting an API endpoint using documentation | [Solved](https://github.com/proochicken/PortSwigger/tree/main/API_testing#lab-exploiting-an-api-endpoint-using-documentation) |
| Practitioner     | Exploiting server-side parameter pollution in a query string | [Solved](https://github.com/proochicken/PortSwigger/tree/main/API_testing#lab-exploiting-server-side-parameter-pollution-in-a-query-string) |
| Practitioner     | Finding and exploiting an unused API endpoint | [Solved](https://github.com/proochicken/PortSwigger/tree/main/API_testing#lab-finding-and-exploiting-an-unused-api-endpoint) |
| Practitioner     | Exploiting a mass assignment vulnerability | [Solved](https://github.com/proochicken/PortSwigger/tree/main/API_testing#lab-exploiting-a-mass-assignment-vulnerability) |
| Expert          | Exploiting server-side parameter pollution in a REST URL | [Solved](https://github.com/proochicken/PortSwigger/tree/main/API_testing#lab-exploiting-server-side-parameter-pollution-in-a-rest-url) |


## XML External Entity (XXE) Injection

| **Difficulty**   | **Title**                                                                 | **Status**   |
|------------------|---------------------------------------------------------------------------|--------------|
| Apprentice       | Exploiting XXE using external entities to retrieve files                  | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-xxe-using-external-entities-to-retrieve-files) |
| Apprentice       | Exploiting XXE to perform SSRF attacks                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-xxe-to-perform-ssrf-attacks) |
| Practitioner     | Blind XXE with out-of-band interaction                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-blind-xxe-with-out-of-band-interaction) |
| Practitioner     | Blind XXE with out-of-band interaction via XML parameter entities       | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-blind-xxe-with-out-of-band-interaction-via-xml-parameter-entities) |
| Practitioner     | Exploiting blind XXE to exfiltrate data using a malicious external DTD  | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-blind-xxe-to-exfiltrate-data-using-a-malicious-external-dtd) |
| Practitioner     | Exploiting blind XXE to retrieve data via error messages               | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-blind-xxe-to-retrieve-data-via-error-messages) |
| Practitioner     | Exploiting XInclude to retrieve files                                  | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-xinclude-to-retrieve-files) |
| Practitioner     | Exploiting XXE via image file upload                                   | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-xxe-via-image-file-upload) |
| Expert          | Exploiting XXE to retrieve data by repurposing a local DTD             | [Solved](https://github.com/proochicken/PortSwigger/tree/main/XXE#lab-exploiting-xxe-to-retrieve-data-by-repurposing-a-local-dtd) |

