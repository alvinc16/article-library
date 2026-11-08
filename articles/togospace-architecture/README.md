# TogoSpace 源码设计分析

[阅读 HTML](analysis.zh-CN.html) · [原仓库](https://github.com/alexazhou/TogoSpace)

基准提交：`4c3f27839329c00ff5bf531d6d99ac4617d3658d`（2026-11-02）。收录：2026-11-08。

覆盖 Agent 交互、任务调度、Session 生命周期、历史压缩、持久文件、Prompt 来源清单及不同 Driver 的边界。

这是原创中文分析，不是原仓库文档的全文翻译。Prompt 以用途说明与固定源码链接呈现，不含全部 Prompt 原文和逐字翻译。核查仅为静态代码阅读，未运行项目或测试。
