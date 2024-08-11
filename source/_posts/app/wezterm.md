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
Path: `~/.wezterm.lua`
```lua
-- Pull this API
local wezterm = require 'wezterm';
local config = wezterm.config_builder()

-- Font and size
-- config.font = wezterm.font()
config.font_size = 19

-- Hide the tab bar(We use the Tmux all time)
config.enable_tab_bar = false
-- window
config.window_decorations = "RESIZE"

-- config the color
config.colors = {
    foreground = "#CBE0F0",
    background = "#011423",
    cursor_bg = "#47FF9C",
    cursor_border = "#47FF9C",
    cursor_fg = "#011423",
    selection_bg = "#033259",
    selection_fg = "#CBE0F0",
    ansi = { "#214969", "#E52E2E", "#44FFB1", "#FFE073", "#0FC5ED", "#a277ff", "#24EAF7", "#24EAF7" },
    brights = { "#214969", "#E52E2E", "#44FFB1", "#FFE073", "#A277FF", "#a277ff", "#24EAF7", "#24EAF7" },
}

-- window background
config.window_background_opacity = 0.8

return config
```