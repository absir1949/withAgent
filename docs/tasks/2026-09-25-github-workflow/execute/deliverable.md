# 交付物

- **改动摘要**：新增 `human/workflow.md`（v0.1：映射表 + 9 条规则）；新增 `.github/ISSUE_TEMPLATE/plan.md` 与 `.github/PULL_REQUEST_TEMPLATE.md`；`agent/archive.md` 新增第 14 条「GitHub 模式」；README 文档表增至五篇并新增 GitHub 用法段
- **验证结果**：README 全部链接 test -f 通过；Issue 模板字段 = templates/plan.md，PR 模板字段 = templates/deliverable.md；workflow 规则与协议（批次、并发、前置条件）、守则（REVIEW 独立证伪）、档案（探索不进 PR）术语一致
- **不确定点**：快速通道「单文件」门槛对文档类改动是否过严；review agent 分歧上升机制依赖具体工具能力，v0.1 只定义了原则
- **决策记录**：规范放 human/（协议的 GitHub 实现）而非 agent/；不双轨全记，避免定义/交付物重复维护
- **重点验收项**：九条规则是否够用；反馈顺序 CI → review agent → 人是否认可
- **最短验收路径**：读 `human/workflow.md`（约 1 分钟），扫一眼两个 .github 模板
