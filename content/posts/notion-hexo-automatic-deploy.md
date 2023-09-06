---
abbrlink: 634642fd
categories:
  - 博客
  - Hexo
created: 2023-04-12 12:15:00
description: Notion+Hexo+Github Actions自动发布方案, 终于可以解放双手啦!（本文采用Notion撰写）
tags:
  - Notion
  - GitHub
  - Actions
  - Hexo
  - Node.js
status: 已发布
type: post
updated: 2023-09-04 10:02:00
date: 2023-04-12 21:00:00
filename: notion-hexo-automatic-deploy
title: Notion2Markdown联动发布Hexo博客-自动化部署方案
cover: https://i.cuger.cn/b/9ccd42f3-36d6-49de-a44c-5d70d910b65e.png
id: e58b8f82-70b8-49d0-9145-ca95ebf05091
---

<div style="margin:5px 1px;"> <a href="https://github.com/Doradx/notion2markdown-action" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/23170065?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">Doradx/notion2markdown-action</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">Doradx</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2023-04-12T02:04:29Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

# [Updates]

- 2023.09.02：更新适配`Notion`最新图片路径;；修复图片压缩`error`处理。
- 2023.06.05：添加对`synced_block`的支持，能够支持 Notion 中的块引用。
- 2023.04.21：添加对`audio`的支持，建议使用外部 MP3 源文件。
- 2023.04.20：添加`pic_compress`可选配置项，可配置为`true`开启图片自动压缩，默认为`false`。
- 2023.04.18：添加`Notion`一些特性支持，包括`bookmark`，`link_preview`，`video`，`pdf`和`embed`。
- 2023.04.17：添加`pic_base_url`可选配置项，可配置为自己图床的基础链接。图床上传过程中，如检测到此链接，将会自动查询要上传的图片是否已在图床（上传的文件名为 Notion 给图片赋予的`UUID`，据此检测）。此项可极大提高文章更新效率，节省宝贵的`GitHub Action`运行时间和`CDN`流量。

