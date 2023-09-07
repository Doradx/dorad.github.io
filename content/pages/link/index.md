---
created: 2023-06-06 04:51:00
description: 友情链接页面
comments: "true"
updated: 2023-09-07 13:21:00
date: 2023-06-05
slug: link
title: 友情链接
id: 750cea23-f2ce-4bfe-a1be-4c67c9ce1a5f
---

{% raw %}

<div class="links-content">
<div class="link-navigation"></div>
</div>
<link rel="stylesheet" href="/link/index.css">
<script data-pjax src="/link/index.js"></script>
{% endraw %}

## 读者墙

{% raw %}

<div id="waline-users"></div>

<script type="module" data-pjax>
import { UserList } from 'https://cdn.jsdelivr.net/npm/@waline/client/dist/waline.mjs';
UserList({
el: '#waline-users',
serverURL: 'https://pl.cuger.cn',
count: 30,
mode: 'wall',
});
</script>

{% endraw %}

## **欢迎大家互换友链 😊**

## **申请友链**

友链申请无需留言，[**点此自助申请**](https://github.com/Doradx/hexo-friendly-links/issues/new?assignees=&labels=&template=template_friend_new.yaml)即可，博主审核通过后便会同步到此页。

![友链填写模板](https://i.cuger.cn/b/4de7c502-076c-4edf-86cb-87ea1c3b4875.png)

## **我的友链**

信息如下：

```text
博客名称：遐说-Dorad
博客地址：https://blog.cuger.cn
博客图标：https://blog.cuger.cn/images/avatar.png
博客描述：❤编程❤摄影，期待走遍万水千山！
友链地址：https://blog.cuger.cn/link/
订阅地址：https://blog.cuger.cn/feed/
```

## **Tips:**

动态友链基于[Issues-Json Generator](https://github.com/xaoxuu/issues-json-generator)项目魔改生成，Hexo 渲染模板参考:

- [Hexo+Next 自定义友链界面 | McLsk888's Blog](https://mc-lsk888-blog.vercel.app/posts/%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/hexo-next%E8%87%AA%E5%AE%9A%E4%B9%89%E5%8F%8B%E9%93%BE%E7%95%8C%E9%9D%A2/)
- [Hexo 个人博客自定义友链页面](https://enfangzhong.github.io/2019/12/08/Hexo%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2%E8%87%AA%E5%AE%9A%E4%B9%89%E5%8F%8B%E9%93%BE%E9%A1%B5%E9%9D%A2/)
