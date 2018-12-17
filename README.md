# 233.be
---
> 一个用于域名缩短网站的源代码

## 概述
[233.be](https://233.be/) 是一个网址缩短服务的网站，这是它的源代码。
基于[CRZ.im](https://github.com/Caringor/CRZ.im/)

## API
[API文档](https://github.com/qNFCp/233.be/blob/master/API.md)

## 安装
233.be 基于 PHP、SQLite 进行开发，您只需要修改 `config.php` 的相关配置并将 inc 目录设置为公共读写权限即可。
对于 `Nginx` 用户，则还需把 `nginx.txt` 里面的内容添加到 Nginx 的配置文件里。

## 对于宝塔面板
Nginx：在站点修改→配置文件 内加入 `Nginx.txt` 中的内容到底部 `access_log /www/wwwlogs/***` 行之前即可
