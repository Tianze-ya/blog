---
title: 配置Kali-02
date: 2024-08-04
categories: os
tags:
  - kali
  - linux
---
### 一、修改用户名及密码
```shell
# 设置root用户密码，随后注销当前用户，登录root用户
sudo passwd root
# 更改用户名
usermod -l new_name old_name
# 更改组名
groupmod -n new_name old_name
# 更好家目录名
mv /home/old_name /home/new_name
usermod -d /home/new_name -m username
# 更改 passwd 文件中用户的家目录
vim /etc/passwd
```