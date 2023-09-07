---
abbrlink: "54193"
categories:
  - 科研
  - 数据
created: 2023-04-21 01:11:00
description: 【原方法已失效，请看更新】
tags:
  - 三峡
  - Python
  - Data
updated: 2023-09-07 13:21:00
date: 2019-03-04
slug: TGRA-water-level-collector
title: 三峡库区水情水位信息获取
cover: https://i.cuger.cn/b/1647870596432-%E4%B8%89%E5%B3%A1%E5%BA%93%E5%8C%BA%E6%B0%B4%E4%BD%8D2001-2019.png
id: 0effffe0-d214-4381-8e5f-4e00baf41101
---

# 更新于 2021.06.04

目前该方法已经失效！三峡集团源站关闭了[查询页面](https://www.ctg.com.cn/sxjt/sqqk/index.html)，无法进行数据更新。博主已花大量时间将数据源切换到[千里眼水情查询系统](http://113.57.190.228:8001/#!/web/Report/RiverReport)，涵盖湖北省所有水库、大中小河流水文监测情况。

下载链接: [湖北省水文数据共享](https://cloud.cuger.cn/#/Data/%E6%B0%B4%E6%96%87)

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://cloud.cuger.cn/#/Data/水文"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">GONEList</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://cloud.cuger.cn/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://cloud.cuger.cn/#/Data/水文</div></div></div></a></div></div>

---

# 【下述方法已失效】

## Problem

**三峡库区库水位**作为一项基本的水文数据，在地灾、环境和水力等研究中极其重要。

设计 python 脚本采集库水位数据，每天自动同步，并提供下载。

- 数据来源：[【已失效】中国长江三峡集团有限公司](https://www.ctg.com.cn/sxjt/sqqk/index.html)
- 下载地址：[【已失效】ThreeGorgesWaterRegimen.xlsx](https://api.cuger.cn/ThreeGorgesWaterRegimenCollecter/ThreeGorgesWaterRegimen.xlsx)

## Solution

- **F12**分析网站查询请求，导入 postman，生成 python 代码；
- 撰写自动采集脚本，将数据存入 **mysql** 数据库备份（为后期前端分析使用及查询做准备）；
- 同时导出为 **xlsx** 文件提供用户下载；
- 利用 crontab 创建定时任务，每日定时更新 **xlsx** 文件。

## Feature

- **分时数据**，每日 2:00、8:00、14:00 和 20:00 都会有水位数据
- **数据丰富**，有上下游水位和库入库流速
- **多站点**，有三峡、葛洲坝、向家坝和溪洛渡等站点的数据

## Preview

![](https://i.cuger.cn/b/1647870596432-三峡库区水位2001-2019.png)

![](https://i.cuger.cn/b/1647870603474-三峡库区水位2019.png)

## Download

代码已部署于服务器，每日更新 Excel 文件。[下载地址](https://api.cuger.cn/ThreeGorgesWaterRegimenCollecter/ThreeGorgesWaterRegimen.xlsx)

## Others

源码: [Github](https://github.com/Doradx/ThreeGorgesWaterRegimenCollecter)

Email: [ddxid@outlook.com](mailto:ddxid@outlook.com)
