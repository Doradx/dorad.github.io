---
abbrlink: dd3f
categories:
  - 生活
  - 测评
created: 2023-04-21 06:29:00
description: |-
  ChatGPT发布到现在，仅过去了四个月。而衍生出的各类产品、插件和竞品，井喷式地爆发着。
  此文记录个人使用GPT相关产品的个人体验，以及一些个人使用建议。
tags:
  - AI
  - GPT
  - ChatGPT
status: 已发布
type: post
updated: 2023-09-04 09:43:00
date: 2023-05-04 08:00:00
filename: ai-experience
title: AI工具-效率提升神器-使用体验
cover: https://i.cuger.cn/b/144a6466-f3c3-4ae5-8203-4b1558241372.png
id: f45d299e-d18e-409a-bebf-736f361bf714
---

# 写在前面

ChatGPT 发布到现在，仅过去了四个月。而衍生出的各类产品、插件和竞品，井喷式地爆发着。

此文记录个人使用 GPT 相关产品的个人体验，以及一些个人使用建议。

# ChatGPT

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://openai.com/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">OpenAI</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">Creating safe AGI that benefits all of humanity</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://openai.com/</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://images.openai.com/blob/fb4a2ba6-9109-4c7b-af4d-cae530c3fa78/recruitment-video-poster.jpg?trim=0%2C0%2C0%2C0&width=1000&quality=80" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

高强度使用，包括但不限于代码思路、代码错误分析、XX 总结/汇报/感想（无不良引导 🤣）、邮件套话、英文翻译润色.etc

总而言之，非常擅长写车轱辘话。。。而且逻辑能力尚可，让写一下正则表达式完全没啥问题。

之前还开了个`Pro`，试了一下`GPT4`，结果还有提问频率限制，刚开始是`100次/3h`，后来直接降到`25次/3h`，买了个爹。遂弃坑，免费版`GPT3.5`也挺香，付费版`GPT3.5`模型也快不到哪里去。

## ChatGPT 非官方客户端

<div style="margin:5px 1px;"> <a href="https://github.com/lencx/ChatGPT" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/16164244?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">lencx/ChatGPT</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">lencx</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2022-12-07T09:43:02Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

目前在 GitHub 斩获`33K` Stars，非官方跨平台客户端。

### 优点

- 提供会话导出
- 集成大量 prompts，也可快捷自定义，非常便捷

### 缺点

- Win10 上使用经常会闪退，不知道什么情况（使用的最新版）

## **ChatGPT 学术优化**

科研工作专用 ChatGPT/GLM 拓展，特别优化学术 Paper 润色体验，模块化设计支持自定义快捷按钮&函数插件，支持代码块表格显示，Tex 公式双显示，新增 Python 和 C++项目剖析&自译解功能，PDF/LaTex 论文翻译&总结功能，支持并行问询多种 LLM 模型，支持 gpt-3.5/gpt-4/chatglm

<div style="margin:5px 1px;"> <a href="https://github.com/binary-husky/chatgpt_academic" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/96192199?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">binary-husky/gpt_academic</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">binary-husky</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2023-03-20T09:05:13Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

## **Awesome ChatGPT**

> Curated list of awesome tools, demos, docs for ChatGPT and GPT-3

<div style="margin:5px 1px;"> <a href="https://github.com/humanloop/awesome-chatgpt" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/62994890?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">humanloop/awesome-chatgpt</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">humanloop</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2022-12-04T12:28:23Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

搜集了众多 ChatGPT 和 GPT3 的衍生产品。

## 案例

