# 2026 后端 × Agent 真实面经种子库（20 份归档 + ASu-skills 训练入口）

> **定位一句话说明白**：这里存档了 **20 份 2026 年 5 月—11 月真实大厂与垂类团队一面至三面面经**（10 份后端偏向 + 10 份 Agent 偏向，暂不含全栈），把每道真实考题拆成了新手能听懂的大白话逻辑链，并直接对接 [asu-training-seed.md](asu-training-seed.md)，让你可以随时调用 `/asu-skills` 的 `/interview` 模拟面试和 `/job-match` 岗位匹配开练。

## 一、构建原则与事实边界

1. **真实聚焦，不做全栈**：严格挑选 2026 年最新发布的 10 份后端面经（`B01`–`B10`）和 10 份 Agent 面经（`A01`–`A10`），覆盖字节跳动、拼多多、美团、腾讯、京东、百度、快手、VIVO、作业帮、携程、九方智投等十余个真实业务团队。
2. **正视重叠现实**：2026 年真实招聘中，后端岗高频追问 Agent 超时、断点续跑、MCP/Skill、对话存储分层；Agent 岗同样深挖分布式锁、租约与 Fencing Token、数据库状态机与流式断线重连——归档时特意保留了这批真实交叉样本。
3. **忠于原帖、拒绝编造**：每篇归档的「真实面试题清单」均严格对照已抓取网页原文整理；映射 Twenty CRM 时明确划清 **项目已有证据 / 部分证据 / 无证据（真实缺口）/ 待确认（未实测数字）** 四条线，绝不替你虚构线上 QPS 或个人职责。

---

## 二、20 份面经完整总索引

### A. 后端偏向面经（10 份：`B01`–`B10`）

