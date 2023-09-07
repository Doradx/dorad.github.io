---
abbrlink: "5664"
categories:
  - 生活
  - 工具
created: 2023-09-05 11:38:00
description: 最近Adobe系列经常出现Your Adobe app is not
  genuine弹窗，尝试了各类HOST方案后，发现经常不能和Clash客户端的DNS服务共存。
tags:
  - Adobe
  - Clash
updated: 2023-09-07 11:03:00
date: 2023-09-05
slug: adobe-app-genuine
title: "[Adobe]Your Adobe app is not genuine解决方案-Clash版"
cover: https://i.cuger.cn/b/d38fcb8e-fd9e-4143-9785-6fe4b8f427bb.jpg
id: f659789f-baf3-48e8-b750-67ab54a77479
---

# 起因

近期使用 Lightroom 和 Illustrator 时，经常出现**Your Adobe app is not genuine**弹窗提示，影响使用。

尝试了各类 HOST 方案后，发现无法与 Clash 的 DNS 共存，故尝试使用本方案。本方法仅需配置 Clash 即可，无需配置 HOST 文件和防火墙。

> 该方案能有效屏蔽 Adobe 请求，但务必保证 Clash 是开机自启、日常后台。

![Adobe提示框](https://i.cuger.cn/b/4e0b96fd-0358-4878-8844-2a93dbd0da68.jpg)

# 方案

此前[通过 parser 配置 Clash 访问 ChatGPT](https://blog.cuger.cn/p/8c09/)，这里也是类似的方案：采用 Clash 的[parser](https://docs.cfw.lbyczf.com/contents/parser.html)配置，拒绝 Adobe 的请求。

## 打开配置

打开`Clash→Profiles→随便选一个配置文件→右键→点击Parsers`，如下图：

![](https://i.cuger.cn/b/f28b0c73-0928-4b9b-88fb-375ee145abe7.png)

## 配置参数

将下面的配置文件粘贴到 Parsers 配置筐中，如果有其他已有配置，记得手动合并。

配置方案如下：

```yaml
parsers: # array
  - reg: ^[\s\S]*$
    yaml:
      prepend-rules:
        - DOMAIN-SUFFIX,ic.adobe.io,REJECT
        - DOMAIN-SUFFIX,7sj9n87sls.adobe.io,REJECT
        - DOMAIN-SUFFIX,ij0gdyrfka.adobe.io,REJECT
        - DOMAIN-SUFFIX,apps.corel.com,REJECT
        - DOMAIN-SUFFIX,mc.corel.com,REJECT
        - DOMAIN-SUFFIX,origin-mc.corel.com,REJECT
        - DOMAIN-SUFFIX,iws.corel.com,REJECT
        - DOMAIN-SUFFIX,compute-1.amazonaws.com,REJECT
        - DOMAIN-SUFFIX,apps.corel.com,REJECT
        - DOMAIN-SUFFIX,mc.corel.com,REJECT
        - DOMAIN-SUFFIX,origin-mc.corel.com,REJECT
        - DOMAIN-SUFFIX,iws.corel.com,REJECT
        - DOMAIN-SUFFIX,apps.corel.com,REJECT
        - DOMAIN-SUFFIX,www.corel.com,REJECT
        - DOMAIN-SUFFIX,origin-mc.corel.com,REJECT
        - DOMAIN-SUFFIX,mc.corel.com,REJECT
        - DOMAIN-SUFFIX,apps.corel.com,REJECT
        - DOMAIN-SUFFIX,mc.corel.com,REJECT
        - DOMAIN-SUFFIX,origin-mc.corel.com,REJECT
        - DOMAIN-SUFFIX,iws.corel.com,REJECT
        - DOMAIN-SUFFIX,mc.corel.com,REJECT
        - DOMAIN-SUFFIX,content.corel.com,REJECT
        - DOMAIN-SUFFIX,65.200.22.154,REJECT
        - DOMAIN-SUFFIX,65.200.22.99,REJECT
        - DOMAIN-SUFFIX,ipp.corel.com,REJECT
        - DOMAIN-SUFFIX,secure.ipp.corel.com,REJECT
        - DOMAIN-SUFFIX,lm.licenses.adobe.com,REJECT
        - DOMAIN-SUFFIX,na2m-pr.licenses.adobe.com,REJECT
        - DOMAIN-SUFFIX,practivate.adobe.com,REJECT
        - DOMAIN-SUFFIX,activate.adobe.com,REJECT
        - DOMAIN-SUFFIX,ereg.adobe.com,REJECT
        - DOMAIN-SUFFIX,wip.adobe.com,REJECT
        - DOMAIN-SUFFIX,lmlicenses.wip4.adobe.com,REJECT
        - DOMAIN-SUFFIX,apps.corel.com,REJECT
        - DOMAIN-SUFFIX,mc.corel.com,REJECT
        - DOMAIN-SUFFIX,origin-mc.corel.com,REJECT
        - DOMAIN-SUFFIX,iws.corel.com,REJECT
        - DOMAIN-SUFFIX,na1r.services.adobe.com,REJECT
        - DOMAIN-SUFFIX,hlrcv.stage.adobe.com,REJECT
        - DOMAIN-SUFFIX,genuine.adobe.com,REJECT
        - DOMAIN-SUFFIX,prod.adobegenuine.com,REJECT
        - DOMAIN-SUFFIX,cc-api-data.adobe.io,REJECT
        - DOMAIN-SUFFIX,ims-prod06.adobelogin.com,REJECT
        - DOMAIN-SUFFIX,p13n.adobe.io,REJECT
        - DOMAIN-SUFFIX,crs.cr.adobe.com,REJECT
        - DOMAIN-SUFFIX,lcs-cops.adobe.io,REJECT
        - DOMAIN-SUFFIX,hbrt.adobe.com,REJECT
        - DOMAIN-SUFFIX,23ynjitwt5.adobe.io,REJECT
        - DOMAIN-SUFFIX,butler.adobe.com,REJECT
        - DOMAIN-SUFFIX,acp-ss-va6c2.adobe.io,REJECT
```

## 刷新

设置 Parsers 后，为保证其生效，记得点击配置文件的刷新按钮，确保生效。

![](https://i.cuger.cn/b/0a68724d-69bd-4509-b165-0f72cb92d3ca.png)
