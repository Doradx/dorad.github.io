---
created: 2023-09-07 15:45:00
categories:
  - GitHub
  - GitHub Action
  - Notion
tags:
  - Notion
updated: 2023-09-07 16:08:00
date: 2023-09-07
slug: notion2markdown-action-doc
title: "[Docs]Notion2markdown-action"
id: 4f72d1f5-b254-498c-b012-6f2466e6c35a
---

Previously, we developed the [notion2markdown-action](https://github.com/Doradx/notion2markdown-action) plugin, which allows you to synchronize pages from Notion to your blog using GitHub Actions. The old tutorial is available [here](https://blog.cuger.cn/p/634642fd/).

# **Features**

As the name suggests, by using this plugin in GitHub Actions, you can sync pages from Notion to your GitHub repository, typically used for publishing static blogs.

Key features include:

- Comprehensive Notion to Markdown conversion: Built on the [notion-to-md](https://github.com/souvikinator/notion-to-md) project, it supports various types of Notion blocks.
- YAML metadata: Supports converting Notion page properties into YAML metadata in Markdown.
- PicGo image hosting: Supports uploading images from Notion to various image hosting services supported by PicGo, including smms, qiniu, upyun, tcyun, GitHub, aliyun, imgur, and more.

# **Usage**

Simply use this plugin in the workflow of your GitHub Actions. A minimal code snippet is as follows:

```text
- name: Convert notion to markdown
  uses: Doradx/notion2markdown-action@v1
  with:
    notion_secret: ${{ secrets.NOTION_TOKEN }}
    database_id: ${{ secrets.NOTION_DATABASE_ID }}
```

Using this action will convert Notion pages into Markdown files.

## **Parameters**

Parameter details are defined in the [action.yml](https://github.com/Doradx/notion2markdown-action/blob/main/action.yml) configuration file. Here is an explanation and usage of each parameter.

### **Basic Parameters**

| **Name**               | **Required** | **Default Value**     | **Description**                                                                                                                                                                                                                                                                                        | **Example**                       |
| ---------------------- | ------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------- |
| notion_secret          | Yes          | N/A                   | Notion Secret, it's recommended to store it in GitHub Actions Secrets. Obtain it from: [https://www.notion.so/help/create-integrations-with-the-notion-api](https://www.notion.so/help/create-integrations-with-the-notion-api)                                                                        | ${{ secrets.NOTION_SECRET }}      |
| database_id            | Yes          | N/A                   | Notion Database ID, assuming your database page URL is [https://www.notion.so/username/0f3d856498ca4db3b457c5b4eeaxxxx?v=xxxx](https://www.notion.so/username/0f3d856498ca4db3b457c5b4eeaxxxx?v=xxxx), then 0f3d856498ca4db3b457c5b4eeaxxxx is your database ID                                        | ${{ secrets.NOTION_DATABASE_ID }} |
| status_name            | No           | status                | The field name in the Notion database used to distinguish page status. Customizable.                                                                                                                                                                                                                   | status                            |
| status_published       | No           | Published             | The field value in the Notion database indicating a published article.                                                                                                                                                                                                                                 | Published                         |
| page_output_dir        | No           | source/               | Save pages with type 'page' from Notion to the page_output_dir in GitHub.                                                                                                                                                                                                                              | source/                           |
| post_output_dir        | No           | source/\_posts/notion | Save pages with type 'page' from Notion to the post_output_dir in GitHub.                                                                                                                                                                                                                              | source/\_posts/notion             |
| clean_unpublished_post | No           | false                 | Enable article deletion, which means if the status in Notion changes from 'Published' to something else, the article is removed from GitHub. It is recommended to enable, but make sure that only Notion-synchronized articles exist in post_output_dir!!! Otherwise, it may delete existing articles. | true                              |
| metas_keeped           | No           | abbrlink              | During article synchronization, the Markdown metadata fields to keep and synchronize to Notion page properties. Use commas to separate multiple values, e.g., abbrlink, date                                                                                                                           | abbrlink, date                    |
| metas_excluded         | No           | ptype, pstatus        | Notion page properties to be removed from Markdown during article synchronization.                                                                                                                                                                                                                     | ptype, pstatus                    |
| last_sync_datetime     | No           | N/A                   | The last time the Notion database was synchronized, used for incremental synchronization. Make sure it is in a format that moment.js can parse. Suggested to use the commit time of the latest Notion synchronization in Git, e.g., git log -n 1 --grep="NotionSync" --format="%aI"                    | 2023-09-04T17:21:33+00:00         |
| timezone               | No           | Asia/Shanghai         | Time zone. Converts ISO time in Notion page properties to local time in the specified timezone.                                                                                                                                                                                                        | Asia/Shanghai                     |

Among the basic parameters, `notion_secret` and `database_id` are sensitive, so it's recommended to store them in GitHub Actions Secrets. Instructions for setting them up can be found [here](https://docs.github.com/zh/actions/security-guides/using-secrets-in-github-actions).

Other parameters can be configured as described.

### **Image Hosting Parameters**

| **Name**       | **Required** | **Default Value** | **Description**                                                                                                                                                                                                                                                                 | **Example** |
| -------------- | ------------ | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| pic_migrate    | No           | false             | Whether to migrate images to an image hosting service. Note: If images are not migrated, the default image links from Notion with a one-hour time limit will be used.                                                                                                           | true        |
| pic_bed_config | No           | {}                | When using an image hosting service, configure the picBed section of PicGo-Core. Supports multiple types of image hosting services. Detailed information can be found [here](https://picgo.github.io/PicGo-Core-Doc/zh/guide/config.html#%E6%89%8B%E5%8A%A8%E7%94%9F%E6%88%90). | See below   |
| pic_compress   | No           | false             | Whether to compress images before uploading them to the image hosting service.                                                                                                                                                                                                  | true        |

In the image hosting parameters, `pic_bed_config` and `pic_base_url` configurations are critical.

Here are example configurations for Tencent Cloud (Tencent Cloud Object Storage - COS), Alibaba Cloud (Aliyun OSS), and GitHub as image hosting services:

Tencent Cloud (COS) Example:

```text
{
    "uploader": "tcyun",
    "tcyun":
    {
        "secretId": "",
        "secretKey": "",
        "bucket": "",
        "appId": "",
        "area": "",
        "path": "",
        "customUrl": "",
        "version": "v5" | "v4"
    }
}
```

Alibaba Cloud (Aliyun OSS) Example:

```text
{
    "uploader": "aliyun",
    "aliyun":
    {
        "accessKeyId": "",
        "accessKeySecret": "",
        "bucket": "",
        "area": "",
        "path": "",
        "customUrl": "",
        "options": ""
    }
}
```

GitHub Example:

```text
{
    "uploader": "github",
    "github":
    {
        "repo": "",
        "token": "",
        "path": "",
        "customUrl": "",
        "branch": ""
    }
}
```

## **Output**

After

the GitHub Actions execution, you will receive an output that reports the number of updated pages.

| **Field**     | **Type** | **Description**         |
| ------------- | -------- | ----------------------- |
| updated_count | Text     | Number of updated pages |

To retrieve the number of updated pages in your workflow, you can use `steps.{step_id}.outputs.updated_count`.

# **Examples**

Below, we provide several example templates for quick deployment.

First, you need to configure GitHub Actions Secrets for your GitHub repository. Go to `Settings → Secrets and variables → Actions → New repository secret` and add the following three crucial configuration parameters:

- `NOTION_SECRET`: Notion integration authorization SECRET. Obtain it from: [Create integrations with the Notion API – Notion Help Center](https://www.notion.so/help/create-integrations-with-the-notion-api)
- `NOTION_DATABASE_ID`: Notion Database ID. Copy your Database link, e.g., `https://www.notion.so/username/{database_id}?v={view_id}`, where `database_id` is your database ID.
- `PICBED_CONFIG`: If you want to upload images to an image hosting service, please configure this parameter. It should be in JSON format as described above.

## **[Example 1] Notion2hexo**

This is a template for deploying Notion to hexo. Simply copy and paste it into the `.github/workflows/notion2hexo.yml` file in your repository.

> Remember to configure GitHub Actions Secrets beforehand.

```text
name: Notion2Hexo
on:
  workflow_dispatch:
  schedule:
   - cron: '*/30 1-17/1 * * *'
permissions:
  contents: write
jobs:
  notionSyncTask:
    name: Notion2hexo on ubuntu-latest
    runs-on: ubuntu-latest
    steps:
      - name: Checkout blog and theme
        uses: actions/checkout@v3
        with:
          submodules: 'recursive'
          fetch-depth: 0
      - name: Check the NOTION_SYNC_DATETIME
        id: GetNotionSyncDatetime
        run: |
          NOTION_SYNC_DATETIME=$(git log -n 1 --grep="NotionSync" --format="%aI")
          echo "NOTION_SYNC_DATETIME=$NOTION_SYNC_DATETIME" >> "$GITHUB_OUTPUT"
          echo -e "Latest notion sync datetime:\n$NOTION_SYNC_DATETIME"
      - name: Convert notion to markdown
        id: NotionSync
        uses: Doradx/notion2markdown-action@v1
        with:
          notion_secret: ${{ secrets.NOTION_TOKEN }}
          database_id: ${{ secrets.NOTION_DATABASE_ID }}
          pic_migrate: true
          pic_bed_config: ${{ secrets.PICBED_CONFIG }}
          pic_compress: true
          output_page_dir: 'source'
          output_post_dir: 'source/_posts/notion'
          clean_unpublished_post: true
          metas_keeped: abbrlink
					metas_excluded: pstatus,ptype
          last_sync_datetime: ${{ steps.GetNotionSyncDatetime.outputs.NOTION_SYNC_DATETIME }}
      - name: Hexo deploy
        if: steps.NotionSync.outputs.updated_count != '0'
        run: |
          git pull
          npm install && npm run deploy
      - name: Commit & Push
        if: steps.NotionSync.outputs.updated_count != '0'
        uses: stefanzweifel/git-auto-commit-action@v4
        with:
          file_pattern: 'source/'
          commit_message: Automatic NotionSync.
```

## **[Example 2] Notion2hugo**

Here is a template for deploying Notion to Hugo:

```text
name: Notion2Hugo
on:
  workflow_dispatch:
  schedule:
    - cron: '*/30 1-17/1 * * *'
permissions:
  contents: write
  pages: write
  id-token: write
jobs:
  notionSyncTask:
    name: Notion2Hugo on ubuntu-latest
    runs-on: ubuntu-latest
    outputs:
      HAS_CHANGES: ${{ steps.NotionSync.outputs.updated_count !='0' }}
    steps:
      - name: Checkout blog and theme
        uses: actions/checkout@v3
        with:
          submodules: 'recursive'
          fetch-depth: 0
      - name: Check the NOTION_SYNC_DATETIME
        id: GetNotionSyncDatetime
        run: |
          NOTION_SYNC_DATETIME=$(git log -n 1 --grep="NotionSync" --format="%aI")
          echo "NOTION_SYNC_DATETIME=$NOTION_SYNC_DATETIME" >> "$GITHUB_OUTPUT"
          echo -e "Latest notion sync datetime:\n$NOTION_SYNC_DATETIME"
      - name: Convert notion to markdown
        id: NotionSync
        uses: Doradx/notion2markdown-action@v1
        with:
          notion_secret: ${{ secrets.NOTION_SECRET }}
          database_id: ${{ secrets.NOTION_DATABASE_ID }}
          pic_migrate: true
          pic_bed_config: ${{ secrets.PICBED_CONFIG }}
          pic_compress: true
          output_page_dir: 'content/pages'
          output_post_dir: 'content/posts'
          clean_unpublished_post: true
          metas_keeped: slug
          metas_excluded: pstatus, ptype
          last_sync_datetime: ${{ steps.GetNotionSyncDatetime.outputs.NOTION_SYNC_DATETIME }}
      - name: Commit & Push
        if: steps.NotionSync.outputs.updated_count != '0'
        uses: stefanzweifel/git-auto-commit-action@v4
        with:
          file_pattern: 'content/'
          commit_message: Automatic NotionSync.

  # Build job
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.114.0
    needs: notionSyncTask
    if: needs.notionSyncTask.outputs.HAS_CHANGES
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: Install Dart Sass
        run: sudo snap install dart-sass
      - name: Checkout
        uses: actions/checkout@v3
        with:
          submodules: recursive
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v3
      - name: Install Node.js dependencies
        run: "[[ -f package-lock.json || -f npm-shrinkwrap.json ]] && npm ci || true"
      - name: Build with Hugo
        env:
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          path: ./public

  # Deployment job
  deploy:
    environment:
      name: github

-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2
```

Adjust the `schedule` as per your needs, but it's recommended to have an interval of not less than 20 minutes.
