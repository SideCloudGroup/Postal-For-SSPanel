# Postal-For-SSPanel
## 介绍
为SSPanel提供通过Postal API发送邮件的功能 \
与SMTP协议相比，Postal API提供了更高的发送速度和更低的延迟 \
此插件仅在较低版本SSPanel上测试，未在新版本测试

## 安装
从Release页面下载最新版本的插件，上传至网站根目录并解压

## 配置
在`.config.php`中添加以下内容
```php
$_ENV['postal_host']    = ''; // Postal API地址
$_ENV['postal_key']     = ''; // Postal API密钥
$_ENV['postal_sender'] = ''; // 发件人邮箱
$_ENV['postal_name']   = ''; // 发件人名称
```
然后修改发信驱动 
```php 
$_ENV['mailDriver']      = 'postal';
```

## 问题
如果您在使用过程中遇到任何问题，欢迎提出Issue