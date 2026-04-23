# 操作日志

> 按时间倒序记录 wiki 的所有操作。格式：`## [日期] 操作类型 | 标题`

## [2026-04-23] 摄入 | Harness Engineering 工程化落地（白家杰）

- 来源：微信公众号，作者白家杰，2026-04-23，案例项目：JK Launcher（Unity 桌面启动器）
- 创建页面：
  - `来源_Harness Engineering工程化落地_白家杰.md`（来源摘要）
  - `白家杰.md`（实体页）
- 更新页面：`Harness Engineering.md`（增加六大零件定义、SPEC先行、三种多 Agent 对比、七Agent架构、六轮补稳、总验证脚本、四块拼图、起步路径）、`index.md`、`log.md`
- 关键发现：
  - **Rule 只能做“原则约束”，不能做“流程执行”**：这是本文最近高层的认知，也是为什么成熟 Harness 越来越依赖脚本的根本原因
  - **结构化调度明确放弃去中心化协作**：“真正贵的不是 token，真正贵的是失控”——这是弹巳的工程层理念
  - **总验证脚本是最被低估的核心模块**：Harness 具备“结果感知能力”的关键一步，从此 AI 的“完成定义”不再是自就主观判断
  - **知识进项目而非进人**：真正专业的 Harness 不应来越像“我和我的 AI 的默契”，而是“任何人拿到这个工程都能顺着这套系统做对事情”
  - **与腾讯 LEGO 的互补**：白家杰路径（个人项目从零搞起）+ LEGO 路径（百万行 C++ 团队落地）+ 腾讯审核团队（L3全自动化），三种不同规模和场景的 Harness 实践已全部进入 wiki

## [2026-04-22] 摄入 | 如何正确 Vibe Coding？Schluntz 演讲

- 来源：微信公众号“Vibe Coding的”，演讲者 Erik Schluntz（Anthropic 研究员），2026-04-20
- 创建页面：
  - `来源_如何正确Vibe Coding_Schluntz.md`（来源摘要）
  - `Erik Schluntz.md`（实体页——Anthropic 研究员）
- 更新页面：`Vibe Coding.md`（增加叶子节点策略、可验证抽象层、TDD 实践）、`上下文工程.md`（增加前置规划工作流、Context Compact 技巧）、`index.md`、`log.md`
- 关键发现：
  - **叶子节点策略**是将 Vibe Coding 应用于生产环境的关键安全阀棒：只在不被其他模块依赖的末端功能区域使用 AI，主干人工控制
  - **可验证抽象层**是 Dijkstra 窄接口原则的工程实现：用 TDD/E2E 测试替代逐行审查
  - 22000 行代码、两周压缩到 1 天的实战案例证实了前置规划+可验证框架的有效性
  - **Context Compact** 技巧：先写文档再压缩，是上下文工程在实操层的核心技能

## [2026-04-22] 摄入 | 腾讯审核团队全链路AI自动化

- 来源：微信公众号"腾讯程序员"，腾讯审核团队，2026-04-22
- 创建页面：
  - `来源_腾讯审核团队全链路AI自动化.md`（来源摘要）
  - `AI全自动化交付.md`（概念页——L3 全自动化交付模式与公式）
- 更新页面：`Harness Engineering.md`（增加审核团队全链路自动化实践引用）、`index.md`、`log.md`
- 关键发现：
  - 腾讯审核团队提炼出公式：AI 全自动化交付 = LLM + Harness Engineering + Business Engineering
  - L3 全自动化需要"交付框架"（效率）+ "治理框架"（质量）双轮驱动，缺一不可
  - 当前 L2 阶段最大进展是打通测试和部署工具链（MCP），将跨平台从 6 个减为 1 个，步骤从 12 步减为 5 步

## [2026-04-22] 摄入 | 腾讯CDN LEGO Harness Engineering 实践

- 来源：微信公众号"腾讯程序员"，腾讯CDN LEGO团队，2026-04-22
- 创建页面：
  - `来源_腾讯CDN LEGO Harness Engineering实践.md`（来源摘要）
  - `对抗式CR.md`（概念页——多模型并行独立审查技术）
