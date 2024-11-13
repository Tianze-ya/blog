---
title: Wezterm
date: 2024-08-11
categories: 软件
tags: []
---
# 简介
一款由Rust编写的Terminal
具有强大的定制化内容
官网： https://wezfurlong.org/wezterm/

# 安装
更新源
```bash
curl -fsSL https://apt.fury.io/wez/gpg.key | sudo gpg --yes --dearmor -o /usr/share/keyrings/wezterm-fury.gpg
echo 'deb [signed-by=/usr/share/keyrings/wezterm-fury.gpg] https://apt.fury.io/wez/ * *' | sudo tee /etc/apt/sources.list.d/wezterm.list
sudo apt update
```
下载
```bash
sudo apt install wezterm
```

# 配置
FilePath: `~/.wezterm.lua`
