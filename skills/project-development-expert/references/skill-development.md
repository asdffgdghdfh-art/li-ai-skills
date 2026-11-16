# Agent Skill 开发规范

## 1. 设计前检查

- 阅读仓库 README、SKILL_INDEX 和 CHANGELOG。
- 搜索相近 Skill，确定复用、扩展还是新建。
- 明确目标用户、触发条件、输入材料、交付结果和职责边界。
- 不把单次任务提示词包装成 Skill；Skill 应提供可重复执行的工作流程。

## 2. 推荐目录结构

```text
skills/<skill-name>/
  SKILL.md
  references/
    domain-guide.md
    workflow.md
  templates/
    example-template.md
  tests/
    acceptance-scenarios.md
```

按实际需要创建，不为凑目录而创建空文件。

## 3. SKILL.md 必须包含

- YAML frontmatter：name、description；可选 metadata.version、language、author。
- 角色定位与核心职责。
- 适用场景和不适用场景。
- 输入与输出要求。
- 工作流程。
- 关键规则、边界和安全约束。
- 工具使用条件及能力限制。
- 结果验证方式。
- 必要的 references / templates 链接。

description 应说明何时使用，避免写成泛泛的宣传语。

## 4. 内容质量

- 主文件优先写可执行规则，不堆叠背景知识。
- 说明触发条件、优先级、前置检查和失败处理。
- 对关键步骤写出完成标准和证据要求。
- 对需要用户批准的操作写清楚批准边界。
- 不假设 Skill 自动拥有文件、网络、数据库、终端或后台权限。
- 避免依赖某一家模型的隐藏能力，保持跨 Agent 可读。
- 默认中文说明，保留必要的英文标准字段名和命令。

## 5. Skill 测试

至少检查：
- 触发条件是否准确。
- 是否能识别已有项目和历史任务。
- 是否会覆盖未完成任务。
- 是否保留目标变更历史。
- 是否区分已完成、未验证和被阻塞。
- 工具不可用时是否如实说明。
- 是否能交接给另一个 Agent。
- 是否不会越权执行删除、部署、合并或付费操作。

## 6. 发布与同步

- 变更前检查 Git 状态和已有文件。
- 在独立分支完成新增或修改。
- 更新索引、README、CHANGELOG 和版本号。
- 检查引用路径和文件是否存在。
- 通过 PR 提供审查，不自动合并。
- 合并后再让 Codex / CC Switch 刷新技能仓库。
- ChatGPT、Codex 和其他 Agent 的安装状态分别验证；仓库有文件不代表所有平台已同步。

## 7. 公开仓库注意事项

如果技能仓库是公开的：
- 不写入 API Key、Token、密码、私有地址或个人敏感信息。
- 不写入用户的 Notion 私有页面 ID、数据库 ID 或个人工作记录。
- 将通用规则保存在 Skill，将用户专属项目状态保存在私有项目数据库。
- 示例数据使用虚构或脱敏内容。
