# teamwork-devkit-skills

一套可移植的“团队研发流程化”技能包：用 AGENTS.md 固化研发门禁与目录规范，用多个子技能按阶段推进产物与实现。

## 典型用法

初始化一个新项目：

- “使用 teamwork-dev-entry 初始化项目，并生成 AGENTS.md 和 docs 骨架”

初始化完成后，按阶段推进：

- 需求：更新 docs/requirements/PRD.md
- 方案：更新 docs/design/SPEC.md 与 docs/decisions/
- 测试：更新 docs/testing/TEST_PLAN.md
- 发布：更新 docs/release/RELEASE.md

注意：执行初始化的是在工作空间，不是项目代码目录，避免文件混乱，代码目录单独规划在`source`目录下，可按需组织任意多个仓库

## 在 Claude Code 中使用

- 安装与用法说明：与 Claude 官方 skills 相同

```bash
/plugin marketplace add CoderMonkie/teamwork-devkit-skills
/plugin install teamwork-devkit-skills@teamwork-devkit-skills
```

## 技能清单

- 总入口：skills/teamwork-dev-entry
- 初始化：skills/teamwork-project-init
- 产品：skills/teamwork-product
- 架构：skills/teamwork-architect
- UI/UX：skills/teamwork-uiux-design
- 全栈：skills/teamwork-fullstack
- 测试：skills/teamwork-qa
