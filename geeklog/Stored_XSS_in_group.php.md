# Stored XSS in Geeklog v2.2.2
Geeklog v2.2.2 is vulnerable to Stored Cross-Site Scripting (XSS) in public_html/admin/group.php

Vendor:https://github.com/Geeklog-Core/geeklog

## PoC
1. Log in to the Geeklog's admin account and Navigate to Groups and click an Edit button.

![Geeklog_groups](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/groups.png)

2. Enter the payloads to the input areas of Description. Then click on SAVE. The payloads are
~~~
<script>alert('xss')</script>
~~~

![groups_inject](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/groups_inject.png)
3. We can observe the payloads getting triggered. Multiple visits to the page of Groups will still trigger payloads.

![groups_reflect](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/groups_reflect.png)

![groups_reflect1](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/groups_reflect1.png)
