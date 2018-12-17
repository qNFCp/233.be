## 功能  
本服务可生成http(s)网址的短链接

## API

API地址
```
https://233.be/api/set.php
```

API方式：POST

### 例子
其中 
{"url": "https://www.google.com/"}
{"url": "www.google.com/"}'
{"url": "https://233.be/537b"}'
为POST参数

例1：

```
curl -X POST \
    -d '{"url": "https://www.google.com/"}' \
    https://233.be/api/set.php
```
 返回值
 ```
{"success":"true","content":{"url":"https:\/\/233.be\/f476"}}
```
例2：

```
curl -X POST \
    -d '{"url": "google.com"}' \
    https://233.be/api/set.php
```
返回值
```
{"success":"true","content":{"url":"https:\/\/233.be\/537b"}}
```
例3：

```
curl -X POST \
    -d '{"url": "https://233.be/537b"}' \
    https://233.be/api/set.php
```
返回值

```
{"success":"false","content":"\u94fe\u63a5\u5df2\u7ecf\u662f\u77ed\u5730\u5740\u4e86\u3002"}
```
返回值译文：
```
{"success":"false","content":"链接已经是短地址了"}
```