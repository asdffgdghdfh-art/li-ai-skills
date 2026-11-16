# 个人 AI 技能库

这是一个面向个人 AI 助手的可复用技能仓库。所有面向使用者的说明、规则、示例和模板默认使用简体中文；技能目录名和元数据中的 name 使用小写英文与连字符，以兼容 Agent Skills 标准。

## 当前技能组

| 技能 | 中文名称 | 用途 |
|---|---|---|
| academic-paper-writing | 学术论文写作 | 在研究结果完成后，组织、撰写、润色、审查和准备投稿学术论文 |
| learning-router | 学习总调度 | 判断学习目的并选择合适的教学模式 |
| concept-explainer | 概念讲解 | 用简短、准确的方式解释概念 |
| exam-prep | 应试备考 | 考点梳理、答题方法、练习与错题复盘 |
| problem-solving | 解题训练 | 分析题目、推导解法、检查答案 |
| socratic-tutor | 启发式教学 | 通过循序渐进的问题帮助学习者自己理解 |
| learning-coach | 学习教练 | 制定计划、追踪进度、主动回忆与间隔复习 |

## 目录

    skills/
      academic-paper-writing/
        SKILL.md
        references/
          prompt-library.md
          control-theory-writing-guide.md
        templates/
          paper-writing-brief.md
          claim-evidence-matrix.md
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

## 在 CC Switch 中添加

1. 打开「技能」页面，进入「管理技能仓库」。
2. 仓库 URL 填写 asdffgdghdfh-art/li-ai-skills。
3. 分支填写 main。
4. 如果界面提供「技能路径」字段，填写 skills；如果没有该字段，留空并重新读取仓库。
5. 在「发现」页面刷新仓库，应该能看到 7 个技能。
6. 选择要启用的应用，再安装所需技能。建议按实际任务启用，不必让所有技能同时参与每次对话。

## 学术论文写作技能

学术论文写作技能的定位是：在定理证明、仿真或实验结果已经完成或基本闭合后，把研究成果转化为规范的学术论文。

配套资料：
- 30 个论文写作提示词：skills/academic-paper-writing/references/prompt-library.md
- 控制理论与网络化控制论文指南：skills/academic-paper-writing/references/control-theory-writing-guide.md
- 论文写作任务单：skills/academic-paper-writing/templates/paper-writing-brief.md
- 论断与证据核对表：skills/academic-paper-writing/templates/claim-evidence-matrix.md

该技能不会凭空生成定理、证明、数据或文献；会检查数学条件、公式符号、论断强度和证据一致性。

## 使用建议

- 一般学习请求：启用「学习总调度」。
- 希望不同教学方式可独立调用：按需启用对应的专项学习技能。
- 论文写作、润色、审稿或投稿：启用「学术论文写作」。
- 同一个任务不需要同时调用所有技能；由当前任务决定最合适的技能。

## 语言约定

- 面向使用者的说明、教学规则、示例和文档默认使用简体中文。
- 必要的英文专业术语首次出现时附中文解释。
- 论文正文使用中文还是英文，以用户要求和目标期刊要求为准。

## 版本原则

- 新增能力时优先新增或扩展对应技能，不随意覆盖其他技能的职责。
- 重要修改记录在 CHANGELOG.md。
- 保留 Git 历史，便于回退和比较。
- 技能文件只提供工作方法，不会自动获得外部工具、自动提醒或跨应用共享记忆。
