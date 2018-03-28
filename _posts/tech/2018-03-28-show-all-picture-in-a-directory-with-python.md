---
layout: post
title: 用网页展示目录下的所有图片
category: 技术
tags: python; html
keywords: python; html; 
description: 
---

>用局域网网页来分享照片的暴力方法

## 依赖 
- python
- localnetwork

## 实现

1. 网页的生成

   将所有照片放到同一个目录下，

   执行如下python代码

   ```python
   import os


   def main():
       dirlist=os.listdir("./")
       print(dirlist)
       with open('index.html','w') as wf:
           for it in dirlist:
               wf.write('<img src="'+it+'" Style="width:600px;height:400px;"/>\n')

   if __name__=='__main__':
       main()
   ```

   将生成一个`index.html`文件

2. 开启HTTPServer

   ```shell
   python -m SimpleHTTPServer
   ```

3. 同一局域网下，浏览器访问 `主机ip:8000`

## 缺点

1. 简单暴力

   网页将加载所有的图片，不经压缩，卡顿，速度慢

## 待改进

1. 。。。。。。。。。。。



## Other

1. display the filesystem 

   ```shell
   df -h
   ```

2. display or manipulate a disk partition table

   ```shell
   fdisk -l
   ```

   ​

3. mount & umount

   ```shell
   cd /mnt/
   mkdir sd
   mount /dev/sda1 /mnt/sd
   # ok
   cd /mnt/sd/sd
   ```

   ​




