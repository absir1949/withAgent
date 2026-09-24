# 计划：仓库分层重构

- **Goal**：仓库结构按受众分层并支持持续扩充，全部路径改为英文
- **Non-goals**：不改动四篇文档的正文内容
- **Scope**：目录结构调整与文件改名；README 重写；新增 templates/；新增本任务档案
- **Constraints**：路径一律英文 kebab-case；中文标题保留在文内首行；git 历史保留（用 git mv）
- **Acceptance Criteria**：
  1. 根目录无平铺内容文档，四篇分别位于 philosophy/ human/ agent/
  2. README 所有链接可达
  3. templates/ 三个模板与守则、档案定义的字段一致
- **Verification**：git status 显示 rename 而非 delete+add；README 链接逐一检查存在
