# 在线辅导平台 · 项目说明

## 重要同步规则

**`docs/UX答疑交互.md` 与 `docs/demo-ai-答疑-ipad.html` 必须保持一致。**

- 修改任意一侧（UX 文档或 HTML demo），必须同步更新另一侧。
- UX 文档是交互规范的单一来源，demo 是其可视化实现。


## 开发工作流

**所有任务必须由 main agent 分配给 subagent 完成。**

- Main agent 负责任务分析、文件读取和整体协调
- 实际的代码编写、修复和重构工作交由 subagent 执行
- 复杂任务应先拆解后再分配给 subagent，确保指令清晰明确


## Playwright 验证规范

**使用 Playwright 进行页面验证时，截图仅用于临时验证。**

- 验证完成后，必须删除 `.playwright-mcp/` 目录下的截图文件
- 不要将截图文件提交到版本控制
- 截图仅用于开发和验证阶段，不保留在历史记录中
