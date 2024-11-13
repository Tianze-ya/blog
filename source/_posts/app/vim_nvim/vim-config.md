---
title: 配置Vim
date: 2024-08-12
categories: 软件
tags:
---
# 文件
我们将配文件存储在`~/.vim/vimrc`
其中.vim将会存储其他东西

# 键盘映射
`map a b`在全局下，把a映射到b
`noremap a b`在普通模式下，把a映射到b
此外`<CR>`是回车，`C-a`是Ctrl+a，`<nop>`是取消选项

# Plug
官网： https://github.com/junegunn/vim-plug
```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
在`~/.vim/vimrc`的末尾添加
```
call plug#begin("~/.vim/luggd")
call plug#end()
```
如果想安装插件在中间增加`Plug 'github user/github repo'
添加完成后执行`:PlugInstall`来安装

# 推荐插件
### vim-airline
Github：[vim-airline/vim-airline](https://github.com/vim-airline/vim-airline)
