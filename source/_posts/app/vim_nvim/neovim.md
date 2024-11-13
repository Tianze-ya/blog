---
title: Nvim
date: 2024-08-15
categories: 软件
tags:
  - linux
---
# 简介
基于Vim所写的一款功能更强大的编辑器
# 安装
```bash
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz
sudo rm -rf /opt/nvim
sudo tar -C /opt -xzf nvim-linux64.tar.gz
```
在`~/.zshrc`中添加`export PATH="$PATH:/opt/nvim-linux64/bin"`即可
# 配置
## Plug
```bash
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```
在`~/.config/nvim/init.lua`的末尾添加
```
call plug#begin("~/.vim/luggd")
call plug#end()
```
如果想安装插件在中间增加`Plug 'github user/github repo'
添加完成后执行`:PlugInstall`来安装
