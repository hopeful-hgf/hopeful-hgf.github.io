---
layout: post
title: python 打开文件时编码格式的探测
category: 技术
tags: python
keywords: python encoding
---
## 1. 思路
用二进制打开文件，用#chardet#模块探测编码

## 2. 实现

```python
import chardet
wiht open('filename','rb') as f:
    data=f.read()
print(chardet.detect(data))
```

