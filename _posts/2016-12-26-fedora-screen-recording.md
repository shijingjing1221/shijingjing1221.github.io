---
layout: post
title: Fedora使用 ffmpeg 录屏
tags:
- Fedora使用
- ffmpeg
categories: Fedora
description: ffmpeg真的是非常强大，既可以录制屏幕，也可以录制声音。
---
##官方网站
[ffmpeg](https://trac.ffmpeg.org/wiki/Capture/Desktop) 的录制文档在 https://trac.ffmpeg.org/wiki/Capture/Desktop

<!-- more -->
##录制音频和视频的常用命令

```
ffmpeg -video_size 1920x1080 -framerate 25 -f x11grab -i :0.0 -f alsa -ac 2 -i hw:0 output.mkv
```

或者

```
ffmpeg -video_size 1024x768 -framerate 25 -f x11grab -i :0.0 -f pulse -ac 2 -i default output.mkv

```