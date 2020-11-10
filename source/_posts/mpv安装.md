---
title: mpv安装
date: 2020-11-10 17:26:49
categories: 杂项 
tags: 
    - 安装
    - MVP
---
# 一、安装

## 1.方式一:brew 安装

brew install mpv

## 2.方式二：源码安装

下载源码：https://github.com/mpv-player/mpv/

```bash
  $ ./bootstrap.py
  $ ./waf configure
  $ ./waf
  $ ./waf install
  ```

# 3.生成app

网上说可以使用 brew linkapps mpv，但是新版本的brew已经将linksapps操作给删掉了。
直接执行 brew cask install mpv即可，安装之后发现mpv已经出现在了lauchpad里面并且可以打开使用了。

# 4.配置

```bash
// 切换到mpv文件夹
$ /Users/yourname/.config/mpv

// 创建配置文件
$ touch mpv.conf
```

## mpv.conf

```properties
# mpv.conf
hwdec=auto
autofit-larger=92%
video-sync=display-resample
sub-codepage=enca:zh:utf8
sub-auto=fuzzy
sub-font-size=40
sub-shadow-offset=0
sub-color="#ffffffff"
sub-font="STZhongsong"
sub-codepage=utf8:gb18030
screenshot-template=mpv-screenshot-%f-%p
screenshot-format=png
osd-font="STZhongsong"
osd-font-size=36
--script=/Users/jinyinjie/.config/mpv/autoload.lua
```

# 5.使用

```bash
$ mpv http://dlhls.cdn.zhanqi.tv/zqlive/43626_vQOn9.m3u8
```

