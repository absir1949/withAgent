# 计划：注意力杠杆目标函数

- **Goal**：把本轮讨论收敛的目标函数落进方法论文档：Attention Leverage 为第一性目标，机器劳动杠杆降为方法层；观察指标同步扩充
- **Non-goals**：不新增文档；不改四条核心原则主体；不动 workflow.md 与 archive.md；不展开成论文（保持压缩文风）
- **Scope**：philosophy/philosophy.md；human/protocol.md；agent/conduct.md；README.md；本任务档案
- **Constraints**：路径英文 kebab-case；各文档独立版本号；每处改动可追溯到已确认的讨论结论
- **Dependencies**：无
- **Acceptance Criteria**：
  1. philosophy.md 目标函数更新为新表述，且包含：优先级倒置（机器时间/Token 为二级成本）、「有效=被验证过」（防 Goodhart）、注意力一部分是投资（防饿死判断力）、目标→方法→机制→基础设施分层
  2. philosophy.md 二级推论新增「注意力构成」与「可行集扩大」两条；反馈闭环含「被验证者不得同时是验证者」；探索购买信息含「产出为人的注意力设计」的表述
  3. protocol.md 观察指标新增「注意力构成」「验收后返工」，与总比值方向对齐，保留「记录不考核」定位
  4. conduct.md「不得修改验收规则」补充信任不变量理由，行为规则本身零改动
  5. README.md 核心主张与观察指标清单同步
  6. 任务档案四件套齐全，格式与既有档案一致
- **Verification**：git diff 逐条对照 AC；独立上下文 REVIEW 证伪；无中文路径
