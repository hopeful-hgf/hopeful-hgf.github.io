---
layout: post
title: debian更新遇到"Hash校验不符"
category: 技术
tags: linux
keywords: debian;upgrade;hash check
description: 
---

>在用debian系统时，更新遇到`无法下载×××,Hash校验不符`，在网上找到了原因和解决方法。



## debian更新"Hash校验不符"的原因和解决方法
### 这个问题其实有两部分原因

1. 网络问题

2. 压缩格式的问题

### 解决方法

1. /var/lib/apt/lists，把`lists`目录改个名字备份一下，重新 建一个同名目录，然后`apt-get update`

2. 由压缩格式造成的问题，在`/etc/apt/apt.conf.d/00aptitude`文件中（如果没有这个文件请自建）的最后一行添加如下内容：

   `Acquire::CompressionType::Order "gz";`

   然后重新：`apt-get update`

3. 如果还是不行，查看`sourcelist`文件中是否包含有源代码的源，如果有先注释掉，就可以啦。