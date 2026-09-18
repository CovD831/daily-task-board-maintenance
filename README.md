# daily-task-board-maintenance

维护有既定书写风格的进度表 / 计划表 / 看板（HTML 或 Markdown），外加「**每日对账桥**」：改表前把产出文档里的声称拿到仓库实况（提交/合并事件）校验，再把校验结果落表。

**三层真相链：代码 = 真相；文档 = 声称（不能全信）；表格 = 安排，只落经校验的实况。**

## 什么时候用

- 一张已存在、有既定书写风格的表格要填新行/更新旧行，读者会逐列检查风格一致性。
- 每日产出文档与任务表需要对账（已完成查合并事件 / 可开工查前置与基线 / 阻塞查是否被证伪）。

## 安装

把 `SKILL.md` 拷进你的 agent 技能目录（如 `~/.claude/skills/daily-task-board-maintenance/`，或你所用平台的等价位置）。纯 prompt，零依赖，无脚本、无附属文件。

## 验证

零上下文 A/B 对照（同一 git 仓库、同模型、严格只读）：带技能的代理找出 7 条真实状态失真 + 归因（含「planned 但前置已解除」「已合并 25 分钟后账本仍未回写」两类基线遗漏）；无技能基线仅发现 2 条账本过期，且不做「planned 是否该升 ready」的反向核查。增量可归因到技能内「三类必查」条文。

## 相关

- [skill-mining](https://github.com/CovD831/skill-mining) —— 从项目开发史提取可移植 skill
- 全部技能索引：[agent-skills](https://github.com/CovD831/agent-skills)
