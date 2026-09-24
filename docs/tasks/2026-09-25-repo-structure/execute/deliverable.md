# 交付物

- **改动摘要**：四篇文档迁移至 philosophy/philosophy.md、human/protocol.md、agent/conduct.md、agent/archive.md（git mv 保留历史）；新增 templates/（plan / deliverable / verdict）；README 重写（新增仓库结构节，全部链接更新）；档案规则第 5 条加入模板指引；新增本任务档案；lessons.md 回填结构经验
- **验证结果**：README 中 7 个链接逐一 test -f 通过；git status 全部为 R（rename）；模板字段与守则 DEFINE 定义、协议交付物清单、档案 verdict 三种结论一一对应
- **不确定点**：philosophy 作为第一层名称是否合意（备选 thinking/）；conduct 作为「守则」译名（备选 rules/）
- **决策记录**：templates/ 放顶层而非 agent/ 下（plan 模板是写给人的）
- **重点验收项**：三层划分与命名；README 新结构
- **最短验收路径**：看本 README「仓库结构」节 + `ls philosophy human agent templates`
