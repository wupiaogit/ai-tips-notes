# Claude Code 实用指南 · 中文摘要

> **说明**：本文是对英文仓库 [wesammustafa/Claude-Code-Everything-You-Need-to-Know](https://github.com/wesammustafa/Claude-Code-Everything-You-Need-to-Know) 的**结构化中文摘要**（路径指引与要点），便于快速上手。  
> **非原文全文翻译**。细节、示例与版本更新以原仓库为准。  
> 收录来源帖：https://x.com/bkdgiffug/status/2092033210914123874

---

## 这是什么
- Anthropic 官方 CLI：在终端里读仓库、改文件、跑命令、提交与开 PR。
- 相对聊天 UI：能读真实仓库上下文、就地编辑并跑测试、与 git/shell/MCP 组合。

## 安装与登录
```bash
npm install -g @anthropic-ai/claude-code   # 需 Node.js 18+
claude                                     # 启动并完成鉴权
```

## 怎么选学习路径
| 你是… | 建议顺序 |
|---|---|
| 新手 | Setup → Prompt Engineering → 第一个 Skill |
| 已在用、要加深 | Skills · Hooks · MCP |
| 要多 Agent / 自动化 | Dynamic Workflows · Agent Teams · BMAD |

## 五个扩展点（何时用）
| 工具 | 何时用 | 跳过条件 | 位置 |
|---|---|---|---|
| **Skills**（斜杠命令） | 同一提示/流程重复 ≥3 次 | 一次性任务 | `.claude/commands/*.md` |
| **Hooks** | 希望在工具调用/会话开始等时**自动**跑代码 | 只要手动触发 | `.claude/settings.json` |
| **Subagents** | 子任务大到需要独立上下文 | 主会话就能做完 | `.claude/agents/*.md` |
| **Workflows** | 需要协调的 Agent 超过单会话能管 | 两三个 subagent 就够 | `.claude/workflows/*.js` |
| **MCP servers** | 要接浏览器/DB/API 等外部工具 | 数据都在本地文件 | 按项目配置 |

> 多数成熟配置会组合其中 2–3 个。

## 模型怎么挑（摘要页仅记选型原则；具体价目以原仓库为准）
- **日常编码**：默认 Sonnet 档。
- **复杂推理 / 大重构 / 编排 Agent**：Opus 档。
- **极难问题**：更高阶 Mythos-class（若原仓库仍列出）。
- **轻量快问**：Haiku 档。

## 仓库里还有什么（按目录意图）
- 基础：Claude Code 是什么、Setup、提示工程。
- 工作流扩展：Slash Commands、Skills、Hooks。
- 多 Agent 与集成：Subagents、Dynamic Workflows、Agent Teams、MCP。
- 生产力与框架：Effort levels、Fast Mode、Super Claude、BMAD。
- 参考：斜杠命令速查、FAQ、更新与弃用说明。

## 可跟做的最小闭环
1. 安装并 `claude` 登录。
2. 在真实项目里让它解释代码库、修一个失败测试、开 PR。
3. 把重复 ≥3 次的流程写成 Skill；需要自动门禁再加 Hook；需要外接工具再加 MCP。

## 原文
https://github.com/wesammustafa/Claude-Code-Everything-You-Need-to-Know
