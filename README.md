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




