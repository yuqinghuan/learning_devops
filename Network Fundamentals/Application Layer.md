# 应用层

## 职责（将消息运送到传输层）

1. 以符合所使用协议的格式将数据写入网络。
2. 从最终用户读取数据。
3. 为最终用户提供有用的应用程序。
4. 一些应用程序还确保来自最终用户的数据采用正确的格式。
5. 错误处理和恢复也由一些应用程序完成。

## 应用层协议

### HTTP(HyperText Transfer Protocol)

* HTML(HyperText Markup Language)
* URL(Universal Resource Locator): 用于定位服务器上存在的文件
![url剖析](../img/url剖析.jpg)

* Uniform Resource Identifiers (URIs)

`http://host:port/path?request-parameters#nameAnchor`

#### Non-persistent HTTP

#### Persistent HTTP

#### HTTP 请求头和响应头

```
GET /path/to/file/index.html HTTP/1.1
Host: www.educative.io
Connection: close
User-agent: Mozilla/5.0
Accept-language: fr
Accept: text/html
```
##### HTTP Methods
* GET
* POST
* HEAD
* PUT
* DELETE

```
HTTP/1.1 200 OK
Connection: close
Date: Tue, 18 Aug 2015 15: 44 : 04 GMT
Server: Apache/2.2.3 (CentOS)
Last-Modified: Tue, 18 Aug 2015 15:11:03 GMT 
Content-Length: 6821
Content-Type: text/html

[The object that was requested]
```
##### Status Code
* 1xx codes fall in the informational category
* 2xx codes fall in the success category
* 3xx codes are for redirection
* 4xx is client error
* 5xx is server error


扩展: curl(Client URL)





