# AI Coding Wiki

基于 LLM 维护的AI Coding知识库，灵感来自 [Andrej Karpathy 的 LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) 理念。核心思想：**知识编译一次、持续更新**，而非每次查询重新推导。

## 工作方式

- **LLM（Claude Code）** 负责摄入原始资料、生成 wiki 页面、维护交叉引用
- **用户** 负责提供资料来源、提出问题、引导分析方向
- **Obsidian** 作为 wiki 浏览前端，支持双链导航和图谱视图

## 目录结构

```
raw/            # 原始资料（只读，LLM 不修改）
  assets/       # 图片、附件
wiki/           # LLM 生成和维护的 wiki 页面
  index.md      # 内容索引
  log.md        # 操作日志
CLAUDE.md       # LLM 工作规范（Schema）
```

## 页面类型

| 类型 | 文件名格式 | 说明 |
|------|-----------|------|
| 来源摘要 | `来源_<标题>.md` | 对应 `raw/` 中的每份原始资料 |
| 概念 | `<概念名>.md` | 核心概念、理论、方法论 |
| 实体 | `<实体名>.md` | 人物、组织、工具、项目 |
| 主题 | `主题_<标题>.md` | 跨多个来源的综合分析 |
| 比较 | `比较_<A>与<B>.md` | 对比分析 |

## 当前知识库内容

**已摄入 3 份资料：**

- Karpathy 知识库「LLM Wiki」火爆全网（机器之心报道）
- 天猫胶水编程实践（97.9% 代码采纳率）
- Dijkstra 48 年前预言与 Vibe Coding

**已建立 16 个 wiki 页面**，涵盖概念（胶水编程、Vibe Coding、上下文工程等）、实体（Karpathy、Dijkstra、Obsidian）和来源摘要。

## 使用方法

### 摄入新资料

1. 将原始资料放入 `raw/` 目录
2. 告诉 Claude Code 处理新资料
3. LLM 自动生成来源摘要、创建/更新概念页和实体页、维护索引

### 查询知识

向 Claude Code 提问，LLM 会检索 wiki 页面并综合回答。

### 维护检查

让 Claude Code 执行维护（Lint），检查矛盾信息、孤立页面、缺失链接等。

## 技术栈

- **知识管理**：Obsidian（Markdown + 双链）
- **LLM 代理**：Claude Code
- **版本控制**：Git
