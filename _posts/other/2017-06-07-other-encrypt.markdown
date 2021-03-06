---
layout: post
category: "other"
title:  "对称与非对称加密"
tags: [Other]
---

### 对称加密 ###

- 采用对称的密码编码技术，他的特点是，加密和解密使用相同的秘钥  
- 常见有DES AES RC4等  
- 优点：加解密速度快  缺点：防止秘钥泄露是一个难点

<!-- more -->  

### 非对称加密 ###

- 因为加密和解密使用的是两个不同的密钥。故公开密钥对数据进行加密，只有对应的私有密钥才能解密；私有密钥对数据进行加密，只有用对应的公开密钥才能解密。  
- 常见有RSA DSA等  
- 优点：安全性更高，公钥是公开的，秘钥是自己保存的，不需要将私钥给别人。 缺点：加密和解密花费时间长、速度慢，只适合对少量数据进行加密

### 对称与非对称同时使用 ###

对数据采用对称加密，对密钥采用非对称加密。后端收到使用非对称解密出密钥，然后使用该密钥对加密数据进行对称解密