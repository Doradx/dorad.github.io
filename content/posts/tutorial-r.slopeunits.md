---
abbrlink: db83
categories:
  - 科研
  - GIS
created: 2023-05-16 15:59:00
description: |-
  该插件由意大利@Massimiliano基于GRASS平台开发，用于快速划分斜坡单元。
  原作者只适配了在Ubuntu下的操作，而本人尝试使用后发现并不好使，故想办法移植到Windows下使用。由于花费了不少心思摸索，故记录，方便下次查阅。
tags:
  - GIS
  - Python
status: 已发布
type: post
updated: 2023-09-04 09:43:00
date: 2023-05-16 08:00:00
filename: tutorial-r.slopeunits
title: 斜坡单元分割插件(r.slopeunits) windows移植方案
cover: https://i.cuger.cn/b/3366ea09-a053-4046-a9bf-9c16403b638e.jpg
id: 7a57bf57-63c2-48c8-a2b3-b60dda580fa9
---

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://gmd.copernicus.org/articles/9/3975/2016/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">GMD - Automatic delineation of geomorphological slope units with r.slopeunits v1.0 and their optimization for landslide susceptibility modeling</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.geoscientific-model-development.net/favicon_copernicus_16x16_.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://gmd.copernicus.org/articles/9/3975/2016/</div></div></div></a></div></div>

> 该插件由意大利@Massimiliano 基于 GRASS 平台开发，用于快速划分斜坡单元。

原作者只适配了 Ubuntu 系统，而未适配 windows，而本人尝试使用后发现并不好使，故想办法移植到 Windows 下使用。

由于花费了不少心思摸索，故记录，方便下次查阅。

# 快速开始

## QGIS 安装

- 确保自己安装了最新版本的 QGIS，GRASS 会一同被安装。
- 安装完成后，检查目录下是否有 GRASS 程序，程序应位于 QGIS/APP 目录下，例如：`D:\Program Files\QGIS 3.22.4\apps\grass\grass78\`。

## 安装 r.slopeunits

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://geomorphology.irpi.cnr.it/tools/slope-units"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">Slope Units Delineation</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://geomorphology.irpi.cnr.it/++theme++tecnoteca.irpitheme2018/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://geomorphology.irpi.cnr.it/tools/slope-units</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://geomorphology.irpi.cnr.it/@@site-logo/Logo-irpi-cnr.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div><div style="text-align: center; margin:0;"><p>官方网站</p></div></div>

- 在官方网站下载[**slu_grass78.tgz**](https://geomorphology.irpi.cnr.it/tools/slope-units/slu/slu_grass78.tgz)，并从中提取`r.slopeunits`文件，重命名为`r.slopeunits.py`
- 得到`r.slopeunits.py`文件后，复制到`D:\Program Files\QGIS 3.22.4\apps\grass\grass78\scripts`路径（根据自己的安装目录修改）下。

## Windows 适配

在`D:\Program Files\QGIS 3.22.4\apps\grass\grass78\bin`目录下，创建`r.slopeunits.bat`文件，内容如下：

```shell
@"%GRASS_PYTHON%" "%GISBASE%/scripts/r.slopeunits.py" %*
```

## 试运行

运行 GRASS GIS 即可，在 GUI 下即可调用 r.slopeunits 进行斜坡单元分割。

![试运行效果](https://i.cuger.cn/b/0b86fc0d-d9d2-4f19-8e16-70f854f42537.png)

> GRASS 中，调用命令之前记得先调用 r.region 设置边界，否则可能输出结果为空，详情见[r.region - GRASS GIS manual (osgeo.org)](https://grass.osgeo.org/grass82/manuals/r.region.html)

# 问题

近期不少同学发邮件私信我，问我各种问题，在此总结回复。

希望大家有问题发评论区，有空会回复，也可以给其他后来的童鞋一个参考。

- 命令行已经可以调用`r.slopeunits`，但是输出结果是空白？

请检查 r.region 是否提前调用，要设置成 DEM 一样的范围；另外，多试一些参数，调参，可能是参数不正确，具体参考原论文的参数。

本文使用的命令行参数如下，供参考：

```shell
r.slopeunits demmap=DEM_FILL@PERMANENT slumapclean=SluMapC@PERMANENT slumap=SluMap@PERMANENT thresh=50000 areamin=2000 cvmin=0.25 rf=10 maxiteration=5 --overwrite
```

> 如果已经可以调用`r.slopeunits`，说明移植已经成功，本教程目的已经达到；剩下的就是调参和各类 GRASS 软件的使用问题；此类问题可以在评论区提问，但请尽量不要发送邮件私信，感谢。

# 其它

使用该插件的同学应该都是做滑坡易发性评价相关的研究，如果此文帮到了你，方便的话可以引用以下论文，感谢！

- Xia, D., Tang, H., Glade, T., Tang, C., and Wang, Q.: Slope-units-based landslide susceptibility mapping based on graph convolutional network: A case study in Lueyang region, EGU General Assembly 2023, Vienna, Austria, 24–28 Apr 2023, EGU23-16472, [https://doi.org/10.5194/egusphere-egu23-16472](https://doi.org/10.5194/egusphere-egu23-16472), 2023.
- Xia, D., Tang, H., Sun, S., Tang, C., & Zhang, B. (2022). Landslide Susceptibility Mapping Based on the Germinal Center Optimization Algorithm and Support Vector Classification. _Remote Sensing_, _14_(11), 2707. [https://doi.org/10.3390/rs14112707](https://doi.org/10.3390/rs14112707)

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.mdpi.com/2072-4292/14/11/2707"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">Landslide Susceptibility Mapping Based on the Germinal Center Optimization Algorithm and Support Vector Classification</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">A landslide susceptibility model based on a metaheuristic optimization algorithm (germinal center optimization (GCO)) and support vector classification (SVC) is proposed and applied to landslide susceptibility mapping in the Three Gorges Reservoir area in this paper. The proposed GCO-SVC model was constructed via the following steps: First, data on 11 influencing factors and 292 landslide polygons were collected to establish the spatial database. Then, after the influencing factors were subjected to multicollinearity analysis, the data were randomly divided into training and testing sets at a ratio of 7:3. Next, the SVC model with 5-fold cross-validation was optimized by hyperparameter space search using GCO to obtain the optimal hyperparameters, and then the best model was constructed based on the optimal hyperparameters and training set. Finally, the best model acquired by GCO-SVC was applied for landslide susceptibility mapping (LSM), and its performance was compared with that of 6 popular models. The proposed GCO-SVC model achieved better performance (0.9425) than the genetic algorithm support vector classification (GA-SVC; 0.9371), grid search optimized support vector classification (GRID-SVC; 0.9198), random forest (RF; 0.9085), artificial neural network (ANN; 0.9075), K-nearest neighbor (KNN; 0.8976), and decision tree (DT; 0.8914) models in terms of the area under the receiver operating characteristic curve (AUC), and the trends of the other metrics were consistent with that of the AUC. Therefore, the proposed GCO-SVC model has some advantages in LSM and may be worth promoting for wide use.</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.mdpi.com/2072-4292/14/11/2707</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://pub.mdpi-res.com/remotesensing/remotesensing-14-02707/article_deploy/html/images/remotesensing-14-02707-g001-550.jpg?1654675767" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>
