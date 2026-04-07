# Super Dev Session Brief

- 动作类型: 开始新流程
- 当前步骤: 先启动研究阶段
- 当前状态: missing_research
- 用户下一步: 先让宿主进入 Super Dev 研究阶段，产出 research 文档。
- 机器侧动作: super-dev start --idea "请在这里填写需求"
- 推荐宿主: Claude Code
- 工作流状态 JSON: D:\github-projects\super-dev\.super-dev\workflow-state.json
- 你现在可以直接说: 做一个 X / 先研究同类产品 / 开始这个项目 / 先把宿主接好
- 自然语言示例: 做一个 X, 先研究同类产品, 开始这个项目
- 宿主第一句: /super-dev "继续当前项目“Super Dev 是一个本地 Python CLI 与宿主规则协同的 AI Coding 治理工具，用 research-first 流水线约束文档冻结、Spec 拆解、前端优先验证、质量门禁和交付证据闭环。”的 Super Dev 流程，不要当作普通聊天。先读取 .super-dev/SESSION_BRIEF.md、.super-dev/workflow-state.json、.super-dev/WORKFLOW.md、output/*、.super-dev/review-state/* 和最近的 tasks.md。当前步骤是“先启动研究阶段”。只要仓库里还有活动的 Super Dev 上下文，后续自然语言需求默认继续当前流程，而不是切回普通聊天。"
- 原因: 当前尚未完成同类产品研究。
- 依据: 缺少 output/*-research.md

## 会话连续性规则
- 只要仓库里还有活动的 Super Dev 上下文，后续自然语言需求默认继续当前流程，而不是切回普通聊天。

## 离开当前流程的唯一条件
- 用户明确说要取消当前流程。
- 用户明确说要重新开始一条新的流程。
- 用户明确说要切回普通聊天，而不是继续 Super Dev。

## 下次回来怎么继续
- 回到项目根目录后，优先执行 `super-dev resume`。
- 如果只想看系统推荐的唯一下一步，也可以执行 `super-dev next`。
