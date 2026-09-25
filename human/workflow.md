# GitHub 工作流

方法论在 GitHub 上的运行方式。核心转变：**上下文进仓库，会话是一次性执行器**——会话可以中断，工作不丢。

## 原语映射

| GitHub | 方法论 |
|---|---|
| Issue | 定义（计划，人 → Agent） |
| Branch + Worktree | 执行隔离 |
| CI / 检查 | 机器反馈 |
| PR 描述 | 交付物（Agent → 人） |
| Review Agent | REVIEW 独立证伪 |
| 人的 PR review | 批量验收 |
| Merge / Close | 结论 PASS / FAIL |

## 规则

1. 一个 Issue 一个 worktree 一个分支一个 PR；分支名 `N-slug`（N 为 issue 号）。
2. Issue 可派发的标准：plan 模板字段齐全，尤其验收标准。不齐 = 探索态，不进执行队列；依赖未合并的 issue 标注依赖并视为 blocked，不派发。
3. 反馈顺序固定：**CI → review agent → 人**。前一层未过不进下一层；人只 review CI 全绿且 review agent 已过的 PR。
4. Review agent 是过滤器，不是守门员：发现按严重级标注，执行 Agent 逐条回应（修复 / 说明 / 反驳），分歧项上升给人；merge 决定永远是人。
5. Agent 执行期间开 Draft PR：进度可见，不产生完成通知；验收窗口之外人不点开。
6. 在办 PR 数不超过下一个验收窗口的容量。
7. 探索不进 PR：探索产物留在 worktree 或任务档案的 `explore/`，PR 只装确定产物。
8. 快速通道：单文件、无逻辑变更、Agent 自验通过的改动可直提 main，事后补一行记录；其余一律走完整流程。
9. 会话只做执行：进入会话先读 Issue 与任务档案，产出全部写入 PR 与档案，不依赖会话记忆。

---

v0.1