| 编号 | 方向细分 | 公司 · 岗位与轮次 | 日期 | 原题规模 | 核心考点标签 | 原文链接 | 归档文件 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `B01` | 后端核心 | 字节跳动 · 中国交易与广告 · 后端一面 | `2026-11` | 47 题 | Redis Key/版本回源、异步日志/P99、慢 SQL/MVCC、双层限流 | [原文](https://mj.mianlingai.com/interview/bytedance-backend-first-2942591/) | [B01 字节交易广告一面](backend/B01-字节跳动-中国交易与广告-后端一面.md) |
| `B02` | 后端核心 | 字节跳动 · 后端一面（实时链路与容错） | `2026-11` | 16 题 | NATS vs Kafka、下游超时回查幂等、实时链路去重、ClickHouse 预聚合、对账回补 | [原文](https://mj.mianlingai.com/interview/bytedance-backend-first-2942398/) | [B02 字节实时链路一面](backend/B02-字节跳动-实时链路与下游容错-后端一面.md) |
| `B03` | 后端×Agent重叠 | 字节跳动 · 后端/Agent 开发三面 | `2026-11` | 35 题 | 业务本体建模 vs CLI+Skill、Action 粒度、指标口径基线、个人与导师边界 | [原文](https://mj.mianlingai.com/interview/bytedance-backend-agent-2940785/) | [B03 字节后端Agent三面](backend/B03-字节跳动-后端与Agent重叠-三面.md) |
| `B04` | 后端×Agent重叠 | 拼多多 · 提前批 · 后端一面 | `2026-11` | 4 大组 | Agent/LLM 超时分层与写工具防重、MQ 顺序重复丢失、缓存一致性窗口、200ms→5s 排障 | [原文](https://mj.mianlingai.com/interview/pdd-backend-first-953964865771577344/) | [B04 拼多多提前批一面](backend/B04-拼多多-提前批-后端一面.md) |
| `B05` | 后端×Agent重叠 | 美团 · 后端开发一面 | `2026-10` | 7 大组 | RabbitMQ 幂等、冷热分层存储与写一致、多 Agent 拆分边界、线程池 7 参数、慢 SQL | [原文](https://mj.mianlingai.com/interview/meituan-backend-first-round-2927252/) | [B05 美团MQ与多Agent一面](backend/B05-美团-MQ幂等与多Agent-后端一面.md) |
| `B06` | 后端×Agent重叠 | 美团 · 后端一面（40 问全链路） | `2026-10` | 40 题 | Agent 断点续跑与防串位、确认后走代码、binlog 对账与 MQ 积压、双跑影子写、本地消息表 | [原文](https://mj.mianlingai.com/interview/meituan-backend-first-round-2932014/) | [B06 美团断点续跑与对账](backend/B06-美团-断点续跑与对账重构-后端一面.md) |
| `B07` | 后端核心 | 腾讯 · 瑞驰 · 后端开发一面 | `2026-11` | 12 题 | 联合索引失效、B+树 vs 内存红黑树陷阱、Hash-Flooding、系统扩展边界、LCA 四连 | [原文](https://mj.mianlingai.com/interview/tencent-ruichi-backend-first-round-946488757283303424/) | [B07 腾讯瑞驰一面](backend/B07-腾讯瑞驰-数据库索引与数据结构-后端一面.md) |
| `B08` | 后端×Agent重叠 | 京东 · 后端开发一面 | `2026-10` | 15 题 | Redis/MySQL 会话分层、Recall 偏低排查、防开卷作弊评测、中间件选型三步法 | [原文](https://mj.mianlingai.com/interview/jd-backend-2931603/) | [B08 京东会话分层一面](backend/B08-京东-会话分层与评测取舍-后端一面.md) |
| `B09` | 后端×Agent重叠 | 百度 · 后端开发一面（含 Agent） | `2026-11` | 16 题 | MCP 工具发现、Skill 渐进式披露、MVCC 与主从延迟、Redis Lua 防超卖、长时间不一致 | [原文](https://mj.mianlingai.com/interview/baidu-backend-agent-2935881/) | [B09 百度MCP与缓存一面](backend/B09-百度-MCP与Redis一致性-后端一面.md) |
| `B10` | 后端×Agent重叠 | 某互联网公司 · 投递平台后端二面 | `2026-11` | 39 题 | 12.4s→650ms 异步拆解、Kafka 位点陷阱、Redis 锁粒度与唯一索引、SHA256 去重、混合检索归因 | [原文](https://mj.mianlingai.com/interview/company-backend-2937972/) | [B10 投递平台二面](backend/B10-某互联网公司-投递平台异步与检索-后端二面.md) |

### B. Agent 偏向面经（10 份：`A01`–`A10`）

| 编号 | 方向细分 | 公司 · 岗位与轮次 | 日期 | 原题规模 | 核心考点标签 | 原文链接 | 归档文件 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `A01` | Agent核心 | 字节跳动 · 抖音电商 · Agent 一面 | `2026-10` | 36 题 | 50MB 大输出外置落地、Harness 骨架、Planner/Executor、沙箱防注入、日 10 万并发估算 | [原文](https://mj.mianlingai.com/interview/bytedance-agent-development-first-round-939623386806751232/) | [A01 抖音电商Agent一面](agent/A01-字节跳动-抖音电商-Agent开发一面.md) |
| `A02` | Agent×后端重叠 | 字节跳动 · 飞连 · AI Agent 二面 | `2026-05` | 17 题 | Workflow vs LLM 边界、Tool 服务端分发、Bad Case 与反思污染、Redis Stream vs Kafka | [原文](https://developer.cloud.tencent.com/article/2673729) | [A02 飞连Agent二面](agent/A02-字节跳动-飞连-Agent开发二面.md) |
| `A03` | Agent×后端重叠 | 字节跳动 · 火山引擎 · Agent 秋招一面 | `2026-10` | 22 题 | 不用 MQ 设计异步系统、Skills 全链路与传统开发差异、OS/TCP/429 幂等、Redis/MQ 积压 | [原文](https://mj.mianlingai.com/interview/bytedance-volcano-engine-agent-autumn-first-round-2923108/) | [A03 火山引擎Agent一面](agent/A03-字节跳动-火山引擎-Agent秋招一面.md) |
| `A04` | Agent核心 | 某公司 · Claude Code 二开与 Harness 一面 | `2026-11` | 9 题 | Claude Code 二开、Goal Loop 评测、多 Worker 并发写隔离、四层记忆压缩由 Harness 触发 | [原文](https://mj.mianlingai.com/interview/company-agent-development-2939011/) | [A04 Harness二开一面](agent/A04-某公司-ClaudeCode二开与Harness-Agent一面.md) |
| `A05` | Agent×后端重叠 | 快手 · 大模型 Agent 研发一面 | `2026-09` | 20 题 | Reconcile 恢复、Lease 租约过期、Fencing Token 存储校验、多 Agent 评测、目录防注入 | [原文](https://mj.mianlingai.com/interview/kuaishou-agent-dev-first-round-932315325276618752/) | [A05 快手Reconcile一面](agent/A05-快手-Reconcile租约与多Agent-Agent一面.md) |
| `A06` | Agent核心 | 快手 · Agent 开发一面 | `2026-09` | 6 题 | 工具失败五层兜底、共享黑板流水线、上下文三档压缩保硬字段、手撕流式 JSON 半包粘包 | [原文](https://mj.mianlingai.com/interview/kuaishou-agent-first-round-931679347587444736/) | [A06 快手流式与兜底一面](agent/A06-快手-工具兜底与流式解析-Agent一面.md) |
| `A07` | Agent核心 | VIVO · Agent 开发秋招一面 | `2026-09` | 9 题 | 超时「结果未知」态、换强模型退化、防注入策略层、TOCTOU 竞态、消融证明运行时收益 | [原文](https://mj.mianlingai.com/interview/vivo-agent-932565368587976704/) | [A07 VIVO状态机与安全](agent/A07-VIVO-运行时状态机与安全防线-Agent一面.md) |
| `A08` | Agent×后端重叠 | 作业帮 · Agent 开发一面 | `2026-09` | 14 题 | 流式断线重连游标补发、工具幂等唯一索引、Trace 回流迭代、硬指标+Judge 分层评测 | [原文](https://mj.mianlingai.com/interview/zuoyebang-agent-dev-first-round-2916240/) | [A08 作业帮评测与重连](agent/A08-作业帮-评测体系与断线重连-Agent一面.md) |
| `A09` | Agent核心 | 携程 · Agent 开发一面 | `2026-09` | 10 题 | LangGraph 有环图与 Reducer、Checkpoint 非确定性坑、知识图谱多跳 RAG、首 Token 延迟 | [原文](https://mj.mianlingai.com/interview/ctrip-agent-dev-first-round-2916102/) | [A09 携程LangGraph与图谱](agent/A09-携程-LangGraph与图谱RAG-Agent一面.md) |
| `A10` | Agent×后端重叠 | 九方智投 · Agent 开发一面 | `2026-09` | 19 题 | 标题切块不均解法、RRF 倒数融合、MCP 四层权限控制、HITL 防过度弹窗、Java/Redis 八股 | [原文](https://mj.mianlingai.com/interview/jiufangzhitou-agent-dev-first-round-2916834/) | [A10 九方智投MCP权限](agent/A10-九方智投-RAG切块与MCP权限-Agent一面.md) |

---

## 三、跨 20 份面经高频考点统计（看清真实考场分布）

| 象限 | 高频考点群 | 命中面经篇数 | 涉及面经编号 | 大白话一句话考点精髓 |
| :--- | :--- | :---: | :--- | :--- |
| **纯后端地基** | 数据库索引失效、B+ 树底层、MVCC 与慢 SQL 排查 | **6 篇** | `B01` `B05` `B07` `B09` `A03` `A10` | 查慢 SQL 别瞎猜，先分段再看执行计划；磁盘用 B+ 树省寻页次数，内存未必输 |
| **纯后端地基** | Redis 缓存架构（Key/版本回源、一致性、Lua 原子、持久化） | **8 篇** | `B01` `B04` `B06` `B08` `B09` `A02` `A03` `A10` | 缓存讲清失效窗口与漏删排查；原子扣减用 Lua，但最终账本仍以 DB 为准 |
| **纯后端地基** | 并发、限流与线上 RT/CPU 故障排查 | **6 篇** | `B01` `B04` `B05` `B06` `B10` `A03` | 入口+资源双层限流；接口飙到 5s 先定范围、再分段耗时、再看火焰图或等下游 |
| **后端×Agent重叠黄金区** | **超时预算、写工具幂等与「结果未知」回查** | **9 篇** | `B02` `B04` `B05` `B06` `B10` `A01` `A02` `A06` `A07` `A08` | 超时只代表没等到回执，写操作必须凭幂等键先查再重或进未知态，严禁盲重试 |
| **后端×Agent重叠黄金区** | **消息队列（顺序/位点/积压）与无 MQ 异步状态机** | **7 篇** | `B02` `B04` `B05` `B06` `B10` `A02` `A03` | 队列位点不等于业务完成；DB 任务状态机 + 幂等唯一键才是断点恢复底牌 |
| **后端×Agent重叠黄金区** | **断点续跑、流式断线重连与分布式抢占（CAS/Lease/Fencing）** | **6 篇** | `B06` `A01` `A05` `A07` `A08` `A09` | 消息先落库带序号再推；多实例接管靠租约+心跳+存储端校验版本号防覆写 |
| **后端×Agent重叠黄金区** | **MCP 协议、Skill 渐进式披露、Workflow vs LLM 边界** | **6 篇** | `B03` `B09` `A01` `A02` `A03` `A10` | 确定性逻辑归代码工作流，工具按需渐进加载，权限死守在服务端不能靠提示词 |
| **后端×Agent重叠黄金区** | **评测闭环、指标基线口径与 Trace 归因** | **10 篇** | `B03` `B05` `B08` `A01` `A02` `A04` `A05` `A06` `A07` `A08` `A09` | 硬指标一票否决 + Judge 软打分 + 留出集防作弊，所有提升数字必须报清基线和样本 |
| **Agent 专属深化区** | **上下文防爆（50MB 大输出溢写）、压缩触发与长期记忆** | **7 篇** | `A01` `A02` `A04` `A05` `A06` `A09` `B08` | 50MB 数据不进窗口直接写文件留句柄查询；压缩由 Harness 触发且硬字段单列 |
| **Agent 专属深化区** | **向量 RAG 切块、混合检索（BM25+Vector+RRF+图谱）与多 Agent 协作** | **9 篇** | `B05` `B08` `B09` `B10` `A01` `A02` `A04` `A05` `A09` `A10` | Twenty CRM 当前**真实缺口区**，面试要诚实划界并用场景题方法论兜底 |

---

## 四、`/asu-skills` 快速启动指南

本种子库已按 `/asu-skills` 规范完成结构化预处理，你可以直接复制以下任意指令开启训练或规划：

1. **直接开启「后端 × Agent 混合训练模拟面」（推荐新手默认）**
   > `读取 面经种子库/asu-training-seed.md，按 Contract-3 和 immediate 反馈模式，执行 /interview grill 开始模拟面试，每次只问我一题。`
2. **专项压力面：只练 Twenty CRM 最容易被问穿的高风险点**
   > `读取 面经种子库/asu-training-seed.md 的高风险 Claim 清单和 B03/B04/A01/A07/A08，用 /interview grill 对我进行 deferred 模式压力面，重点追问真实边界和 50MB/断线续跑/缓存一致性。`
3. **对照目标岗位 JD 做差距体检**
   > `用 /job-match 对照这份真实面经种子库中的 20 项岗位能力矩阵和 [我贴上的目标 JD]，告诉我 Twenty 项目已经覆盖哪些、哪些属于真实缺口需要补二开或转场景题回答。`
4. **用这 20 份面经反哺重构 Twenty 教程（下一步计划）**
   > `基于 面经种子库/README.md 的统计分布和 asu-training-seed.md 第八部分建议，用 /project-guide 重新规划并升级 Twenty 后端与 Agent 教程，暂不写全栈。`
