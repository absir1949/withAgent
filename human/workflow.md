# GitHub 工作流

方法论在 GitHub 上的运行方式。核心转变：**上下文进仓库，会话是一次性执行器**——会话可以中断，工作不丢；人管理 Goal，不管理 Agent。

## 原语映射

| GitHub | 方法论 |
|---|---|
| Issue | Goal 的持久载体 |
| Branch + Worktree | 执行隔离 |
| CI / 检查 | 机器反馈 |
| PR 描述 | 交付物（Agent → 人） |
| Review Agent | REVIEW 独立证伪 |
| 人的 PR review | 批量验收 |
| Merge / Close | 结论 PASS / FAIL |

## Issue 生命周期

`EXPLORE → READY → EXECUTING → REVIEW → DONE`

- `EXPLORE`：Goal 已立，定义未齐。
- `READY`：plan 字段齐全，可派发。
- `EXECUTING`：Agent 已领取，对应 Draft PR。
- `REVIEW`：PR 就绪，进入 CI → review agent → 人。
- `DONE`：人验收合并。
- 依赖未满足的 Issue 标注 `BLOCKED`，不派发。

状态机分工：**人定义规则并做最终决策，Agent 运行状态机。**

人只在三个节点出手——定义中的价值确认、Review 中的最终验收、`DONE`；其余流转由 Agent 维护，人不维护看板。

## 规则

1. 一个 Issue 一个 worktree 一个分支一个 PR；分支名 `N-slug`（N 为 issue 号）。
2. 反馈顺序固定：**CI → review agent → 人**。前一层未过不进下一层；人只 review CI 全绿且 review agent 已过的 PR。
3. Review agent 是过滤器，不是守门员：输出强制压缩——`PASS`，或 `FAIL` + 按严重级标注的问题 + 证据 + 仅剩需人判断的分歧；不写长报告。merge 决定永远是人。
4. 只记录、不考核两个观察项：人发现而机器本应发现的问题数；人的 review 耗时。
5. Agent 执行期间开 Draft PR：进度可见，不产生完成通知；验收窗口之外人不点开。
6. 在办 PR 数不超过下一个验收窗口的容量。
7. 探索不进 PR：探索产物留在 worktree 或任务档案的 `explore/`，PR 只装确定产物。
8. 会话只做执行：进入会话先读 Issue 与任务档案，产出全部写入 PR 与档案，不依赖会话记忆。

---

v0.1
