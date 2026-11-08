# Article Library · 文章资料库

按文章集中管理原文链接、中文翻译、解读与生成的 HTML。仓库默认保持私有，不启用公开网站。

## 文章目录

### 001 · 当 Agent 替你工作时，如何保持批判性思维

Addy Osmani · *Critical thinking when agents do the work*

- [文章信息与来源](articles/critical-thinking-with-agents/README.md)
- [完整中文翻译 · 重点高亮](articles/critical-thinking-with-agents/translation.zh-CN.html)
- [中文可视化解读 · 互动练习](articles/critical-thinking-with-agents/visual-guide.zh-CN.html)

两份 HTML 是同一篇文章的不同阅读版本，原有文件内容保持不变。

## 如何阅读

GitHub 的文件页面主要显示 HTML 源码。下载或克隆仓库后，用浏览器打开根目录的 `index.html`，即可进入阅读目录。两份文章 HTML 均为单文件，可独立离线打开；外部原文链接需要联网。

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
5. 参照现有文章填写 `metadata.json`，并更新本文件和根目录 `index.html` 的入口。

## 版权与来源

本仓库用于个人阅读与资料管理。原文版权归原作者所有；翻译、概括与可视化解读均保留来源说明。本仓库未附加开源许可，不表示对原文或派生内容授予再分发权利。
