---
abbrlink: 4dc2a61c
categories:
  - 编程
created: 2023-04-19 03:59:00
description: 给Gay Hub上的各位安全地添加上备注。
tags:
  - Tampermonkey
  - GitHub
updated: 2023-09-07 11:23:00
date: 2023-04-17
slug: github-remark
title: GitHub Remark|给Gay Hub的小伙伴加备注
cover: https://i.cuger.cn/b/49e8ae3c-bf2c-4468-88f9-5bb67c95c905.png
id: 29d75c91-6be1-4cf3-9441-3149d963dd71
---

# 项目介绍

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://greasyfork.org/zh-CN/scripts/443857-github-remark"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">GitHub Remark</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">GitHub remark</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://greasyfork.org/vite/assets/blacklogo16-bc64b9f7.png"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://greasyfork.org/zh-CN/scripts/443857-github-remark</div></div></div></a></div></div>

为给 GitHub 上的童鞋标记备注而生。本地化方案，方便、安全。

# 起因

`GitHub` 无法添加备注，想给各位小伙伴加上备注，但又`担心数据安全问题`。Fork 一[在线方案](https://github.com/dpy1123/GithubRemark)后，改为了离线方案，故有此项目。

> 此方案已并入原作者仓库：[GithubRemark/tampermonkey](https://github.com/dpy1123/GithubRemark/tree/master/tampermonkey)

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://chrome.google.com/webstore/detail/githubremark/mfimgdoejnljagjkeeieiidhejnnoicp"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">GithubRemark</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">给你的Github好友增加备注名吧～</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.google.com/images/icons/product/chrome_web_store-32.png"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://chrome.google.com/webstore/detail/githubremark/mfimgdoejnljagjkeeieiidhejnnoicp</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://lh3.googleusercontent.com/48VhSM_D5ZIK5PJtlU8MeHd78EVYhjFJBT3Mtlcvq8Aa0DZbJJIb1jXHGEDmGdIR01DogTm2N_X-bhn-kkEOYNIFzg=w128-h128-e365-rj-sc0x00ffffff" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div><div style="text-align: center; margin:0;"><p>原Chrome插件，存在较大安全问题，</p></div></div>

# 用途

给 GitHub 上的各位小伙伴打上备注名称，采用离线存储方式。

设置好的备注在 GitHub 的各类页面中均会显示，包括但不限于 Home、followers、following

# 安装

> 本项目基于[Tampermonkey](https://www.tampermonkey.net/)，如无，请先安装此浏览器插件。

- 从 GitHub 安装：[GitHub Remark (github.com)](https://raw.githubusercontent.com/dpy1123/GithubRemark/master/tampermonkey/GitHubRemark.js)
- 从 Greafork 安装：[GitHub Remark (greasyfork.org)](https://greasyfork.org/zh-CN/scripts/443857-github-remark)

安装成功后，打开 GitHub 个人主页，会在个人名称下显示`(unset)`，表明未设置备注，双击编辑备注即可。

# 使用

## 添加/修改备注

对于未设置备注的用户，其旁边会显示`(unset),` 双击并编辑即可！

对于已添加备注的用户，直接双击备注，在弹窗中修改即可！

![备注设置示意图](https://i.cuger.cn/b/51bc8173-d5ec-444e-a225-a81d10b07c42.png)

## 数据备份/同步

备注数据会存储在浏览器的`Local Storage`中的`GithubRemark-cache`字段中，如需备份，在`GitHub`页面按`F12`，切换到`Application->Local Storage`，复制或修改`GithubRemark-cache`字段即可，其存储格式为`JSON`，可复制粘贴到本地或者密码记录软件进行备份。

![Local Storage存储的数据](https://i.cuger.cn/b/f4307461-ae66-4563-89ec-1d9f64627ee1.png)

我个人将其存储在`KeePass2`中，方便在不同 PC 上使用。

# 数据安全

由于一般备注都是实名，或者是接近实名，包含隐私信息，[原作品(GitHubRemark-Chrome 插件)](https://chrome.google.com/webstore/detail/githubremark/mfimgdoejnljagjkeeieiidhejnnoicp)采用云端存储方式，但 API 缺乏鉴权，且存在高度数据泄露危险（[详见我提的 issue](https://github.com/dpy1123/GithubRemark/issues/7)）！**个人非常不建议使用该 Chrome 插件！**方便快捷、云端同步，会成为数据泄露的窗口。

<div style="margin:5px 1px;"> <a href="https://github.com/dpy1123/GithubRemark/issues/7" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/23170065?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">建议添加鉴权，或添加删除云端数据的方式 <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="12.5" height="12.5"><path d="M11.28 6.78a.75.75 0 0 0-1.06-1.06L7.25 8.69 5.78 7.22a.75.75 0 0 0-1.06 1.06l2 2a.75.75 0 0 0 1.06 0l3.5-3.5Z"></path><path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0Zm-1.5 0a6.5 6.5 0 1 0-13 0 6.5 6.5 0 0 0 13 0Z"></path></svg> #7<span style="margin-left:3px;margin-right:3px">•</span>Closed</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="12.5" height="12.5"><path d="M11.28 6.78a.75.75 0 0 0-1.06-1.06L7.25 8.69 5.78 7.22a.75.75 0 0 0-1.06 1.06l2 2a.75.75 0 0 0 1.06 0l3.5-3.5Z"></path><path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0Zm-1.5 0a6.5 6.5 0 1 0-13 0 6.5 6.5 0 0 0 13 0Z"></path></svg> #7<span style="margin-left:3px;margin-right:3px">•</span>Doradx</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2023-04-17T11:25:10Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

# 参考

- [dpy1123/GithubRemark: 给 Github 上的用户增加备注名](https://github.com/dpy1123/GithubRemark)
