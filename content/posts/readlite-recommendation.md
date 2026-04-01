---
title: "插件推荐：ReadLite——打造你的沉浸式阅读空间"
date: 2026-04-01
tags: ["工具推荐", "阅读", "浏览器插件"]
---

## 信息过载时代的个人解法

作为一个长期依赖浏览器阅读的技术人，我受够了满屏的广告、侧边栏和弹窗。几年前的某个午后，我决定自己动手——于是有了 **ReadLite**。

ReadLite 是一个轻量级的浏览器阅读模式扩展，核心目标很纯粹：把任何网页变成干净、舒适的文档视图。它基于 Mozilla 的 Readability 引擎，但我在上面加了点自己的坚持。

## 为什么做 ReadLite？

市面上有 Safari 的阅读视图、Firefox 的 Reader Mode、Chrome 的 Distill Page，但它们要么功能太基础，要么平台受限。我想做一个：

- **跨浏览器统一体验**（Chrome/Firefox 都能用）
- **深度可定制**（让用户按自己的阅读习惯调整）
- **保留笔记能力**（很多阅读扩展忽略了这一点）

## 技术亮点

ReadLite 的实现有几个关键点：

1. **Readability 核心 + 样式隔离**
   用 iframe sandbox 机制把原始页面的样式完全隔离，再注入一套精心调过的阅读主题。字体、行高、段落间距都参考了 Medium 和 Safari 阅读视图的最佳实践。

2. **多主题系统**
   内置 Light/Dark/Sepia 三套主题，每套都经过对比度测试。深色模式不仅是反转颜色，而是重新计算了灰度比例，避免刺眼的对比。

3. **用户配置持久化**
   所有设置（主题、字体、宽度等）以 per-site 或 global 方式存在 `chrome.storage` 里，同步到云端（可选）。

4. **笔记功能**
   这是我最看重的部分。划词高亮 + Markdown 导出，让我可以把 reading 变成 research。笔记数据存 LocalStorage，支持 JSON 导出，后续会考虑对接 Notion API。

## 如果你也在考虑做浏览器扩展

ReadLite 的代码完全开源（GitHub），用 TypeScript + Plasmo 框架开发。Plasmo 真的很香，一套代码构建出 Chrome/Firefox 两个版本，不用维护两套 manifest。

如果你对阅读体验优化、内容提取、跨浏览器开发感兴趣，欢迎来 GitHub 聊聊。有 issue 和 PR 都会认真看。

## 安装

- Chrome 用户：[Chrome 网上应用店](https://chromewebstore.google.com/detail/readlite-simple-reading-m/bcagnbmncmeliaknnhmbkkgackfipoic)
- Firefox 用户：[Firefox 附加组件](https://addons.mozilla.org/en-US/firefox/addon/readlite-simple-reading-mode/)

## 一个作者的小期望

ReadLite 没有付费功能，不收集用户数据，也不打算加社交分享。它就是我解决信息过载的一个个人工具，现在分享出来，万一也能帮到你。

如果你试用了，有任何反馈（bug、功能建议、使用场景），都欢迎来 GitHub 留言。我也会持续更新，比如 PDF 导出、语音阅读、更多主题等。

---

_代码开源在 GitHub: zhongyiio/readlite（搜索 "ReadLite" 就能找到）_