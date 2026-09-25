# GitHub 工作流规范

- **状态**：PASS（2026-09-25 验收）
- **时间线**：
  - 2026-09-25 定义：确定 Issue / Worktree / PR + Review Agent 工作方式的 v0.1 规范
  - 2026-09-25 执行：新增 `human/workflow.md`；`.github/` 下内置 Issue 与 PR 模板；档案规则新增第 14 条（GitHub 模式）；README 接入第五篇
  - 2026-09-25 验收：PASS
- **决策记录**：
  - Issue 承载定义与结论、PR 描述承载交付物、任务目录只留 explore 与大附件（不双轨全记）
  - 反馈顺序固定：CI → review agent → 人；merge 决定永远是人
  - 快速通道门槛：单文件、无逻辑变更、Agent 自验通过
