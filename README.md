# Postal-For-SSPanel

## 介绍

为SSPanel提供通过Postal API发送邮件的功能 \
与SMTP协议相比，Postal API提供了更高的发送速度和更低的延迟 \
此插件理论上可以在2022.09之前的SSPanel上运行（不支持master分支） \
2023.02之后的SSPanel已内置了Postal API的支持，不再需要此插件

## 安装

下载源码并解压，将目录下的所有文件复制到SSPanel根目录下 \
在SSPanel网站根目录下执行以下命令

```bash
composer require postal/postal
```

## 配置

在`.config.php`中添加以下内容

```php
$_ENV['postal_host']    = ''; // Postal API地址
$_ENV['postal_key']     = ''; // Postal API密钥
$_ENV['postal_sender'] = ''; // 发件人邮箱
$_ENV['postal_name']   = ''; // 发件人名称
```

并修改发信驱动

```php 
$_ENV['mailDriver']      = 'postal';
```

## 问题

如果您在使用过程中遇到任何问题，欢迎提出Issue