
# 本地环境配置：

## Nginx + PHP 配置：
```perl
		location / {
            root   D:/workspace/m-html/v1.1;
            index  index.html index.htm index.php;
        }

		location /client {
			proxy_pass http://xxxx.xxx.com/client;
		}

		location ~ \.php$ {
			root			D:/workspace/m-html/v1.1;
			fastcgi_pass 	127.0.0.1:90;
			fastcgi_index	index.php;
			fastcgi_param	SCRIPT_FILENAME $document_root$fastcgi_script_name;
			include			fastcgi_params;
		}
```
## 服务器启动：
```bash
start_nginx.bat:
@echo off
echo Starting PHP FastCGI...
D:\server\nginx\RunHiddenConsole.exe D:/server/php5/php-cgi.exe -b 127.0.0.1:90 -c D:/server/php5/php.ini
echo Starting nginx...
D:\server\nginx\RunHiddenConsole.exe D:/server/nginx/nginx.exe -p D:/server/nginx/
```
## 项目启动：
url:http://localhost/html/new/index.php <br>
在本地登录时 先刷一下这个链接：localhost/client?functionId=login/testLogin&body={"pin":"xxxxxxxx"}