![写车轱辘话的邮件那真是一套一套的，省了不少事。](https://i.cuger.cn/b/ff9de7f3-be56-4eb4-9ae8-590ea0b98d81.png)

# New Bing

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.bing.com/new"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">Introducing the new Bing</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">Ask real questions. Get complete answers. Chat and create.</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.bing.com/rp/SOP97zQpFD4pG6teqCTC-c4LEgE.svg"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.bing.com/new</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://www.bing.com/sa/simg/facebook_sharing_5.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

> Updates: 2023.05.04 New Bing 正式开放，无需加入 waitlist

免费使用，GPT4 模型，响应速度一般，会先根据你的提问在搜索引擎检索，再给出 AI 的总结性回复，会给引用源。

中文高强度引用[知乎](https://www.zhihu.com/)，估计是权重比较高，对比而言，英文问答的质量明显更高。

对于编程的理解能力比 ChatGPT 3.5 的模型要差一点，适合做文档查询和信息检索。

用英文提问，回答的质量会稍微高一点。Bing 的中文检索本来就不咋地，也能理解。中文回答高强度引用[知乎](https://www.zhihu.com/)，而知乎还天天在搞盐选和虚拟创作。简中互联网真的在堕落吗？。

## 优点

- 整合了 Bing 搜索引擎的资源，搜索引擎+AI，吊打同类竞品。Where is google? 哈哈哈
- 免费，响应速度较快

## 缺点

- 中文资源较为匮乏

各厂商圈地自萌，稍微大点的项目文档，要么英文，要么中英双语。简中互联网何去何从。

> 刚开始注册用的主账号，死活注册不了，各种折腾。注册个新号，秒过。

# Midjourney

热门 AI 绘画工具，采用 discord 进行问答式图像生成，非常有趣。

想给自己生成个头像，订阅了一个月，尝试使用了一下，响应速度还挺快的，效果确实惊艳，但也存在一些问题。

目前唯一比较尴尬的点在于：

- trial 已经取消，无法试用，只能订阅（月费 10 美元，不含税）
- 只能在 discord 上进行聊天生成，大家都可以看到你的消息记录，私密性较差

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.midjourney.com/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">www.midjourney.com</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;"></div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.midjourney.com/</div></div></div></a></div><div style="text-align: center; margin:0;"><p>Midjourney官方网站</p></div></div>

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.techxiaofei.com/post/ai/cartoon/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">Midjourney - 用AI绘制你的专属迪斯尼卡通头像</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">推广 tip 推荐以下翻墙必备工具 推荐 链接 教程 翻墙机场VPN 注册链接 自用机场推荐，翻墙VPN，秒开4K，解锁ChatGPT、奈飞流媒体 美国虚拟信用卡</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.techxiaofei.com/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.techxiaofei.com/post/ai/cartoon/</div></div></div></a></div><div style="text-align: center; margin:0;"><p>使用Midjourney给自己生成迪斯尼卡通头像</p></div></div>

![使用Midjourney生成的头像](https://i.cuger.cn/b/4025c504-1fd2-428f-a6a4-996e5d5858ac.png)

# GitHub Copilot

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://github.com/features/copilot"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">GitHub Copilot · Your AI pair programmer</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">GitHub Copilot works alongside you directly in your editor, suggesting whole lines or entire functions for you.</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://github.githubassets.com/favicons/favicon.svg"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://github.com/features/copilot</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://github.githubassets.com/images/modules/site/social-cards/copilot-ga.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

编程时高强度使用，多类型代码提示，极大提升效率。Edu 用户免费。

程序猿福音。真的是减少了很多重复性劳动。

如果你想让它帮你写非常准确的代码，那就好好撰写注释吧~哈哈哈

> 最逗的是，它会根据你的上下文的编程风格生成代码。。。  
> 如果写的一坨翔，生成的大概率也是一坨翔哈哈哈哈。。。

# Notion AI

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://www.notion.so/product/ai"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">Notion AI | Work faster. Write better. Think bigger.</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">Access the limitless power of AI, right inside Notion. Work faster. Write better. Think bigger.</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://www.notion.so/front-static/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://www.notion.so/product/ai</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://www.notion.so/front-static/meta/ai-v2.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

试用了 20 次，感觉还是不赖的。

Edu 用户 Notion 可免费升级 Pro，但 Notion AI 是另外付费，10 刀/月，还是相当贵的。。。

虽然是基于 GPT3 模型构建的，表现能力不俗。

综合来说性价比较低，目前暂无付费打算。

> 我让 Notion AI 给我扩充了一下上述内容，结果如下：  
> 我试用了 Notion AI20 次，感觉它的表现还是不错的。虽然它是基于 GPT3 模型构建的，但是它的表现能力非常不俗。  
> 虽然 Edu 用户可以免费升级到 Notion 的 Pro 版本，但 Notion AI 则需要额外支付，价格为每月 10 美元，相当昂贵。然而，我认为这个价格是值得的，因为它可以给你带来很多的便利。  
> 例如，使用 Notion AI，你可以轻松地创建复杂的文档和报告，而不需要过多地考虑文本的结构和语法。此外，Notion AI 还可以帮助你更快地完成日常任务，如发送电子邮件、提醒和日程安排。  
> 虽然 Notion AI 的价格比较高，但是它的性能和便利性是无可比拟的。因此，我强烈建议你考虑使用 Notion AI 来提高你的工作效率和准确性。

哈哈哈哈，肉眼可见其篡改了我的意思。。。强行自我安利，有趣~

# AI Shell

<div style="margin:5px 1px;"> <a href="https://github.com/BuilderIO/ai-shell" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/35700027?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">BuilderIO/ai-shell</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)">BuilderIO</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2023-04-05T18:17:07Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

体验了几次，需要使用 openai 的 API KEY，开源项目。

用 Shell 交互的方式，提供建议的命令行，并给出解释，案例如下：

```shell
dorad@DESKTOP:~$ ai "write a regrex to match all the image path within a markdown file, including the images from internet and local"
┌  AI Shell
│
◇  Your script:

grep -Po '(https?:\/\/[^\s)]+|(?<=\().*?(?=\)))' input.md

•
│
◇  Explanation:

1. Utilizes the 'grep' command
2. Searches for patterns matching either 'https://' or 'http://'
3. Looks for any non-whitespace character until a space or ')' is found
4. Extracts any text between parentheses (if present)
5. Searches for patterns in a file named 'input.md'

•
│
◆  Run this script?
│  ● ✅ Yes (Lets go!)
│  ○ 📝 Edit
│  ○ 🔁 Revise
│  ○ ❌ Cancel
```

使用体验上没有特别亮的点，唯一优势可能是可以命令行执行吧。

推荐在远程无 GUI VPS 上使用，本地不推荐，对比 New Bing 等同类产品无明显优势。

# ChatGLM-6B

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://huggingface.co/THUDM/chatglm-6b"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">THUDM/chatglm-6b · Hugging Face</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">We’re on a journey to advance and democratize artificial intelligence through open source and open science.</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src=""style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://huggingface.co/THUDM/chatglm-6b</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://cdn-thumbnails.huggingface.co/social-thumbnails/models/THUDM/chatglm-6b.png" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

清华大学技术成果转化公司（智普 AI）开发的开源模型，内测已停。

支持本地化部署，毕竟开源，6B 版需要 13G 显存，4T 版需要 6G 显存，暂未实际部署体验，等回国拿工作站试试~

优点：

- 开源、免费
- 本地化部署，安全，稳定

缺点：

- 硬件要求较高

# 有趣项目

## 数字永生(雏形)

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://sspai.com/post/79230"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">用 10 万条微信聊天记录和 280 篇博客文章，我克隆了一个数字版自己 - 少数派</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">Matrix精选Matrix是少数派的写作社区，我们主张分享真实的产品体验，有实用价值的经验与思考。我们会不定期挑选Matrix最优质的文章，展示来自用户的最真实的体验和观点。文章代表作者个人观点，少 ...</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://cdn-static.sspai.com/favicon/sspai.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://sspai.com/post/79230</div></div></div><div style="flex: 1 1 180px; display: block; position: relative;"><div style="position: absolute; inset: 0px;"><div style="width: 100%; height: 100%;"><img src="https://cdn.sspai.com/2023/4/19/article/8a6bfed2-13bf-a68d-2353-bbe3f14d95cc.jpg" referrerpolicy="no-referrer" style="display: block; object-fit: cover; border-radius: 3px; width: 100%; height: 100%;"></div></div></div></a></div></div>

这老哥用自己日常产生的数据用 ChatGLM-6B+个人数据训练生成了自己，数字生命雏形哈哈哈哈

开放了体验接口：[DK 数字分身 (greatdk.com)](https://ai.greatdk.com/)

有兴趣的小伙伴可以尝试和他聊聊，暴躁老哥一个哈哈哈

很有意思

## 法律助手

<div style="width: 100%; margin-top: 4px; margin-bottom: 4px;"><div style="display: flex; background:white;border-radius:5px"><a href="https://law-cn-ai.vercel.app/"target="_blank"rel="noopener noreferrer"style="display: flex; color: inherit; text-decoration: none; user-select: none; transition: background 20ms ease-in 0s; cursor: pointer; flex-grow: 1; min-width: 0px; flex-wrap: wrap-reverse; align-items: stretch; text-align: left; overflow: hidden; border: 1px solid rgba(55, 53, 47, 0.16); border-radius: 5px; position: relative; fill: inherit;"><div style="flex: 4 1 180px; padding: 12px 14px 14px; overflow: hidden; text-align: left;"><div style="font-size: 14px; line-height: 20px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-height: 24px; margin-bottom: 2px;">AI 法律助手</div><div style="font-size: 12px; line-height: 16px; color: rgba(55, 53, 47, 0.65); height: 32px; overflow: hidden;">AI 法律助手</div><div style="display: flex; margin-top: 6px; height: 16px;"><img src="https://law-cn-ai.vercel.app/favicon.ico"style="width: 16px; height: 16px; min-width: 16px; margin-right: 6px;"><div style="font-size: 12px; line-height: 16px; color: rgb(55, 53, 47); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">https://law-cn-ai.vercel.app/</div></div></div></a></div></div>

根据中国法律法规+ChatGPT 生成的法律 AI 助手，有啥不懂的可以去问问看。

尝试私有化部署，但刚部署完还不能生效，是个人工智障。

![刚部署完的效果，需要等待](https://i.cuger.cn/b/8f345d34-b137-49b4-be4f-b1ec950fa3d8.png)

> 若配置正确，初次部署会对全部法律条文计算 embedding，因此时间较久并且会产生较大的资费。我个人这边是用了 100 分钟左右，开销大概为 3 USD。此外 Vercel 的构建有 45 分钟限制，因此需要手动重新部署两次左右。

<div style="margin:5px 1px;"> <a href="https://github.com/lvwzhen/law-cn-ai/issues/10" target="_blank" rel="noopener noreferrer" style="display:flex;color:inherit;background:#f5f5f5;text-decoration:none;user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;flex-grow:1;min-width:0;align-items:center;border:1px solid rgba(55,53,47,.16);border-radius:5px;padding:6px;fill:inherit"><div style="display:flex;align-self:start;height:32px;width:32px;margin:3px 12px 3px 4px;position:relative"><div><div style="width:100%;height:100%"><img src="https://avatars.githubusercontent.com/u/13360135?v=4" referrerpolicy="same-origin" style="display:block;object-fit:cover;border-radius:34px;width:30.192px;height:30.192px;transition:opacity .1s ease-out 0s;box-shadow:rgba(15,15,15,.1) 0 2px 4px"></div></div><div style="position:absolute;bottom:-2px;right:-2px"><div style="width:100%;height:100%"><svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 496 512" style="display:block;object-fit:cover;border-radius:5px;width:14.208px;height:14.208px;transition:opacity .1s ease-out 0s;filter:drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px) drop-shadow(white 0 0 1px)"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"></path></svg></div></div></div><div style="display:flex;flex-direction:column;justify-content:center;flex-grow:1;flex-shrink:1;overflow:hidden"><div style="display:flex;align-items:baseline;font-size:14px"><div spellcheck="false" style="white-space:nowrap;color:#37352f;font-weight:500;overflow:hidden;text-overflow:ellipsis">自行部署指南 <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="12.5" height="12.5"><path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3Z"></path><path d="M8 0a8 8 0 1 1 0 16A8 8 0 0 1 8 0ZM1.5 8a6.5 6.5 0 1 0 13 0 6.5 6.5 0 0 0-13 0Z"></path></svg> #10<span style="margin-left:3px;margin-right:3px">•</span>Open</div></div><div style="display:flex;align-items:center;color:rgba(55,53,47,.65);font-size:12px"><div spellcheck="false" style="white-space:nowrap;color:rgba(55,53,47,.65)"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="12.5" height="12.5"><path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3Z"></path><path d="M8 0a8 8 0 1 1 0 16A8 8 0 0 1 8 0ZM1.5 8a6.5 6.5 0 1 0 13 0 6.5 6.5 0 0 0-13 0Z"></path></svg> #10<span style="margin-left:3px;margin-right:3px">•</span>kaaass</div><span style="margin-left:3px;margin-right:3px">•</span><div style="color:rgba(55,53,47,.65);font-size:12px;white-space:nowrap">Created: 2023-04-22T11:50:35Z</div></div></div><div role="button" tabindex="0" style="user-select:none;transition:background 20ms ease-in 0s;cursor:pointer;opacity:0;display:flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:5px;flex-shrink:0;margin-right:4px;color:rgba(55,53,47,.65)"><svg viewbox="0 0 13 3" class="dots" style="width:14px;height:100%;display:block;fill:inherit;flex-shrink:0;backface-visibility:hidden;color:rgba(55,53,47,.45)"><g><path d="M3,1.5A1.5,1.5,0,1,1,1.5,0,1.5,1.5,0,0,1,3,1.5Z"></path><path d="M8,1.5A1.5,1.5,0,1,1,6.5,0,1.5,1.5,0,0,1,8,1.5Z"></path><path d="M13,1.5A1.5,1.5,0,1,1,11.5,0,1.5,1.5,0,0,1,13,1.5Z"></path></g></svg></div></a></div>

遂放弃部署。

# 总结

无论你愿不愿意、喜不喜欢，AI 都正在“入侵”到我们生活的各方各面。

人总归是要适应时代洪流的，而 AI 可能就是未来生活不可或缺的一部分，至少目前已快成为我日常工作生活的一部分。
