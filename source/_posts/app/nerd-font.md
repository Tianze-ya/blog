---
title: Nerd Font
date: 2024-11-17
categories: 软件
tags:
---
## 我正在使用的字体
[MapleMono-NF](https://github.com/subframe7536/maple-font)

你可能需要下载
```bash
brew install p7zip
```

**Download for Linux
```bash
# 下载最新版本的字体文件
curl -OL https://github.com/subframe7536/maple-font/releases/latest/download/MapleMono-NF.zip
# 解压
7z x ./MapleMono-NF.zip
# 将字体文件复制到系统字体文件夹
sudo cp ./*.ttf /usr/share/fonts/
# 或者复制到用户字体文件夹
sudo cp ./*.ttf ~/.local/share/forts/
# 删除无用文件
rm -rf ./*.ttf
# 使用以下命令清除并重新生成字体缓存和索引
fc-cache -f -v
# 查看安装情况
fc-list | grep "Maple"
```

## 推荐的字体
[JetBrainsMono Nerd Font](https://github.com/JetBrains/JetBrainsMono)
[MesloLG](https://github.com/andreberg/Meslo-Font)
[Hack Nerd Font](https://github.com/source-foundry/Hack)

## 更多
[Nerd Fonts](https://www.nerdfonts.com/font-downloads)
