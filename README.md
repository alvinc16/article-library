# Article Library · 文章资料库

按文章集中管理原文链接、中文翻译、解读与生成的 HTML。仓库现已公开，并通过 GitHub Pages 发布公开网站。

在线阅读：[文章资料库](https://alvinc16.github.io/article-library/index.html)。

## 文章目录

### 001 · 当 Agent 替你工作时，如何保持批判性思维

Addy Osmani · *Critical thinking when agents do the work*

- [文章信息与来源](articles/critical-thinking-with-agents/README.md)
- [完整中文翻译 · 重点高亮](articles/critical-thinking-with-agents/translation.zh-CN.html)
- [中文可视化解读 · 互动练习](articles/critical-thinking-with-agents/visual-guide.zh-CN.html)

两份 HTML 是同一篇文章的不同阅读版本，原有文件内容保持不变。

### 002 · TogoSpace 源码设计：Agent 交互、Prompt、Session 与记忆

alexazhou / TogoSpace · 基准提交 `4c3f27839329c00ff5bf531d6d99ac4617d3658d`

- [源码设计图解](articles/togospace-architecture/analysis.zh-CN.html)
- [文章信息与核查范围](articles/togospace-architecture/README.md)
- [Prompt 清单与源码入口](articles/togospace-architecture/analysis.zh-CN.html#prompts)

静态源码分析，未运行项目；Prompt 部分为原创解释与源码链接，不含全部原文和逐字翻译。

## 如何阅读

GitHub 的文件页面主要显示 HTML 源码。下载或克隆仓库后，用浏览器打开根目录的 `index.html`，即可进入文章主页。主页支持主题标签筛选、标题／作者／标签搜索，以及按收录日期正序或倒序排列的年度时间线；搜索和标签可组合使用，无结果时可一键清除筛选。两份文章 HTML 均为单文件，可独立离线打开；外部原文链接需要联网。

## 目录约定

```text
article-library/
├── README.md
├── index.html
└── articles/
    └── critical-thinking-with-agents/
        ├── README.md                 # 标题、作者、来源与版本说明
        ├── metadata.json             # 可供后续目录工具使用的文章信息
        ├── translation.zh-CN.html    # 完整中文翻译
        └── visual-guide.zh-CN.html   # 中文可视化解读
```

## 添加下一篇文章

1. 在 `articles/` 下新建一个简短、稳定的英文目录名，例如 `building-better-agents/`。
2. 把同一篇文章的全部文件放入这个目录，不按文件类型拆散。
3. 添加 `README.md`，记录原文标题、作者、原文链接、收录日期、翻译或解读说明。
4. 按需要添加 `source.md`、`notes.md`、`translation.zh-CN.html`、`visual-guide.zh-CN.html` 和 `assets/`。只保存已经取得并允许保存的材料，不用占位内容冒充原文。
5. 参照现有文章填写 `metadata.json`，并更新本文件的文章目录。
6. 打开根目录 `index.html`，在底部脚本的 `ARTICLES` 数组中复制现有对象，为新文章填写以下字段：
   - `id`：与目录名一致的唯一标识。
   - `title`、`original_title`、`author`：中文标题、原文标题与作者。
   - `added_on`：收录日期，严格使用 `YYYY-MM-DD`，时间线按它分组排序（不是原文发布日期）。
   - `tags`：与该篇 `metadata.json` 一致的标签数组；新标签会自动出现在筛选栏。
   - `summary`：一两句阅读提示。
   - `translation`、`guide`：相对根目录 `index.html` 的两份 HTML 路径。也可使用 `links` 数组，每项含 `path` 和 `label`，适用于源码分析等不同阅读形式。
7. 如果标签原值为英文，可在 `TAG_LABELS` 中增加中文显示名；未配置的标签直接显示原值。日期、标签计数和时间线会自动更新，不必手动添加卡片。
8. 用浏览器直接打开 `index.html`，验证新文章在标签、搜索和时间线中出现，且两份阅读链接均能打开。

### 离线索引说明

主页使用内嵌 CSS 和 JavaScript，不请求网络、不使用 `fetch`，因此不需要启动服务器、安装依赖或构建。为兼容 `file://`，索引数据直接保存在 `ARTICLES` 数组，不会自动读取各篇 `metadata.json`；修改标题、日期或标签时，请同步更新两处。

搜索匹配中文／原文标题、作者以及标签的原始值和中文显示名，不搜索文章正文。每次刷新恢复默认的「全部文章、最新收录在前」。JavaScript 被禁用时，页面保留首篇文章的静态入口；如需扩充无脚本入口，可同步更新 `<noscript>` 区域。

## 版权与来源

本仓库用于个人阅读与资料管理。原文版权归原作者所有；翻译、概括与可视化解读均保留来源说明。本仓库未附加开源许可，不表示对原文或派生内容授予再分发权利。
