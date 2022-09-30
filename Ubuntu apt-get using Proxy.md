# How to Install Application (apt-get install) using Corporate Proxy
1. Create configuration on APT
``` bash
$ sudo nano /etc/apt/apt.conf.d/proxy.conf
```
2. Add/Replace this configuration
```
Acquire::http::Proxy "http://<user.name>:<password>@proxy.corp.yourcompany.co.id:8080";
Acquire::https::Proxy "https://<user.name>:<password>@proxy.corp.yourcompany.co.id:8080";
Acquire::ftp::Proxy "ftp://<user.name>:<password>@proxy.corp.yourcompany.co.id:8080";
```
3. Save the file! `CTRL + X` >> `Y` >> `ENTER`!
