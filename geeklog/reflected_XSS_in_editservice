# Reflected XSS in Geeklog v2.2.2
Geeklog v2.2.2 is vulnerable to Reflected Cross-Site Scripting (XSS) in public_html/admin/trackback.php

Vendor:https://github.com/Geeklog-Core/geeklog

## PoC
1. Log in to the Geeklog's admin account and Navigate to Trackback and click an Create New.

![traceback](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/geeklog_traceback.png)

2. Enter the payloads to the input areas of Service, Website and URL to ping. Then click on SAVE. The payloads are
~~~
" onmouseover=alert('xss1')//
" onmouseover=alert('xss2')//
" onmouseover=alert('xss3')//
~~~

![editservice_inject](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/geeklog_editservice_inject.png)
3. Move our mouse to the three input areas. We can observe the payloads getting triggered.

![eeklog_es_rf1](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/geeklog_es_rf1.png)

![eeklog_es_rf2](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/geeklog_es_rf2.png)

![eeklog_es_rf3](https://github.com/CrownZTX/vulnerabilities/blob/main/geeklog/images/geeklog_es_rf3.png)