> 本项目受[`notion-blog-action`](https://github.com/mohuishou/notion-blog-actions)项目启发，fork 后深度修改而得，在此感谢[@Mo Huishou](https://github.com/mohuishou)。

# 概览

本方案主要是为了将 Notion 中的各种格式导出为 Markdown 格式，并在此基础上添加对 Notion 各类特性的支持，包括`bookmark`，`link_preview`，`video`，`pdf`和`embed`。符合原生 Markdown 格式的将转为纯 Markdown 语法，其它部分将转为 html 格式。[渲染效果](https://blog.cuger.cn/p/634642fd/#效果展示)

方案主要分为三部分：

- `Notion database`：创建写作, 进行稿件管理
- `notion2markdown-action`：GitHub Actions 将 notion 转为 Markdown，并将图片上传图床
- `GitHub Actions`: 编译部署 Hexo, 推送到 COS

# 实现原理

1. 采用`Notion API`，从`Notion`中同步`Dataset`中的`Pages`，并转换为`Markdown`，将其中的图片上传到图床中；
2. `Hexo/Huge`部署。
3. 以上均通过`Github Action`实现。

# 食用方法

## Notion 配置

1. 从[Blog - Template](https://www.notion.so/397943b2d0384e15ba69448900823984) 复制`Dataset`模板
2. 参考`Notion`官方教程[Create an integration (notion.com)](https://developers.notion.com/docs/create-a-notion-integration)，创建**Notion integration**
   应用，并获取**`Secrets`**，直达链接：[My integrations | Notion Developers](https://www.notion.so/my-integrations)
3. 将创建的`Dataset`数据库授权给刚创建的`Integration`应用，如下图：

![在Notion给Integration应用授权](https://i.cuger.cn/b/6d2f3047-beae-41a2-984e-be64b9ddc508.png)

## GitHub 配置

### workflows 配置

1. 切换到自己在 GitHub 上托管的仓库目录
2. 分别添加`notion_sync.yml`和`deploy.yml`

```yaml
name: Automatic sync pages from notion

on:
#   push:
#     branches: master
  workflow_dispatch:
  schedule:
    - cron: "5 */1 * * *"

permissions:
  contents: write

jobs:
  notionSyncTask:
    name: Ubuntu and node ${{ matrix.node_version }} and ${{ matrix.os }}
    runs-on: ubuntu-latest
    strategy:
      matrix:
        os: [ubuntu-latest]
        node_version: [16.x]
    outputs:
      HAS_CHANGES: ${{ steps.checkStep.outputs.HAS_CHANGES }}

    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Use Node.js ${{ matrix.node_version }}
        uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node_version }}
      - name: Convert notion to markdown
        uses: Doradx/notion2markdown-action@latest
        with:
          notion_secret: ${{ secrets.NOTION_TOKEN }} # NOTION授权码
          database_id: ${{ secrets.NOTION_DATABASE_ID }} # Dataset ID
          migrate_image: true
          picBedConfig: ${{ secrets.PICBED_CONFIG}} # picBed的配置，JSON格式，建议为minify JSON, 否则可能报错. 不同图床的配置可参考：https://picgo.github.io/PicGo-Core-Doc/zh/guide/config.html#picbed
          # 图床基础链接, 可留空。如填写，在图片上传图床前，会检查该图片是否已经上传过，如已上传则跳过，提升效率。
					pic_base_url: "" # 改成你的链接，例如你图床的图片链接为：https://i.blog.com/image/xxxx.jpg, 则此处填写https://i.blog.com/image/
					pic_compress: false # 是否开启图片压缩, 节约图床空间
					page_output_dir: 'source' # page 类文章的输出目录，例如about。
          post_output_dir: 'source/_posts/notion' # post 的输出目录，切记当clean_unpublished_post为true时，勿设置为 'source/_posts', 可能会删除你原目录下的文章！！！
          clean_unpublished_post: true # 是否清除未发表的文章，例如之前发表了，你又在notion中给移到草稿箱了.
      - name: Check if there is anything changed
        id: checkStep
        run: |
          if [[ -n "$(git status --porcelain)" ]]; then
            echo "HAS_CHANGES=true" >> $GITHUB_OUTPUT;
            echo "Updates available & redeployment required."
          else
            echo "HAS_CHANGES=false" >> $GITHUB_OUTPUT;
            echo "Nothing to commit & deploy."
          fi
      - name: Commit & Push
        uses: stefanzweifel/git-auto-commit-action@v4
        with:
          commit_message: Automatic sync from notion.
  callDepolyTask:
    name: Call the depoly workflow
    needs: notionSyncTask
    if: ${{ needs.notionSyncTask.outputs.HAS_CHANGES=='true' }}
    uses: Doradx/hexo-blog/.github/workflows/deploy.yml@master # 根据自身Github地址修改即可
```

```yaml
name: Automatic deployment of Dorad's Blog -> Tencent COS

on:
  push:
    branches: master
    paths:
      - "source/**"
      - "**.yml"
  workflow_dispatch:
  workflow_call:

env:
  GIT_USER: Dorad
  GIT_EMAIL: ddxid@outlook.com

jobs:
  build:
    name: Ubuntu and node ${{ matrix.node_version }} and ${{ matrix.os }}
    runs-on: ubuntu-latest
    strategy:
      matrix:
        os: [ubuntu-latest]
        node_version: [14.x]

    steps:
      - name: Checkout blog and theme
        uses: actions/checkout@v3
        with:
          submodules: "recursive"
      - name: Use Node.js ${{ matrix.node_version }}
        uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node_version }}
      - name: Install dependencies
        run: |
          git pull
          npm install
      - name: Depoly
        run: |
          npm run clean
          gulp
          npm run build
          npm run deploy
      - name: Commit & Push
        uses: stefanzweifel/git-auto-commit-action@v4
        with:
          commit_message: Automatic deployment.
```

### GitHub Action 环境变量配置

前往博客仓库的`settings/secrets/actions`中添加环境变量，核心为`NOTION_DATABASE_ID`, `NOTION_TOKEN`和`PICBED_CONFIG`。

![配置完成的GITHUB ACTION环境变量](https://i.cuger.cn/b/4d140b8a-51d3-4eb8-b25f-31935412639e.png)

其中，

- `NOTION_DATABASE_ID`：`Notion Dataset`的页面 ID，在`Notion Dataset`主页中点击`Copy Link`，得到链接，例如：[https://www.notion.so/doradx/397943b2d0384e15ba69448900823984?v=06762d5d3e2140e399c03d84131ee682](/397943b2d0384e15ba69448900823984?v=06762d5d3e2140e399c03d84131ee682)，其中`397943b2d0384e15ba69448900823984`便是此`Dataset`的 ID。
- `NOTION_TOKEN`：在此前获取的`Notion Integration`的**`Secrets`**，直达链接：[My integrations | Notion Developers](https://www.notion.so/my-integrations)
- `PICBED_CONFIG`：图床的配置文件，JSON 格式，由于图床使用的是[PicGo-Core](https://picgo.github.io/PicGo-Core-Doc/), 其配置保持相同，但只需要`picBed`部分，不同图床的配置方式详见：[配置文件 | PicGo-Core](https://picgo.github.io/PicGo-Core-Doc/zh/guide/config.html#%E6%89%8B%E5%8A%A8%E7%94%9F%E6%88%90)

以腾讯云 COS 为例，`PICBED_CONFIG`的格式为：

```json
{
    "uploader": "tcyun", // 代表当前的默认上传图床为,
    "tcyun":
    {
        "secretId": "",
        "secretKey": "",
        "bucket": "", // 存储桶名，v4 和 v5 版本不一样
        "appId": "",
        "area": "", // 存储区域，例如 ap-beijing-1
        "path": "", // 自定义存储路径，比如 img/
        "customUrl": "", // 自定义域名，注意要加 http://或者 https://
        "version": "v5" | "v4" // COS 版本，v4 或者 v5
    }
}
```

如需使用不同图床，直接修改`uploader`字段，并配置相应的参数即可。以下提供几种常见图床的配置文件案例：

- `qiniu`

```json
{
    "uploader": "qiniu", // 代表当前的默认上传图床为,
    "qiniu":
    {
        "accessKey": "",
        "secretKey": "",
        "bucket": "", // 存储空间名
        "url": "", // 自定义域名
        "area": "z0" | "z1" | "z2" | "na0" | "as0", // 存储区域编号
        "options": "", // 网址后缀，比如？imgslim
        "path": "" // 自定义存储路径，比如 img/
    }
}
```

- `aliyun`

```json
{
  "uploader": "aliyun", // 代表当前的默认上传图床,
  "aliyun": {
    "accessKeyId": "",
    "accessKeySecret": "",
    "bucket": "", // 存储空间名
    "area": "", // 存储区域代号
    "path": "", // 自定义存储路径
    "customUrl": "", // 自定义域名，注意要加 http://或者 https://
    "options": "" // 针对图片的一些后缀处理参数 PicGo 2.2.0+ PicGo-Core 1.4.0+
  }
}
```

- `github`

```json
{
  "uploader": "github", // 代表当前的默认上传图床,
  "github": {
    "repo": "", // 仓库名，格式是 username/reponame
    "token": "", // github token
    "path": "", // 自定义存储路径，比如 img/
    "customUrl": "", // 自定义域名，注意要加 http://或者 https://
    "branch": "" // 分支名，默认是 main
  }
}
```

## 测试效果

前往仓库的`Actions`页面，选择`Automatic sync pages from notion`，进行测试手动部署，并查看运行情况。

![手动触发，查看运行结果](https://i.cuger.cn/b/c826874f-4c03-44d8-91e8-94faa227476f.png)

搞定！尽情享受写作吧！

# 完整版配置文件及说明

[`notion2markdown`](https://github.com/Doradx/notion2markdown-action)提供了众多配置参数，以满足各类需求，以下为根据此 action 的配置文件，撰写的参数说明。

````yaml
name: "notion2markdown-action"
description: |
  将 notion database 中的 page 转换为 markdown 文档，可以用于 hexo、hugo 等静态博客构建, 内置picgo-core,使用picBed上传图床。
inputs:
  notion_secret: # id of input
    description: notion app token，建议最好放到 Action Secret 中
    required: true
  database_id:
    required: true
    description: |
      notion 中的数据库 id
      - 假设你的数据库页面链接是 `https://www.notion.so/you-name/0f3d856498ca4db3b457c5b4eeaxxxxx`
      - 那么 `database_id=0f3d856498ca4db3b457c5b4eeaxxxxx`
  status_name:
    description: notion database 状态字段的字段名，支持自定义
    default: "status"
  status_published:
    description: notion database 文章已发布状态的字段值
    default: "已发布"
  status_unpublish:
    description: |
      notion database 文章待发布状态的字段值
      触发 action 后会自动拉去所有该状态的文章，成功导出之后会把这篇文章的状态修改为上面设置的已发布状态
    default: "待发布"
  migrate_image:
    required: false
    description: |
      是否迁移图片到图床
      注意: 如果不迁移图片默认导出图片链接是 notion 的自带链接，有访问时效
      目前支持迁移图片到多类图床中，采用的是PicGO-Core.
    default: "true"
  picBedConfig:
    description: |
      picgo-core中picBed配置文件, 支持多类型图床。
      example:
      ```
      "current": "smms",
      "uploader": "smms", // 代表当前的默认上传图床为 SM.MS,
      "smms": {
        "token": "" // 从 https://sm.ms/home/apitoken 获取的 token
      }
      "aliyun":{
        "accessKeyId": "",
        "accessKeySecret": "",
        "bucket": "", // 存储空间名
        "area": "", // 存储区域代号
        "path": "", // 自定义存储路径
        "customUrl": "", // 自定义域名，注意要加 http://或者 https://
        "options": "" // 针对图片的一些后缀处理参数 PicGo 2.2.0+ PicGo-Core 1.4.0+
      },
      "tcyun":{
        "secretId": "",
        "secretKey": "",
        "bucket": "", // 存储桶名，v4 和 v5 版本不一样
        "appId": "",
        "area": "", // 存储区域，例如 ap-beijing-1
        "path": "", // 自定义存储路径，比如 img/
        "customUrl": "", // 自定义域名，注意要加 http://或者 https://
        "version": "v5" | "v4" // COS 版本，v4 或者 v5
      }
      ```
      详见: https://picgo.github.io/PicGo-Core-Doc/zh/guide/config.html#%E6%89%8B%E5%8A%A8%E7%94%9F%E6%88%90
    default: "{}"
  pic_base_url:
    description: |
      图床的基础链接, 例如: https://i.blog.com/image/，如填写此链接，在图片上传图床前，会检查该图片是否已经上传过，如已上传则跳过，提升效率。
    default: ""
  pic_compress:
    description: |
      是否开启图片压缩？true为开启，默认不开启
    default: ""
  page_output_dir:
    description: page类型页面的输出文件夹
    default: "source/"
  post_output_dir:
    description: post类型页面的输出文件夹
    default: "source/_posts/notion"
  clean_unpublished_post:
    description: 是否清除未发表的post
    default: "false"
  timezone:
    description: 设置的时区
    default: "Asia/Shanghai"
````

# Notion 文章属性说明

## 属性列表

`Nation Dataset`中，每篇文章都预设了属性字段，字段说明如下：

- `status`: 文章状态
- `type`:页面类型，`post/page`, 分别对应 hexo 中的`page`和`post`, 留空则默认为`post`
- `date`: 发表日期
- `categories`: 分类
- `tags`: 标签
- `filename`: `Markdown`文件最终的文件名，可留空，默认为文章的标题
- `description`: 文章简介
- `abbrlink`: 静态文章链接, 此项需搭配[**hexo-abbrlink**](https://github.com/rozbo/hexo-abbrlink)使用，如果你不知道该属性的意义，可留空
- `Created time`:　创建时间，此属性自动更新，将会被同步到`*.md`文件的 cre`ated`属性中
- `Last edit time`：最后修改时间，此属性自动更新，将会被同步到`*.md`文件的`updated`属性中

## Tips

- 只有状态为`待发布`的文章才会被`Github Action`转为`Markdown`
- `Notion`上设置的`文章封面`会被用作文章的`cover`字段，并上传图床
- `Notion`中每个页面会有一个独一无二的 UID, 为方便管理，此 ID 会被同步到`*.md`文件的`id`属性
- `Notion`中每个页面会有`created_time`和`last_edited_time`, 会被分别同步到`*.md`文件的`created`和`updated`属性
- `Notion Dataset`中，使用`status`进行阶段管理，其中只有处于`待发布`状态的文章会被自动处理。所以，只需要保证`待发布`和`已发布`两个状态存在即可，其它几个状态可以根据喜好修改或删除；
- `Notion Dataset`中，每篇文章都设置了众多属性，其均会写入到最终`Markdown`文件头部的 YAML 配置中，可根据自身需要添加属性，但注意字段名最好不要有特殊字符，否则可能出错；
- 使用`hexo`的童鞋，如**部署过慢**，建议升级`hexo`版本，并**清理项目依赖**（在`package.json`中），可极大提升部署效率。博主升级后时间缩短了一半，目前约`90s内`能完成部署。

## Actions 耗时分析

### notion_sync.yml

对于此任务，最耗时的部分在于图床上传，具体耗时与图片数量和`GitHub Actions`的具体执行机器有关（每次机器都不一样）。

由于是每小时轮询，当查到 Notion 无需要发布的文献时候

> 本文处理耗时约`17s`，各任务为并行，取决于执行机器网速和图片数量。此步骤主要瓶颈在于 GitHub 上传图床速度，可优化面较小。。。或许用 GitHub 做图床会非常快？利好图床采用外网平台的童鞋。

### deploy.yml

此任务最大耗时在依赖安装(`Install dependencies`)和部署(`Deploy`)：

- 升级`Hexo`到最新版`v6.3.0`，并清理`package.json`中无用的包后，依赖安装约耗时`20s`
- 部署部分主要还是网络问题，速度取决于你的部署类型，博主使用腾讯云 COS，单次部署上传约`30s`

> 单次部署的典型耗时约`1min`

# 渲染效果展示

Notion 页面：

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.notion.so/doradx/notion2markdown-action-e9053491ccb74c219c8674e873883d96?pvs=4"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">Notion – The all-in-one workspace for your notes, tasks, wikis, and databases.</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">A new tool that blends your everyday work apps into one. It's the all-in-one workspace for you and your team</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.notion.so/images/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.notion.so/doradx/notion2markdown-action-e9053491ccb74c219c8674e873883d96?pvs=4</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://www.notion.so/images/meta/default.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

博客渲染页面：

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://blog.cuger.cn/p/ca96"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">blog.cuger.cn</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://blog.cuger.cn/p/ca96</div></div></div></a></div></div>

# Q&A

- 如何更新`已发布`的文章？

撰写修改后，将文章状态修改为`待发布`即可，会自动更新。

- 如何删除`已发布`的文章？

直接将文章状态修改为`正在写`/`计划中`，或其它任何不是`已发布`/`待发布`的状态即可。

> 注意：需要`notion_sync.yml`中配置`clean_unpublished_post: true`

- 更新`已发布`的文章，如何保证文章链接不变？

方案 1（手动）：给`Notion`的文章手动设置`abbrlink`，会同步到`Markdown`文件中

方案 2（自动）：采用[rozbo/hexo-abbrlink](https://github.com/rozbo/hexo-abbrlink)插件的童鞋，`Notion`文章的 abbrlink 留空即可，会自动处理；当然如果想自定义`abbrlink`，直接填写即可

> [rozbo/hexo-abbrlink](https://github.com/rozbo/hexo-abbrlink)会在`Deploy`阶段自动给文章生成`abbrlink`，当将已发布文章修改后重新发布时，会读取原 Markfown 文件中的`abbrlink`并同步到 Notion 文章。

- 如何修改同步频次？

在`notion_sync.yml`配置中修改 `schedule`配置即可，格式为 cron，可利用[Crontab.guru](https://crontab.guru/#5_*/1_*_*_*)进行可视化调整。

> 注意：不要改那么高频！GitHub 对于私有仓库，调用 GitHub Actions 的时间是有限的，Pro 用户每个月 3000 分钟。小心 GitHub 找你收钱。根据推算，建议触发间隔不小于 10 分钟！

- 如何嵌入 HTML 等代码？

在`Notion`中直接粘贴即可，需要**确保在粘贴过程中 Notion 没有给你的 URL 链接自动加上超链接**，否则可能渲染出错，例如：

```html
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/r7iLI8vW4bE"
  title="YouTube video player"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  allowfullscreen
></iframe>
```

复制后直接粘贴到 Notion 的文章，它会自动给 URL 加上超链接：

```html
<iframe
  width="560"
  height="315"
  src="[https://www.youtube.com/embed/r7iLI8vW4bE](https://www.youtube.com/embed/r7iLI8vW4bE)
"
  title="YouTube video player"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  allowfullscreen
></iframe>
```

会导致最终的`Markdown`渲染出错，出现以下情况：

![](https://i.cuger.cn/b/849e1ea2-0bc7-47d6-a94d-df4daf93f0a8.png)

- 什么图片会被上传到图床？

为节省空间，本插件只将 Notion 存储的图片转到图床中，外链图片和原本就属于自己图床的图片链接不会被上传。

> 注意：插入外链图片时请检查是否允许跨域，否则可能图片不显示。

# 总结

## 优势

- 功能完备，虽然有一些小坑，但`Notion`转`Markdown`功能完备
- 自动化部署，只需要在`Notion`编辑即可，且方便管理，剩余流程全自动
- 利用`Notion`可在多端同步编辑，图床自动上传，无需关心其它问题，转注写作即可
- 理论上支持各类静态博客，因为原理就是`Notion to Markdown`，通用型极高
- 可设置指定的目录存储 Notion 导出的 post, 例如: `source/_posts/notion`,不影响原先使用其它编辑器撰写的文章
- 多处备份，`Notion+GitHub`,暂不用担心数据丢失

## 不足

- `Notion`的有些特性，`Markdown`可能不支持，所以写作时的结果和发表后的结果可能有差异。

> 例如如何嵌入`HTML`代码…添加`Bilibili/YouTube/163`等视频或音乐`iframe`媒体文件，`Markdown`导入`Notion`时，`Notion`给转成了`embed`类型，再导出`Markdown`的时候就全成链接了！！！麻了。。。解决方案也很简单，将`iframe`代码直接复制粘贴到`Notion`中粘贴为纯文本即可，记得检查`Notion`是否把链接给转成了引用。

- 目前是采用`GitHub Actions Schedule` 定时触发，从`Notion`同步数据，但`GitHub`的**`schedule`**并不是总准时，而且还有可能跳票，详见：[Events that trigger workflows - GitHub Docs](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule)

> Note: The `schedule`event can be delayed during periods of high loads of GitHub Actions workflow runs. High load times include the start of every hour. If the load is sufficiently high enough, some queued jobs may be dropped. To decrease the chance of delay, schedule your workflow to run at a different time of the hour.

- 后期可考虑换为`Webhook`(更及时、节省资源) - 已支持，详情见：

<div style="margin:5px 1px;"> <a href="https://github.com/Doradx/notion2markdown-vercel" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/23170065?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">Doradx/notion2markdown-vercel</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">Doradx</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2023-04-18T02:53:33Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

> 特别鸣谢[@王云子](https://wangyunzi.com/)同学协助`debug`并完善此项目。

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://wangyunzi.com/posts/notion/64/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">wangyunzi.com</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://wangyunzi.com/posts/notion/64/</div></div></div></a></div></div>

# 后记

> 为了折腾自动化部署，fork 了`notion-blog-action`后，捣鼓了半天，重写 debug…已麻…近期肯定是不想再折腾了 😂

## notion2markdown-vercel

由于前面配置的`GitHub Actions`通过`crontab`控制部署间隔，或手动调用。

当我想要提高部署的实时性时，面临以下几个问题：

- 将定时任务间隔缩小：会大量消耗 GitHub Actions 的时间（每个月每个账号 3000 分钟）
- 打开`GitHub`手动触发`GitHub Actions`：既繁琐又慢，我可不想在每次写完文章又打开 GitHub 一通乱点。

要么实时性较差，要么操作复杂。故为了方便博客同步，我采用`Webhook`触发`GitHub Actions`, 触发`Notion同步`和`Hexo部署`。

### 方案概览

部署后的工作流为：

- 人工同步（实时性强，我最常用）：每次写完 or 更新文章，点击 Notion 上的超链接，部署博客，等待约`2分钟`即可；

  ![](https://i.cuger.cn/b/430a605e-3061-4134-a1d8-4693a56bc7b2.png)

- 自动同步（懒惰版）：在树莓派部署了`cron`任务，每两分钟检查是否有文章需要同步，若有，直接触发 GitHub Action，发布约需`5分钟`；

总的来说，部署不算快捷，但省事，手机端&电脑端都可以写作，写完将博文调为[待发布]状态即可。

### 快速部署

点击下方按钮即可部署到 Vercel！

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FDoradx%2Fnotion2markdown-vercel&env=GITHUB_REPO,GITHUB_USERNAME,GITHUB_TOKEN,NOTION_DATABASE_ID,NOTION_TOKEN&project-name=notion2markdown-vercel&repository-name=notion2markdown-vercel&demo-title=notion2markdown-vercel - Dorad&demo-description=The instance used by Dorad&demo-url=https%3A%2F%2Fnotion2markdown-vercel.vercel.app%2F)

部署过程中需要填写以下环境变量：

![环境变量列表](https://i.cuger.cn/b/9dd0b5f6-481c-4915-9afe-474d2e8e10db.png)

- GITHUB_REPO: 你的博客代码仓库
- GITHUB_USERNAME: GGitHub 用户名
- GITHUB_TOKEN：GitHub 的 Token，很多人的博客是私有仓库
- NOTION_DATABASE_ID：前面已经使用过的 Notion 数据库 ID
- NOTION_TOKEN：前面已经使用过的 Notion 认证 Token

配置完成后，访问主页即可看到两个同步超链接，如：[notion2markdown-vercel.vercel.app](https://notion2markdown-vercel.vercel.app/)

![实例页面，Actions即为目前支持的动作](https://i.cuger.cn/b/d0d18ec7-744d-4d36-9827-b5cce3bc16df.png)

将其链接复制后，配置到 Notion 主页面的描述栏，即可实现博主的效果。

![](https://i.cuger.cn/b/93d6915c-bfe3-4772-815d-2f98611224b5.png)

博客更大的意义在于记录，而不是折腾各种工具。

目前对于这套流程较为满意，希望能加油产出内容！

# 主要参考

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://github.com/mohuishou/notion-blog-actions"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">GitHub - mohuishou/notion-blog-actions: convert notion database pages to markdown files for hexo or hugo</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">convert notion database pages to markdown files for hexo or hugo - GitHub - mohuishou/notion-blog-actions: convert notion database pages to markdown files for hexo or hugo</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://github.githubassets.com/favicons/favicon.svg"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://github.com/mohuishou/notion-blog-actions</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://opengraph.githubassets.com/f0bc7a08d7486ffd155f9eee69a1ce843254e0616687984573dbf312ef41566f/mohuishou/notion-blog-actions" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://lailin.xyz/post/notion-markdown-blog.html"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">使用 Notion Database 管理静态博客文章</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">当博客文章变多了之后就发现，放在 hexo 的本地文件夹中管理就有些力不从心了</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://lailin.xyz/icons/favicon-32x32.png"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://lailin.xyz/post/notion-markdown-blog.html</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://img-lailin-xyz.oss-cn-hangzhou.aliyuncs.com/image/4822d5f97a1c93d47bf2921789a3a730.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://sanonz.github.io/2020/deploy-a-hexo-blog-from-github-actions/#Workflow-模版"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">利用 Github Actions 自动部署 Hexo 博客 | Sanonz</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">介绍Github Actions 可以很方便实现 CI/CD 工作流，类似 Travis 的用法，来帮我们完成一些工作，比如实现自动化测试、打包、部署等操作。当我们运行 Jobs 时，它会创建一个容器 (runner)，容器支持：Ubuntu、Windows 和 MacOS 等系统，在容器中我们可以安装软件，利用安装的软件帮我们处理一些数据，然后把处理好的数据推送到某个地方。本文将介绍利用 Github Actions 实现自动部署 hexo 到 Github Pages，在之前我们需要写完文章</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://sanonz.github.io/images/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://sanonz.github.io/2020/deploy-a-hexo-blog-from-github-actions/#Workflow-模版</div></div></div></a></div></div>
