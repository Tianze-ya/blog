---
title: 配置Kali-02
date: 2024-08-04
categories: os
tags:
  - kali
  - linux
---
## 一、修改用户名和密码

```shell
# 设置root用户密码，随后重启，登录root用户
sudo passwd root
# 更改用户名
usermod -l new_name kali
# 更好家目录名
mv /home/kali /home/new_name
usermod -d /home/new_name -m new_name
# 为用户设置新密码
passwd new_name
```

## 二、修改组名和主机名
```bash
# 更改组名
sudo groupmod -n new_name kali
# 更改主机名
sudo hostnamectl set-hostname new_hostname && sudo vim /etc/hosts
```
![](img/note/navigation/kali/hosts.png)

## 三、更改用户权限
```bash
# 通过修改sudoers达到效果（visudo指令），可用格式如下
# [用户名]    [被管理主机的IP]=([可以使用的身份])   [NOPASSWD: ][授权的命令]
# %[组名]    [被管理主机的IP]=([可以使用的身份])   [NOPASSWD: ][授权的命令]
# [被管理主机的IP]、[可以使用的身份]、[授权的命令] 都可以使用 ALL 来表示不限制
# 示例（NOPASSWD 不需要输入密码）
sudo visudo
new_name    ALL=(ALL)   NOPASSWD:ALL
```