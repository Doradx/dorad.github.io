---
abbrlink: "63499"
categories:
  - 科研
  - 工具
created: 2023-04-21 01:11:00
description: 天下苦EndNote关联PDF久矣！故开发此插件，开启新的EndNote使用姿势！安装链接：SCI RIS Helper - from Greasy Fork
tags:
  - EndNote
  - SCI
  - RIS
  - PDF
  - 科研
  - 效率
  - Tampermonkey
updated: 2023-09-07 13:21:00
date: 2021-10-23
slug: sci-ris-helper
title: EndNote导入PDF文件关联（SCI-RIS-Helper）插件
cover: https://i.cuger.cn/b/35ca75c3dccfa471c199f067a097e2a2.png
id: e84a4b35-792f-497a-8d53-f5eeaebbf329
---

天下苦 EndNote 关联 PDF 久矣！故开发此插件，开启新的 EndNote 使用姿势！安装链接：[SCI RIS Helper - from Greasy Fork](https://greasyfork.org/zh-CN/scripts/434310-sci-ris-helper)

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://greasyfork.org/zh-CN/scripts/434310-sci-ris-helper"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">SCI RIS Helper - EndNote+Scihub</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">一键下载带论文PDF链接的Refman(*.ris)文件，快速导入EndNote并自动下载关联PDF文件，已适配WOS、Researchgate、Springer、ScienceDirect、Scopus和MDPI等80+种网站。</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://greasyfork.org/vite/assets/blacklogo16-bc64b9f7.png"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://greasyfork.org/zh-CN/scripts/434310-sci-ris-helper</div></div></div></a></div></div>

![SCI RIS Helper](https://i.cuger.cn/b/35ca75c3dccfa471c199f067a097e2a2.png)

# 一、介绍

本插件支持在下载**\*.ris**文件时自动关联 sci-hub 中的**pdf**链接，双击**\*.ris**文件将**自动下载 pdf 并进行关联**！

**再也不用手动将 PDF 拖进 EndNote 了！**

安装插件后，网页右下角将显示**圆角矩形图标**，三种颜色和文字代表三种不同状态，状态分别为：

- **RIS+**: 正常找到**Refman**和**PDF**信息，点击**RIS+**将下载 RIS 文件，双击即可导入 EndNote 并**自动关联 PDF**。（最理想的工作状态）
- **RIS**: 找到了**Refman**，但未找到**PDF**，点击**RIS**将下载 RIS 文件，双击即可导入 EndNote，但是不会关联 PDF。
- **NONE**: 啥也没找到，不支持该页面，按钮禁用。

![三种不同状态](https://i.cuger.cn/b/ad744dc87acf8eb2568166dcf1279e62.png)

如果在期刊页面未显示图标，则表明暂未适配该期刊。可将网址提交在**评论区**，博主空闲时随缘更新。

# 二、安装方法

## 1. 前提

本脚本基于 Chrome 油猴插件开发，所以需要使用 Chrome 内核浏览器，并提前安装油猴插件（[Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en)），[油猴插件安装教程](https://zhuanlan.zhihu.com/p/34967781)。

> 温馨提示：
>
> 1. Chrome 最好更新最新版，旧版本可能无法使用该脚本!（博主使用 92.0.4515.159，亲测 Chrome 79.0 翻车）
> 2. 另外：EndNote X9.2、EndNote X9 及汉化版无法成功导入 PDF，只会存在一个 PDF 链接！（博主使用的 EndNote X9.3.3, 亲测 EndNote 20 也可正常使用）

## 2. 插件安装

插件安装完成后，打开下方链接，即可安装【SCI RIS Helper】

【SCI RIS Helper 安装链接】：

- [SCI RIS Helper - from Greasy Fork](https://greasyfork.org/zh-CN/scripts/434310-sci-ris-helper)
- [SCI RIS Helper - from Github](https://github.com/Doradx/CNKI-PDF-RIS-Helper/raw/master/SCI%20RIS%20Helper.user.js)

## 3. 插件使用

脚本更新后，已将 scihub 和 doi 域名加入白名单，已不会出现以下提示信息，但不影响正常使用。

~~安装完成后，由于脚本会调用 https://dx.doi.org/ 和 http://sci-hub.se/，所以会产生跨域请求，点击【总是允许此域名】即可。~~

![跨域请求(目前已经不存在该问题)](https://i.cuger.cn/b/63999b30353f60f462e8448db1d85d80.png)

打开[期刊页面](https://nhess.copernicus.org/articles/13/299/2013/)，查看是否存在图标，下载 RIS 文件，测试是否能正常导入 EndNote 并自动关联 PDF。

# 三、灵感来源&原理

_如果是想单纯用插件的同学可以跳过该部分_

## 1. 发现过程

某次正常下载 RIS 文件并导入 EndNote 时，发现 EndNote 居然自动导入了 PDF 文件！论文网址: https://nhess.copernicus.org/articles/13/299/2013/

研究后发现，其下载的 RIS 与其它 RIS 文件唯一不同的是：该 RIS 文件包含了一个 PDF 网址的字段：`L1 -`，如下图所示。

![NHESS网站发现RIS的奥秘](https://i.cuger.cn/b/9eecbbc1a15a33b3d0ba2f559cd2aca5.png)

我大为震惊！原来可以这么玩！

我试着将上述 HTTP 链接更换为本地 PDF 文件绝对路径，发现也可以成功关联 PDF！

尝试着使用[SCI-HUB](https://sci-hub.se/)上的 PDF 链接进行关联，初步实验可行！

由于之前有油猴脚本开发经验（[CNKI 知网油猴插件-一键导入 Endnote&下载 PDF](https://blog.cuger.cn/p/5187/)），故又开始重操旧业！

## 2. 脚本原理

脚本原理其实很简单，主要分为四步：

- [1] 寻找页面 DOI、标题、摘要和 PDF 链接；
- [2] 根据 DOI，在 https://citation.crosscite.org/docs.html 查询论文信息（Refman 文件）；
- [3] 根据 DOI，在[SCI-HUB](https://sci-hub.se/)寻找 PDF 链接；
- [4] 综合出版商和[SCI-HUB](https://sci-hub.se/)的 PDF 链接，将 PDF 链接和摘要添加到 RIS 文件，并下载。

# 四、兼容性

## 1. EndNote

EndNote 博主使用的 X9.3.3 版本，完美使用！

目前已知支持版本：EndNote 9.3.3、EndNote 20.2.1

目前已知不兼容版本：EndNote X9.2、EndNote X9 汉化版

## 2. Citavi 6

将 RIS 文件默认打开方式改为 Citavi 6 后，双击 RIS 文件即可导入 Citavi 6。

Citavi 6 测试结果表明，在导入过程中，其不会自动下载，但是会保存论文 PDF 链接。

预览窗口“Always preview this location immediately”将会自动下载预览，点击“Save a copy in this project”将在本地存储备份。

![Citavi 6 导入结果](https://i.cuger.cn/b/27e8bb06-100e-45f2-b40a-dda8acaff851.png)

## 3. NoteExpress

经测（NoteExpress），可以成功导入，并导入 PDF 链接，但是不会自动下载 PDF, 需要点击链接自行下载。

![NoteExpress导入情况](https://i.cuger.cn/b/14e14eb07e338279837380d4f444e32f.png)

# 五、其它

油猴脚本开发过程中，参考了[Publication Auto PDF](https://greasyfork.org/zh-CN/scripts/38628-publication-auto-pdf)相关逻辑，在此感谢[sincostandx](https://greasyfork.org/zh-CN/users/171198-sincostandx)！

## 1. 视频介绍&教程

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><iframe src="//player.bilibili.com/player.html?bvid=BV1Sv411u7fv&page=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; margin:0; aspect-ratio: 16/9;"> </iframe><div style="text-align: center; margin:0;"><p>博主自制教程</p></div></div>

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><iframe src="//player.bilibili.com/player.html?bvid=BV1LM411V7GK&page=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; margin:0; aspect-ratio: 16/9;"> </iframe><div style="text-align: center; margin:0;"><p>其它UP制作的教程@可乐仔，简洁明了，推荐观看</p></div></div>

## 2. 参考代码及网址

- [Publication Auto PDF](https://greasyfork.org/zh-CN/scripts/38628-publication-auto-pdf)
- https://nhess.copernicus.org/articles/15/853/2015/
- https://citation.crosscite.org/docs.html
- http://sci-hub.se/

## 3. 源码及英文版介绍

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://github.com/Doradx/CNKI-PDF-RIS-Helper/blob/master/SCI%20RIS%20Helper.user.js"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">github.com</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://github.com/Doradx/CNKI-PDF-RIS-Helper/blob/master/SCI%20RIS%20Helper.user.js</div></div></div></a></div></div>

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://github.com/Doradx/CNKI-PDF-RIS-Helper/blob/master/README-SCI-RIS-Helper.md"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">github.com</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://github.com/Doradx/CNKI-PDF-RIS-Helper/blob/master/README-SCI-RIS-Helper.md</div></div></div></a></div></div>

## 4. 注意！！！

本插件使用过程中会将以下信息发送到博主服务器：

- 论文 RIS 信息，积累可构成数据库。包括：`doi`，`title`，`year`，`ris`, `pdfUrl`
- 使用日志, 方便分析受众面。包括：`action`, `userAgent`, `ip`

使用本插件默认你已知晓并同意以上事项。

本插件完全免费开源，如不想上传信息，可**自行删除**相关 API，不影响正常使用。

本插件纯属摸鱼产物，使用过程出现的任何情况，作者不承担任何责任。

## 5. 问题反馈

在 GitHub 提交 Issues 或者在评论区留言。

<div style="margin:5px 1px;"> <a href="https://github.com/Doradx/CNKI-PDF-RIS-Helper/issues" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/23170065?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">Doradx/CNKI-PDF-RIS-Helper  Issues</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">Doradx</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2021-04-17T03:00:31Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

# Tips

由于大家过于给力，上线以来，本插件收录论文 RIS 已超`10w`条，使用日志`100w`条。

现在我开始担心我腾讯云的小水管了。。。

# 统计

![greasyfork提供的每日安装次数统计](https://i.cuger.cn/b/e9908603-58d6-4771-88c4-217453ccf357.png)

从统计图也可以看出大家在 3 月和 9 月时的学习激情最高！

# 作者

[Dorad](https://blog.cuger.cn/), ddxid@outlook.com
