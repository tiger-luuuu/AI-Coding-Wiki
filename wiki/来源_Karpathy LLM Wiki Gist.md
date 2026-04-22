---
类型: 来源摘要
来源文件: "raw/llm-wiki.md"
来源链接: "https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f"
作者: Andrej Karpathy
日期: 2026-04-08
最后更新: 2026-04-08
标签: [LLM Wiki, Karpathy, 知识管理, 元框架]
---

# Karpathy LLM Wiki Gist（原始来源）

## 基本信息

- **来源**：GitHub Gist
- **作者**：[[Andrej Karpathy]]
- **性质**：这是 [[LLM Wiki]] 理念的**原始出处**，以"想法文件"（idea file）形式发布，旨在分享理念而非具体实现

## 核心要点

1. LLM Wiki 的本质：让 LLM **增量构建并维护持久化 wiki**，取代每次查询从零检索的 [[RAG]] 模式
2. 三层架构（原始数据 / Wiki / Schema）+ 三大操作（Ingest / Query / Lint）
3. 知识管理的核心瓶颈不是阅读或思考，而是**记账式的维护工作**——LLM 恰好能解决这个问题
4. 思想源流可追溯至 [[Memex]]（Vannevar Bush, 1945）——个人策划的知识库，文档间关联与文档本身同等重要
5. 推荐 [[qmd]] 作为 wiki 规模增长后的本地搜索引擎

## 详细摘要

### 设计哲学："想法文件"

Karpathy 将这份文档定义为 idea file：在 Agent 时代，不需要分享具体代码或应用，只需分享想法，由对方的 Agent 自动完成定制和实现。文档刻意保持抽象，不绑定具体目录结构、工具链或模型。

### 核心理念

大多数人与 LLM 处理文档的方式是 [[RAG]]：上传文件，查询时检索片段，生成答案。LLM Wiki 不同之处在于：

> When you add a new source, the LLM doesn't just index it for later retrieval. It reads it, extracts the key information, and integrates it into the existing wiki — updating entity pages, revising topic summaries, noting where new data contradicts old claims.

知识被**编译一次并持续更新**，而非每次查询时重新推导。wiki 是一个**持续存在、不断复利的产物**（persistent, compounding artifact）。

### 三层架构

1. **原始数据层（Raw sources）**：不可变，LLM 只读不写，是事实来源
2. **Wiki 层**：LLM 全权维护的 Markdown 文件集合——摘要、实体页、概念页、比较、综述
3. **Schema 层**：配置文档（如 CLAUDE.md），让 LLM 从通用聊天模型变为有纪律的 wiki 维护者

### 三大操作

- **摄入（Ingest）**：添加新资料，LLM 阅读、讨论、创建摘要页、更新索引和相关页面。单次摄入通常影响 10-15 个页面
- **查询（Query）**：围绕 wiki 提问。关键洞察——**好的回答可以归档为新页面**，实现知识复利
- **质量检查（Lint）**：定期健康检查——矛盾、过时信息、孤立页面、缺失概念、缺失交叉引用、可用网络搜索填补的空白

### 索引与日志

- **index.md**：内容导向，按类别组织的页面目录。LLM 查询时先读索引定位相关页面，中等规模下无需 embedding 基础设施
- **log.md**：时间导向，追加记录操作历史。使用一致前缀格式使其可被 unix 工具解析

### CLI 工具建议

随着 wiki 规模增长，index.md 可能不足以支撑检索。Karpathy 推荐 [[qmd]]：

> [qmd](https://github.com/tobi/qmd) is a good option: it's a local search engine for markdown files with hybrid BM25/vector search and LLM re-ranking, all on-device.

qmd 提供 CLI 和 MCP server 两种接口，也可以自行编写简单的搜索脚本。

### 实用技巧

- **Obsidian Web Clipper**：浏览器扩展，将网页转为 Markdown
- **本地下载图片**：在 Obsidian 设置中配置附件目录，绑定快捷键批量下载图片到本地
- **图谱视图**：查看 wiki 的连接结构、枢纽页面和孤立页面
- **Marp**：从 wiki 内容生成幻灯片
- **Dataview**：查询页面 YAML frontmatter，生成动态表格和列表
- Wiki 本质是 Markdown 文件的 git 仓库，天然获得版本历史、分支和协作能力

### 为什么有效

> The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping. Updating cross-references, keeping summaries current, noting when new data contradicts old claims, maintaining consistency across dozens of pages.

人类放弃维护 wiki 是因为维护负担的增长速度超过了知识的价值增长。LLM 不会厌倦，不会忘记更新交叉引用，一次可以修改 15 个文件。维护成本趋近于零。

**人类的角色**：策划来源、引导分析、提出好问题、思考意义
**LLM 的角色**：其他一切——摘要、交叉引用、归档、记账

### 思想源流：Memex

Karpathy 将 LLM Wiki 与 [[Memex]]（Vannevar Bush, 1945）联系起来：

> The idea is related in spirit to Vannevar Bush's Memex (1945) — a personal, curated knowledge store with associative trails between documents. Bush's vision was closer to this than to what the web became: private, actively curated, with the connections between documents as valuable as the documents themselves. The part he couldn't solve was who does the maintenance. The LLM handles that.

### 应用场景

- 个人成长：目标、健康、心理、自我提升
- 深度研究：论文、文章、报告
- 阅读辅助：章节整理、人物/主题/情节关联（如个人版 Tolkien Gateway）
- 企业/团队：接入 Slack、会议记录、项目文档
- 竞品分析、尽职调查、旅行规划、课程笔记、兴趣深挖

## 与 wiki 中其他页面的关联

- [[来源_Karpathy知识库LLM Wiki火爆全网]] — 机器之心对本 gist 的二手报道
- [[LLM Wiki]] — 本 gist 所阐述的核心概念
- [[RAG]] — LLM Wiki 试图超越的传统模式
- [[元框架]] — gist 的"想法文件"设计本身就是元框架理念的体现
- [[Obsidian]] — 推荐的浏览前端
- [[qmd]] — 推荐的 wiki 搜索引擎
- [[Memex]] — LLM Wiki 的思想先驱
