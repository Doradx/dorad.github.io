---
abbrlink: "64568"
categories:
  - 科研
  - GIS
created: 2023-04-21 01:01:00
description: 最近大疆精灵4RTK版本更新支持了“仿地飞行”模块，这对于经常在山区飞行的小伙伴来说无疑是极好的，动辄几百米的高差如果仅能在一定的高度飞行，无论是成像质量还是重叠度都很难有保障，而飞行器如果能根据地面起伏以相对恒定的高度飞行，不仅能够保障飞行器的安全而且成像质量也会有极大提升。但对于此功能官方并未给出详细的操作教程，网上各种信息说的也是含糊不清，给很多用户造成了极大的困扰，故写下此文与各位飞手分享，希望能有所帮助。
tags:
  - 大疆
  - 仿地飞行
  - DEM
updated: 2023-09-07 11:23:00
date: 2019-08-08
title: 大疆精灵4RTK仿地飞行教程
cover: https://i.cuger.cn/b/1647870299451-2019-08-08-21-16-24.png
id: 58d69c09-fa6d-4ee5-9249-512065190cc6
---

# 写在前面

最近大疆精灵 4RTK 版本更新支持了“仿地飞行”模块，这对于经常在山区飞行的小伙伴来说无疑是极好的，动辄几百米的高差如果仅能在一定的高度飞行，无论是成像质量还是重叠度都很难有保障，而飞行器如果能根据地面起伏以相对恒定的高度飞行，不仅能够保障飞行器的安全而且成像质量也会有极大提升。

但对于此功能官方并未给出详细的操作教程，网上各种信息说的也是含糊不清，给很多用户造成了极大的困扰，故写下此文与各位飞手分享，希望能有所帮助。

# 实现方法

目前，该功能主要有两个实现途径：

## 自制 DSM 数据

一是自制数字表面模型（DSM）数据，首先在研究区内采用正射的方法飞行一遍，然后利用 Pix4d 等空三软件，生成研究区的 DSM，然后将 DSM（包括 tif 和 tfw）两个文件导入遥控器中。该种方法生成的 DSM 相对较为精细，可以实现更好的仿地效果，但工作量较大，且对于山区高差较大的区域，首次飞行时安全问题难以保证。

## 借用现有 DEM 替代 DSM

二是直接使用已有的数字高程模型（DEM）来替代 DSM，DEM 数据相对 DSM 数据来说缺少植被、建筑等高程信息，因此在采用 DEM 替代 DSM 进行仿地飞行时要注意飞行区内的植被、建筑物及高压电线塔等构筑物的高度。目前覆盖全国的公开 DEM 数据有空间分辨率为 SRTM90m、ASTER GDEM30m、ALOS12.5m 的可供下载。较为方便的下载地址有：

- 地理空间数据云: http://www.gscloud.cn/(90/30m免费，需要注册账号)
- 百度网盘：链接：https://pan.baidu.com/s/1waqY2VNNz8Q6FlJZenvk0A 提取码：2wnp（30m，GIS 前沿公众号提供）
- LocaSpace：在 LocaSpace Viewer 软件中点击下载工具，圈定下载区域，选择地形下载即可得到一个裁剪好的 TIF 格式的 DEM 数据，该数据精度为 90m。此种方法经常失效，大区域慎重采用。此外该公司提供原始 DEM 数据下载服务，需收取一定费用：[30m](http://www.tuxingis.com/resource/aster.html) [12.5m](http://www.tuxingis.com/resource/dem_12_download.html)速度相对快，目前仅部分省份有数据）
- Alaska Satellite Facility: https://www.bilibili.com/video/av19558468/ （12.5m 官方下载教程)

# 使用方法

以 ALOS12.5m 精度的汉中市固城县 DEM 作为案例详细讲解。

![](https://i.cuger.cn/b/1647870269311-2019-08-08-21-14-09.png)

## 数据转换

### UAV 软件转换

由于 DJI 对于数据格式的要求，首先需要对下载得到的 DEM（tif 格式，WGS84 地理坐标）进行转换，为方便起见，目前有两种较为便捷的途径可以实现： windows 平台下载 UAV Mate 软件，使用其 DSM TIFF 工具，进行转换并生成 TFW 文件。（可申请试用，试用期过后需要购买软件才可继续试用。）

![UAV Mate软件转换效果](https://i.cuger.cn/b/1647870272853-2019-08-08-21-14-42.png)

![转换得到的结果文件](https://i.cuger.cn/b/1647870283789-2019-08-08-21-14-56.png)

### 在线转换

将下载好的 DEM 上传到

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://dji.cuger.cn/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">DJI DSM Tool - 大疆仿地飞行DSM数据在线转换工具</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://dji.cuger.cn/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://dji.cuger.cn/</div></div></div></a></div></div>

[https://dji.cuger.cn/](https://dji.cuger.cn/)

网站上，稍等片刻点击数据下载，即可得到两个文件一个为转换好的 tif，另一个为 tfw 文件。由于在线操作，因此最好将 tif 文件大小限制在 100MB 以下。（该网站对于大文件需要收取少量的服务费）。

![在线转换网站](https://i.cuger.cn/b/1647870278030-2019-08-08-21-15-19.png)

通过以上工作，我们已经获得了可供 DJI 识别的 tif 和 tfw 两个文件 ## 2.2 数据导入 - 将无人机遥控器右下角的内存卡拔出，连接到电脑上，创建文件夹 DJI→DSM（此处务必按要求来，否则程序无法识别）在 DSM 文件夹下创建研究区文件夹（固城县），将上面转好的两个文件放入固城县文件夹下（该文件夹内只能放以上两个文件.tif 和.tfw）。

![遥控器内存卡取出](https://i.cuger.cn/b/1647870293374-2019-08-08-21-15-43.png)

- 将内存卡插回遥控器，打开电源（支持热插拔开机状态下亦可），屏幕会弹出导入 DSM 选项，若没有弹出可手动点击屏幕左下角内存卡选项，导入上面做好的 DSM 文件。 - 点击规划 → 仿地飞行，屏幕右侧选择区域（固城县），待数据读取完毕，手动将屏幕区域移到固城县（数据量较小时，程序会自动将有 DSM 数据的区域以阴影的方式凸显出来，区域较大时则无特殊标识），点击右下角规划航点，在屏幕上编辑区域即可看到屏幕下方有无人机相应节点的飞行高度。

![仿地飞行航线规划](https://i.cuger.cn/b/1647870296269-2019-08-08-21-15-59.png)

> 注意：由于遥控器数据处理的限制，尽量使 tif 文件的大小在 100MB 以内，以保证软件的流畅运行，文件压缩会造成地形精度的下降，飞行高度设置较低时要注意安全问题。效果展示：

![仿地飞行效果展示](https://i.cuger.cn/b/1647870299451-2019-08-08-21-16-24.png)

该区域前后缘高差约 200m，规划用 DEM 精度为 12.5m，仿地精度 10m，飞行高度 80m，无人机能够按照设定方式稳定的飞行，获得了良好的测量结果。

# Tips:

该[转换工具](https://dji.cuger.cn/)由博主自主开发。 Email:[ddxid@outlook.com](mailto:ddxid@outlook.com)

但对于此功能官方并未给出详细的操作教程，网上各种信息说的也是含糊不清，给很多用户造成了极大的困扰，故写下此文与各位飞手分享，希望能有所帮助。
