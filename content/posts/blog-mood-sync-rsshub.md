---
abbrlink: a809
categories:
  - 博客
created: 2023-07-07 22:37:00
tags:
  - Hexo
  - Blog
  - RSShub
updated: 2023-09-07 11:03:00
date: 2023-07-07
slug: blog-mood-sync-rsshub
title: 微博/Twitter同步到博客瞬间方案-RSSHub
id: d157d5fb-2281-4103-b8bf-43072159fd38
---

# 起因

看到不少博客会有“瞬间”页面，一般用来发送简短的心情，类似于说说，例如[瞬间 - 长街短梦](https://wangyunzi.com/memos)

。故也想倒腾一个。

但 Hexo 是静态博客，所以我准备将 Twitter 上的内容直接同步过来。

# 操作流程(简洁版)

## 1. RSSHub 链接生成

打开[RSSHub 网站](https://docs.rsshub.app/social-media.html)，找到你需要的数据源类型，并定制化你的 URL，在 URL 末尾添加`.json`，指定返回数据为 JSON 格式。例如：https://rsshub.app/twitter/user/_Dorad.json

## 2. 创建新页面

首先使用 Hexo 命令创建新页面

```shell
hexo new page mood
```

打开页面 md 文件，添加以下内容（按需修改）：

```html
---
title: 瞬间
comments: "false"
date: 2023-07-06 15:53:58
---

<div class="mood-container"></div>

<script src="https://cdn.jsdelivr.net/npm/dayjs@1.10.6/dayjs.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/dayjs@1/plugin/relativeTime.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/dayjs@1/locale/zh-cn.min.js"></script>
<link rel="stylesheet" href="/mood/index.css" />
<script data-pjax src="/mood/index.js"></script>
```

在 mood 文件夹下，新建 index.js 和 index.css 文件，分别存放 js 代码和 css 样式，内容如下：

```javascript
dayjs.extend(window.dayjs_plugin_relativeTime);
dayjs.locale("zh-cn");

function loadMood() {
  fetch("/mood/mood.json")
    .then((res) => res.json())
    .then((data) => {
      console.log(data);
      data["items"].forEach((post) => {
        const moodPostDiv = document.createElement("div");
        moodPostDiv.classList.add("mood-post");
        moodPostDiv.innerHTML = `
                    <div class="mood-avatar-container"><img class="mood-avatar"
                        src="${data.icon}">
                    </div>
                    <div class="mood-right">
                        <div class="mood-title">
                            <div class="mood-nickname"><a href="${post.url}"
                                    target="_blank">${
                                      post.authors[0]?.name
                                    }</a></div>
                            <div class="mood-time">${dayjs(
                              post.date_published
                            ).fromNow()}</div>
                        </div>
                        <div class="mood-dotted-line"></div>
                        <div class="mood-content">${post.content_html}</div>
                    </div>
                `;
        document.querySelector(".mood-container").appendChild(moodPostDiv);
      });
    });
}

window.onload = loadMood();
```

```css
.mood-container {
  margin: 0 auto;
}

.mood-post {
  display: flex;
  margin-bottom: 10px;
  padding: 4px;
  border-radius: 1rem;
  background-color: var(--global-bg);
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
}

.mood-avatar-container {
  width: 4rem;
  margin-top: 3px;
  margin-right: 0.5rem;
  display: inline-block;
  vertical-align: middle;
}

.mood-avatar {
  overflow: hidden;
  width: 5em;
  border-radius: 50%;
}

.mood-right {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 3px;
}

.mood-title {
  display: grid;
  grid-template-columns: auto auto;
  align-items: left, center;
}

.mood-nickname {
  font-weight: bold;
  text-align: left;
}

.mood-time {
  color: var(--font-color);
  margin-right: 0.3rem;
  text-align: right;
}

.mood-content {
  margin-top: 3px;
  color: var(--font-color);
  flex: 1;
}

.mood-dotted-line {
  height: 1px;
  background-image: linear-gradient(
    to right,
    #d9d9d9 50%,
    #d9d9d9 50%,
    transparent 0%
  );
  background-size: 10px 1px;
  background-repeat: repeat-x;
}
```

## 3. JSON 缓存

采用 shell 或者 bash，在部署的时候自动将`JSON`缓存到本地文件。

```shell
curl https://rsshub.app/twitter/user/_Dorad.json -o ./source/mood/mood.json
```

由于我是采用 GitHub Action 进行自动化部署，所以我将上面的代码加入到了 GitHub Action 工作流，并设置每小时同步一次~

以下是我使用的案例：

```bash
name: Automatic sync links

on:
 workflow_dispatch:
 schedule:
   - cron: '0 2-17/1 * * *'

jobs:
 syncLinks:
  name: Ubuntu and node ${{ matrix.node_version }} and ${{ matrix.os }}
  runs-on: ubuntu-latest
  strategy:
   matrix:
    os: [ubuntu-latest]
    node_version: [18.x]
  outputs:
   HAS_CHANGES: ${{ steps.changes.outputs.HAS_CHANGES }}
  steps:
   - name: Checkout
     uses: actions/checkout@v3
   - name: Featch the friendly link & mood link
     run: |
      mood_str=$(curl https://rsshub.app/twitter/user/_Dorad.json)
      if [[ $mood_str =~ "^(\{.*\}|\[.*\])$" ]]; then
        echo "mood_str is not vaild json file"
      else
        echo $mood_str > source/mood/mood.json
      fi
   - name: Check if there is anything changed in source dir
     id: changes
     run: |
        if [[ -n "$(git status --porcelain)" ]]; then
        echo "HAS_CHANGES=true" >> $GITHUB_OUTPUT;
        echo "Updates available & redeployment required."
        else
        echo "HAS_CHANGES=false" >> $GITHUB_OUTPUT;
        echo "Nothing to commit & deploy."
        fi
   - name: Commit & Push
     if: steps.changes.outputs.HAS_CHANGES == 'true'
     uses: stefanzweifel/git-auto-commit-action@v4
     with:
      file_pattern: 'source/'
      commit_message: link sync.
```

## 4. 网站部署&效果展示

由于我采用的 GitHub Action 自动化部署，所以配置完基本不用管。

如果是手动部署的小伙伴，推荐使用以下自用脚本：

```css
curl https://rsshub.app/twitter/user/_Dorad.json -o ./source/mood/mood.json
hexo c& hexo g & hexo d
```

根据自己的情况，修改 URL 和 JSON 存储路径即可，部署时执行`./deploy.bat`即可一键同步部署。

# 方案分析

由于 Twitter API 比较难搞，而我又经常用 RSS，理所当然的想到了[RSSHub](https://docs.rsshub.app/social-media.html#_755)项目，几乎能订阅一切，哈哈哈哈 😂 故本方案基于[RSSHub](https://docs.rsshub.app/social-media.html#_755)项目的订阅而生。

## 数据流

1. RSSHub 订阅某数据源，例如微博、Twitter、小红书、Telegram、抖音、豆瓣、知乎、B 站.etc
2. 部署的时候通过命令行，将 Feed 同步到本地，保存为 JSON 文件
3. 博客“瞬间”页面加载时，读取 JSON，并渲染页面

## 优点

- 兼容性极强：基于 RSSHub 通用 JSON 格式，可用于微博、Twitter、小红书、Telegram、抖音、豆瓣、知乎、B 站、酷安等等等一众数据源，详情参考[RSSHub 官方文档](https://docs.rsshub.app/social-media.html#ku-an)
- 配置相对简单，迁移博客也方便
- 有 JSON 缓存，响应更快，无墙烦恼（相对于直接请求方案）

## 缺点

- 同步相对缓慢：首先 RSSHub 有缓存，更新不是那么及时，其次手动部署方案更加不及时，所以推荐使用 GitHub Action 自动化部署方案的同学使用。[GitHub Action 自动化部署 Hexo 参考博文](https://blog.cuger.cn/p/634642fd/#workflows-%E9%85%8D%E7%BD%AE)
- RSSHub 提供的信息不一定全面：像是 Twitter、知乎、微博等防爬严重的数据源，基本都是只能抓取 20 条最新条目。
- 反爬严重：如上所述，很多网站反爬严重，需要私有化部署 RSSHub 才能抓取。

# 参考

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://docs.rsshub.app/social-media.html#dou-ban"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;"></div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://docs.rsshub.app/social-media.html#dou-ban</div></div></div></a></div></div>
