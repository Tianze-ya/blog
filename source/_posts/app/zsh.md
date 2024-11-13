---
title: Zsh
date: 2024-08-11
categories: 软件
tags:
  - linux
---
# 简介
一款扩展性强的shell

# 安装
安装zsh
```bash
sudo apt install zsh
```
设置为默认shell
```bash
chsh -s /bin/zsh
```

# 插件
### 安装oh-my-zsh
```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### 安装powerlevel10k
*弃*
```bash
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```
打开~/.zshrc
将`ZSH_THEME`的值改为`powerlevel10k/powerlevel10k`
并添加`POWERLEVEL9K_MODE="awesome-patched"`
重载
```bash
source ~/.zshrc
```
之后完成配置即可
重新配置p10k
```bash
p10k configure
```
### 安装Starrship
```bash
curl -sS https://starship.rs/install.sh | sh
```
安装完后再`~/.zshrc`的最后添加`eval "$(starship init zsh)"`即可
配置文件在`~/.config/starship.toml`

## 插件
### zsh- autosuggestion
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
打开~/.zshrc
将`plugin=(git)`改为
```
plugin=(git
		zsh-autosuggestion
)
```

### zsh-syntax-highlighting
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```
打开~/.zshrc
将`plugin`项改为
```
plugin=(git
		zsh-autosuggestion
		zsh-syntax-highlighting
)
```
## 配置
## 管理历史记录
打开~/.zshrc 添加以下内容
```
# history setup
HISTFILE=$HOME/.zhistory
SAVEHIST=1000
HISTSIZE=999
setopt share_history
setopt hist_expire_dups_first
setopt hist_ignore_dups
setopt hist_verify

# completion using arrow keys (based on history)
bindkey '^[[A' history-search-backward
bindkey '^[[B' history-search-forward
```