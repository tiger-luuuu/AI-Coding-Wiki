---
类型: 实体
实体类别: 工具
最后更新: 2026-04-08
标签: [搜索引擎, 工具, Markdown, 知识管理]
---

# qmd

## 简介

一个本地 Markdown 文件搜索引擎，由 Tobi Lütke 开发，被 [[Andrej Karpathy]] 在 [[LLM Wiki]] 的 gist 中推荐为 wiki 规模增长后的检索工具。

- GitHub 地址：`https://github.com/tobi/qmd`

## 核心特性

- **混合搜索**：结合 BM25（关键词匹配）和向量搜索（语义匹配）
- **LLM 重排序**：用 LLM 对搜索结果进行二次排序，提升相关性
- **全本地运行**：所有计算在设备上完成，无需外部服务
- **双接口**：
  - **CLI**：LLM Agent 可通过 shell 调用
  - **MCP server**：LLM 可作为原生工具（native tool）直接使用

## 在 LLM Wiki 中的角色

[[LLM Wiki]] 在中等规模下（~100 篇来源）仅靠 index.md 索引文件即可支撑检索。但随着 wiki 增长，需要更强的搜索能力。Karpathy 推荐 qmd 作为这一阶段的解决方案：

> [qmd] is a local search engine for markdown files with hybrid BM25/vector search and LLM re-ranking, all on-device. It has both a CLI (so the LLM can shell out to it) and an MCP server (so the LLM can use it as a native tool).

也可以选择自行编写更简单的搜索脚本——LLM 可以帮助快速搭建。

## 相关概念

- [[LLM Wiki]] — qmd 的主要使用场景
- [[RAG]] — qmd 的混合搜索与 RAG 的向量检索有相通之处，但服务于不同的架构

## 来源

- [[来源_Karpathy LLM Wiki Gist]]