- 更新页面：`Harness Engineering.md`（大幅扩充，增加五层架构、工程实践细节）、`index.md`、`log.md`
- 关键发现：
  - Harness Engineering 的三大核心要素：上下文（消除记忆偏差）、约束（结构化约束替代语言化期望）、反馈（进化闭环）
  - 最危险的 AI 问题不是幻觉，而是"不会说我不知道"——AI 用自信语气输出错误结论，降低人的审查意愿
  - 对抗式 CR（三模型并行）将代码审查从等待 1-3 天压缩至 30 分钟
  - 工程体系才是核心资产（不是模型，不是 prompt），每个踩坑 → 规则 → Skill 的进化闭环是护城河

## [2026-04-08] 摄入 | Karpathy LLM Wiki Gist（原始来源）

- 来源：Karpathy GitHub Gist，LLM Wiki 理念的第一手原始文档
- 创建页面：
  - `来源_Karpathy LLM Wiki Gist.md`（来源摘要）
  - `qmd.md`（实体页——本地 Markdown 搜索引擎）
  - `Memex.md`（概念页——Vannevar Bush 1945 年的思想先驱）
- 更新页面：`LLM Wiki.md`、`Andrej Karpathy.md`、`Obsidian.md`、`RAG.md`、`元框架.md`、`index.md`
- 关键发现：
  - Karpathy 推荐 qmd 作为 wiki 规模增长后的搜索引擎（混合 BM25/向量搜索 + LLM 重排序）
  - LLM Wiki 的思想源流可追溯至 Memex（1945），LLM 解决了 Bush 当年无法回答的"谁来做维护"问题
  - 知识库维护的核心瓶颈是记账式工作而非思考，LLM 使维护成本趋近于零
  - gist 本身是"想法文件"设计：分享理念而非代码，由 Agent 自行实现

## [2026-04-07] 摄入 | Dijkstra 预言与 Vibe Coding

- 来源：知乎专栏文章（2026-04-03），作者王勃
- 创建页面：
  - `来源_Dijkstra预言与Vibe Coding.md`（来源摘要）
  - `Vibe Coding.md`（概念页）
  - `Harness Engineering.md`（概念页）
  - `Edsger Dijkstra.md`（实体页）
- 更新页面：`胶水编程.md`、`上下文工程.md`、`Andrej Karpathy.md`、`index.md`
- 关键发现：AI 编程工具演进（Prompt → Context → Harness）的方向是从自然语言走向形式化约束，这与胶水编程的三级递进（Vibe → SPEC → Glue）互为印证。Dijkstra 48 年前的预言在 AI 时代获得新的生命力

## [2026-04-07] 摄入 | 天猫胶水编程实践

- 来源：微信公众号"大淘宝技术"文章，天猫品牌行业前端团队
- 创建页面：
  - `来源_天猫胶水编程实践.md`（来源摘要）
  - `胶水编程.md`（概念页）
  - `上下文工程.md`（概念页）
  - `代码采纳率.md`（概念页）
- 更新页面：`LLM Wiki.md`、`RAG.md`、`元框架.md`、`index.md`
- 关键发现：胶水编程与 LLM Wiki 理念高度相通——都强调知识编译一次、持续复用。核心洞察是 AI 编码质量上限取决于喂给它的上下文物料，而非模型本身能力

## [2026-04-07] 摄入 | Karpathy 知识库「LLM Wiki」火爆全网

- 来源：机器之心知乎文章（2026-04-05）
- 创建页面：
  - `来源_Karpathy知识库LLM Wiki火爆全网.md`（来源摘要）
  - `LLM Wiki.md`（概念页）
  - `RAG.md`（概念页）
  - `元框架.md`（概念页）
  - `Andrej Karpathy.md`（实体页）
  - `Obsidian.md`（实体页）
- 更新页面：`index.md`
- 关键发现：LLM Wiki 是 Karpathy 提出的知识管理元框架，核心在于知识编译一次、持续更新，而非每次查询重新推导

## [2026-04-07] 初始化 | Wiki 创建

- 创建了 wiki 基础结构：`raw/`、`raw/assets/`、`wiki/`
- 创建了 schema 文件 `CLAUDE.md`
- 创建了索引 `wiki/index.md` 和日志 `wiki/log.md`
- wiki 已就绪，等待第一份资料摄入
