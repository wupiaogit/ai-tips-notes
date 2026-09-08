# Codex 从入门到精通 · 分章学习笔记

> **说明**：本文是对 [@miles_mazy](https://x.com/miles_mazy) X Article《万字长文｜Codex 从入门到精通》的**结构化学习笔记**（分章摘要与要点），便于检索与对照练习。  
> **非原文全文转载**。完整原文与表述以原帖为准：  
> https://x.com/miles_mazy/status/2091339513134010554  
> 原作者：Miles Ma（@miles_mazy）

---

## 一、Codex 是什么
- 不只是聊天，而是能读写文件、跑命令、看 Git、调工具的 Agent。
- 基本循环：`Prompt → Plan → Execute → Verify`；「完成了」≠ 已验证正确。
- 入口很多（App / CLI / Cloud / IDE / 扩展）：先把当前入口用熟，不必一次全学。

## 二、App 界面三块
- **左**：项目（长期目录）与任务（一次有结束点的对话）。
- **中**：对话 + 控制台（发送/停止/模型/权限/附件/Local·Worktree·Cloud）。
- **右**：Diff 审查（行内评论、暂存撤销、commit/push/PR）。
- 旧任务上下文很脏时，新需求宜新开任务。

## 三、工作区怎么选
- 原则：完成任务所需文件能否收在一个最小目录。
- 独立项目开根目录；多应用可拆多个 Project；只分析用只读；远端执行选 Cloud。
- CLI：`--cd` / `--add-dir` 收窄范围，优于整机放权。

## 四、Local / Worktree / Cloud
- **Local**：直接改当前目录，日常小改最省事。
- **Worktree**：隔离副本，适合并行或怕踩当前分支。
- **Cloud**：远端异步（审查、Issue、批量重构）；强依赖本机时别硬上。

## 五、Plan 怎么用
- 复杂/难回退/要先调查：先 Plan。
- 改标题、查一个报错：不必强行五步计划。
- 好 Plan 要回答：解决什么、看哪些材料、改哪里、如何证明完成。
- 原则：最短可靠路径；能局部改就不推倒重来。

## 六、权限与审批
- 常见档位：只读 → 工作区可写 → 更高权限；多数日常用工作区可写即可。
- 审批时看：命令是什么、在哪执行、要不要网、是否必要。
- `/permissions`；`--full-auto` ≠ 整机开放；`--yolo` 不适合当默认。

## 七、容易忽略的基础能力
- 集成终端（可读终端报错）、In-App Browser（元素评论）、Computer Use（桌面操作）、图片输入/生图、Memory。
- 重要规则仍建议写进 `AGENTS.md`；Memory 更像隐式偏好。

## 八、CLI 常用
- `codex` 进 TUI；常用 `/plan` `/review` `/diff` `/permissions` `/status`。
- `@` 引用文件，`!` 跑 shell；Enter 补充、Tab 排队；`/clear` 清上下文。

## 九、AGENTS.md
- 项目级长期规则：构建、结构、规范、验收、不能做的事。
- `/init` 出初稿再删水分；短而准，从真实翻车补规则。

## 十、Skills / Plugins / MCP
- **Skill**：怎么做一类事（`SKILL.md`）。
- **Plugin**：打包 Skills/MCP/连接器。
- **MCP**：接外部工具与数据。
- 重复才固化 Skill；真需要外部系统再 MCP；整套现成能力再 Plugin。

## 十一、Automations
- 定时/预约任务；先手动跑通同一 Prompt 再无人值守。
- 结果进 Triage；Git 仓库用 Worktree 更稳。

## 十二、/goal vs Plan vs Automation
- `/goal`：跨会话长期目标（要有可验证完成标准）。
- Plan：单次执行前路线。
- Automation：闹钟/定时唤醒。
- Skill=手册，Plugin=能力包，MCP=接口，Automation=闹钟，/goal=长期状态。

## 十三、0→1 学习顺序
1. 选对工作区 + 新建任务 + 控权限 + 会看 Diff  
2. Plan + 终端 + `/review`  
3. Worktree / 并行（有真实需要再开）  
4. 按需装 Skill / MCP / Plugin / Automation / `/goal`  
分水岭：给对材料与范围、执行中纠偏、用 Diff/测试/页面验收，而不是只听「已完成」。

---

## 延伸
- 原帖（请直接阅读全文）：https://x.com/miles_mazy/status/2091339513134010554
- 本地干货索引稿：`ganhuo` 侧对应 `2026-09-08-1422-01-miles-mazy-codex-guide.md`
