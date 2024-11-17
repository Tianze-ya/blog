---
title: Nerd Font
date: 2024-11-17
categories: 软件
tags:
---
## 我正在使用的字体
[Hack Nerd Font](https://www.programmingfonts.org/#hack)

**Download for windows
[Hack Windows Installer](https://github.com/source-foundry/Hack-windows-installer/releases/latest)

**Download for Linux
```zsh
# 下载最新版本的字体文件
wget https://github.com/source-foundry/Hack/releases/download/v3.003/Hack-v3.003-ttf.zip
# 解压
unzip ./Hack-v3.003-ttf.zip
# 将字体文件复制到系统字体文件夹
cp ./ttf/* /usr/share/fonts/
# 或者复制到用户字体文件夹
cp ./ttf/* ~/.local/share/forts/
# 使用以下命令清除并重新生成字体缓存和索引
fc-cache -f -v
# 查看安装情况
fc-list | grep "Hack"
```

## 推荐的字体
[JetBrainsMono Nerd Font](https://www.programmingfonts.org/#jetbrainsmono)
[MesloLG Nerd Font](https://www.programmingfonts.org/#meslo)

## 更多
[Nerd Fonts](https://www.nerdfonts.com/font-downloads)
