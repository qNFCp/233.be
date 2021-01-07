## 功能  function
本服务可生成http(s)网址的短链接
This service generates short links to http(s) URLs.

## API

API地址
API's URL
```
https://***/api/set.php
```

API方式：POST

### 例子 e.g.
其中 
{"url": "https://www.google.com/"}

{"url": "www.google.com/"}

{"url": "https://233.be/537b"}

为POST参数
is a parameter for the POST

#### 例1 e.g.1：

```
curl -X POST \
    -d '{"url": "https://www.google.com/"}' \
    https://233.be/api/set.php
```
 返回值 Returned value:
 ```
{"success":"true","content":{"url":"https:\/\/233.be\/f476"}}
```
#### 例2 e.g.2：

```
curl -X POST \
    -d '{"url": "google.com"}' \
    https://233.be/api/set.php
```
返回值 Returned value:
```
{"success":"true","content":{"url":"https:\/\/233.be\/537b"}}
```
#### 例3 e.g.3：

```
curl -X POST \
    -d '{"url": "https://233.be/537b"}' \
    https://233.be/api/set.php
```
返回值 Returned value:

```
{"success":"false","content":"\u94fe\u63a5\u5df2\u7ecf\u662f\u77ed\u5730\u5740\u4e86\u3002"}
```
返回值译文 Really returned value：
```
{"success":"false","content":"链接已经是短地址了"}
{"success":"false","content":"This link is already a short URL"}
```
