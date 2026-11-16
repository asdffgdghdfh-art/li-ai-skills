# 个人 AI 技能库

这是一个面向个人 AI 助手的可复用技能仓库。当前优先建设「学习专家」技能组。

## 语言约定

- 面向使用者的说明、教学规则、示例和文档默认使用简体中文。
- 为兼容 Agent Skills 标准，技能目录名和 `SKILL.md` 元数据中的 `name` 使用小写英文与连字符。
- 必要的英文专业术语首次出现时附中文解释。

## 当前技能组

| 技能 | 中文名称 | 用途 |
|---|---|---|
| `learning-router` | 学习总调度 | 判断学习目的并选择合适的教学模式 |
| `concept-explainer` | 概念讲解 | 用简短、准确的方式解释概念 |
| `exam-prep` | 应试备考 | 考点梳理、答题方法、练习与错题复盘 |
| `problem-solving` | 解题训练 | 分析题目、推导解法、检查答案 |
| `socratic-tutor` | 启发式教学 | 通过循序渐进的问题帮助学习者自己理解 |
| `learning-coach` | 学习教练 | 制定计划、追踪进度、主动回忆与间隔复习 |

## 目录

```text
skills/
  learning-router/
    SKILL.md
  concept-explainer/
    SKILL.md
  exam-prep/
    SKILL.md
  problem-solving/
    SKILL.md
  socratic-tutor/
    SKILL.md
  learning-coach/
    SKILL.md
templates/
  学习进度卡.md
  错题卡.md
  知识卡.md
SKILL_INDEX.md
CHANGELOG.md
```

## 在 CC Switch 中添加

1. 打开「技能」页面，进入「管理技能仓库」。
2. 仓库 URL 填写 `asdffgdghdfh-art/li-ai-skills`。
3. 分支填写 `main`。
4. 如果界面提供「技能路径」字段，填写 `skills`；如果没有该字段，留空并重新读取仓库。
5. 在「发现」页面刷新仓库，应该能看到 6 个技能。
6. 选择要启用的应用，再安装所需技能。建议先安装全部 6 个，后续可按应用分别启用。

## 使用建议

- 一般学习请求：启用「学习总调度」。
- 希望不同教学方式可独立调用：同时启用对应的专项技能。
- 同一个问题不需要同时调用所有技能；由学习总调度判断最合适的模式。
- 技能文件只提供工作方法，不会自动获得外部工具、自动提醒或跨应用共享记忆。

## 版本原则

- 新增能力时优先新增或扩展对应技能，不随意覆盖其他技能的职责。
- 重要修改记录在 `CHANGELOG.md`。
- 保留 Git 历史，便于回退和比较。
