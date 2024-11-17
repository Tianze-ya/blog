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

## 配置
```zsh
mkdir ~/.config/wezterm
vim ~/.config/wezterm/wezterm.lua
```

```lua
local wezterm = require("wezterm")
local config = {
	font_size = 15,
	font = wezterm.font("Hack", { weight = "Regular" }),
	color_scheme = "Catppuccin Mocha",
	use_fancy_tab_bar = false,
	hide_tab_bar_if_only_one_tab = true,
	window_decorations = "RESIZE",
	show_new_tab_button_in_tab_bar = false,
	window_background_opacity = 0.9,
	macos_window_background_blur = 70,
	text_background_opacity = 0.9,
	adjust_window_size_when_changing_font_size = false,
	window_padding = {
		left = 20, 
		right = 20,
		top = 20,
		bottom = 5,
	},
}

return config
```