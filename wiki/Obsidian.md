---
类型: 实体
实体类别: 工具
最后更新: 2026-04-08
标签: [知识管理, 工具, Markdown]
---

# Obsidian

## 简介

一款基于 Markdown 的本地知识管理工具，支持双向链接和图谱视图。在 [[LLM Wiki]] 模式中被推荐作为 wiki 的浏览前端。

## 在 LLM Wiki 中的角色

[[Andrej Karpathy]] 将 Obsidian 比喻为 IDE：

> Obsidian 是 IDE，LLM 是程序员，wiki 是代码库。

实际使用中，一边打开 LLM Agent 编辑 wiki 内容，一边在 Obsidian 中实时浏览：点击链接、查看图谱视图、阅读更新后的页面。

## 相关功能

- **图谱视图**：查看 wiki 的整体连接结构，发现枢纽页面和孤立页面——Karpathy 称之为"看到 wiki 形状"的最佳方式
- **双向链接**：`[[页面名]]` 语法，自动建立页面间的双向关联
- **Web Clipper**：浏览器扩展，将网页文章转换为 Markdown，快速将来源放入 raw/ 目录
- **本地图片下载**：在设置中配置附件目录（如 `raw/assets/`），绑定快捷键（如 Ctrl+Shift+D）批量下载文章中的图片到本地，让 LLM 可以直接引用
- **Marp 插件**：从 wiki 内容生成 Markdown 格式的幻灯片
- **Dataview 插件**：查询页面 YAML frontmatter（标签、日期、来源数等），生成动态表格和列表

## 来源

- [[来源_Karpathy LLM Wiki Gist]]（原始来源）
- [[来源_Karpathy知识库LLM Wiki火爆全网]]
