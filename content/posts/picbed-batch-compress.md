---
abbrlink: 75cd
categories:
  - 博客
  - CDN
created: 2023-04-22 06:22:00
description: 由于最近上传了不少高清大图，导致图床存储量飙升，开始担心我的钱包。故花点功夫对图床上现有的图片进行批量压缩，减少数据量。
tags:
  - Shell
  - 图床
  - 图片压缩
  - CDN
status: 已发布
type: post
updated: 2023-09-04 09:43:00
date: 2023-04-22 06:00:00
filename: picbed-batch-compress
title: CDN流量太贵？图床图片批量压缩替换
cover: https://i.cuger.cn/b/7b333366-1baa-4e09-9df5-82584aa4e00f.png
id: c70aa029-7d86-43a5-9afa-fea902b5ed75
---

# 初衷

最近倒腾了[Notion2markdown](https://blog.cuger.cn/p/634642fd/)写作，上传了很多高清大图，但没想到 CDN 流量账单一路狂飙。。。

遂出此策，将封面图统一调小，另将图床上的图片批量压缩后重新上传，减少流量消耗（穷）。

# 实现步骤

对 Notion 上传的封面图片：

- 统一用`PowerToys`提供的`Image Resizer`进行尺寸压缩，压缩到`800×600px`进行替换

对于图床上的既有图片：

- 从图床批量打包下载原图
- 在`Linux`系统下（博主采用的`WSL2/Ubuntu 22.04 TLS`），使用`compress.sh`进行图片批量压缩，采用的图片质量为`50%`，可自定义
- 重新上传到图床，覆盖原文件
- 原图打包丢网盘保存，备用

重新配置图床`CDN`图片浏览器缓存时间，增加到 30 天，开启防盗链。

下面重点介绍压缩过程。

# 批量压缩

主要介绍采用`compress.sh`脚本进行批量压缩的过程，其采用`ImageMagick`命令对图片进行压缩。

`compress.sh`脚本已共享，见[源码](https://gist.github.com/Doradx/a1c4b502958895a281e5770ed8dc14f1)。

执行方法如下：

```shell
./compress.sh <source_path> <output_path> [quality]
```

参数说明：

- `source_path` 原图目录
- `output_path` 压缩后图片保存位置
- `quality` 压缩后的图片质量百分比，默认`80%`

以下是将`source`文件夹下所有图片质量压缩到`50%`，并输出到`compressed`的命令行案例：

```shell
./compress.sh ./backups ./output 50
```

# 效果

## 本地

![压缩前约830M，压缩后280M，减少66%（选用的图片质量为50%，供参考）](https://i.cuger.cn/b/511251bc-7083-4db5-abb0-cafec363a502.png)

## COS 腾讯云

![直接减半，减少钱包烦恼](https://i.cuger.cn/b/eea97ad1-0176-4008-9561-73f46362e197.png)

# compress.sh

所撰写的核心代码如下：

```shell
#!/bin/bash
###
# @Author: Dorad, ddxi@qq.com
# @Date: 2023-04-22 00:04:43 +02:00
# @LastEditors: Dorad, ddxi@qq.com
# @LastEditTime: 2023-04-22 00:18:13 +02:00
# @FilePath: \compress.sh
# @Description:
#
# Copyright (c) 2023 by Dorad (ddxi@qq.com), All Rights Reserved.
###

# 输入文件夹路径和输出文件夹路径

# 获取输入参数
if [ $# -lt 2 ]; then
    echo "Usage: $0 input_dir output_dir <quality%>"
    exit 1
fi

if [ ! -d "$1" ]; then
    echo "Input dir $1 not exists"
    exit 1
fi

input_dir=$1
output_dir=$2
# 压缩后的图片质量百分比, 默认为 80
if [ -z "$3" ]; then
    quality=80
else
    quality=$3
fi

# 检查convert命令是否存在
if ! command -v convert &>/dev/null; then
    echo "convert command not found, please install ImageMagick first"
    exit 1
fi

# 遍历输入文件夹下所有图片文件
find $input_dir -type f -iname '*.jpg' -o -iname '*.jpeg' -o -iname '*.png' -o -iname '*.gif' | while read file; do
    # 创建输出文件夹的相同目录结构
    relative_path=${file#"$input_dir"}
    output_file="$output_dir/$relative_path"
    echo "Output file: $output_file"
    # 创建输出文件夹
    mkdir -p "${output_file%/*}"
    # 压缩图片并输出到相应的文件夹下
    convert "$file" -quality $quality "$output_file"
    echo "Compress $file, output to $output_dir/$file"
done

echo "Total files: $(find $input_dir -type f -iname '*.jpg' -o -iname '*.jpeg' -o -iname '*.png' -o -iname '*.gif' | wc -l)"
echo "Compressed files: $(find $output_dir -type f -iname '*.jpg' -o -iname '*.jpeg' -o -iname '*.png' -o -iname '*.gif' | wc -l)"
echo "Done!"
```

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://gist.github.com/Doradx/a1c4b502958895a281e5770ed8dc14f1"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">A shell script to batch compress all images under a folder, based on ImageMagick.</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">A shell script to batch compress all images under a folder, based on ImageMagick. - compress.sh</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://github.githubassets.com/favicons/favicon.svg"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://gist.github.com/Doradx/a1c4b502958895a281e5770ed8dc14f1</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://github.githubassets.com/images/modules/gists/gist-og-image.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div><div style="text-align: center; margin:0;"><p>源码直达</p></div></div>

# 参考

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://openai.com/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">OpenAI</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">Creating safe AGI that benefits all of humanity</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://openai.com/</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://images.openai.com/blob/fb4a2ba6-9109-4c7b-af4d-cae530c3fa78/recruitment-video-poster.jpg?trim=0%2C0%2C0%2C0&width=1000&quality=80" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.ilovexinji.com/imagemagick/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">在Ubuntu下使用imagemagick批量提高或压缩图片质量 - 星空下的狼</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">在Ubuntu下使用imagemagick的convert批量提高或压缩图片质量、转换图片格式、旋转图片</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.ilovexinji.com/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.ilovexinji.com/imagemagick/</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="http://www.ilovexinji.com/wp-content/uploads/2021/10/ImageMagick_logo.svg_.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>
