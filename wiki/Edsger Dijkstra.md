---
类型: 实体
实体类别: 人物
最后更新: 2026-04-07
标签: [计算机科学, 形式化方法, 先驱]
---

# Edsger Dijkstra

## 简介

Edsger Wybe Dijkstra（1930-2002），荷兰计算机科学家，被誉为计算机科学的"祖师爷"之一。以最短路径算法（Dijkstra 算法）、结构化编程倡导、信号量（semaphore）概念等贡献闻名。1972 年获图灵奖。

## 与本 wiki 的关联

### EWD667：论「自然语言编程」的愚蠢（1978）

Dijkstra 的手稿 EWD667（《On the foolishness of "natural language programming"》）在 AI 编程时代获得了新的生命力。其三个核心论点：

1. **形式化符号是文明进步的引擎，不是累赘**——数学史证明，符号化推动了科学进步
2. **自然语言的"自然"是危险的舒适**——让人轻松说出荒谬性并不显而易见的话
3. **窄接口原则**——约束越明确，合作越高效；接口变宽，两边都更累

48 年后，[[Vibe Coding]] 的实践问题精准验证了这些预言：AI 总是漏需求（模糊性）、代码无架构感（缺乏形式化约束）、上下文越长越降智（宽接口的代价）。

### 窄接口思想的现代实践

Dijkstra 的窄接口原则在当代 AI 编程中体现为：

- CLAUDE.md / AGENTS.md — 写给 AI 的形式化规范
- [[胶水编程]]的四层物料体系 — 结构化的上下文注入
- [[Harness Engineering]] — 构建形式化约束环境
- TDD / CI/CD — 自动化验证闭环

> 形式化文本的美德在于，其操作只需满足少数简单规则；它们是排除各种胡说八道的极其有效的工具。——EWD667

## 相关实体与概念

- [[Andrej Karpathy]] — 推广了 [[Vibe Coding]]，而 Vibe Coding 的问题恰好验证了 Dijkstra 的预言
- [[Vibe Coding]] — 自然语言编程的现代实现，EWD667 的反面例证
- [[Harness Engineering]] — Dijkstra 窄接口思想在 AI 时代的系统化实践

## 来源

- [[来源_Dijkstra预言与Vibe Coding]]
