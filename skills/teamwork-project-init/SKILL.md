---
name: teamwork-project-init
description: 初始化一个带研发流程门禁的项目工作区。用户说“初始化项目/创建 AGENTS 规则/立项”或需要落地目录与文档骨架时使用。
---

# teamwork-project-init

你负责把“从立项开始的团队研发规范”落到项目里：生成/更新 AGENTS.md，
并创建文档与目录骨架。优先遵循项目现状；缺省按本技能的约定初始化。

## 目标

- 让用户在第一次对话就得到可执行的 AGENTS.md
- 固化研发流程门禁：先文档，后代码；双重确认
- 目录与产物可追溯：每次迭代能找到 PRD/SPEC/测试计划/变更/发布记录

## 执行步骤

0) 确定目标目录
- 默认在当前项目根目录初始化
- 若用户指定了项目根目录路径，则以用户指定为准

1) 识别是否为新项目
- 新项目：按“默认目录约定”创建骨架
- 既有项目：只补齐缺失文件与关键规则，不强改既有结构

2) 生成或更新规则文件
- 以本技能 assets/AGENTS.md 为基准
- 用用户提供的项目信息替换占位符
- 若已存在 AGENTS.md：做最小差异合并，保留项目已有合理规则
- 若仅存在 AGENT.md：迁移为 AGENTS.md 后再做最小差异合并
- 合并策略：见 references/merge-policy.md
- 初始化验收：见 references/init-acceptance-checklist.md

3) 创建 docs 骨架（若缺失）
- docs/requirements/PRD.md
- docs/requirements/REQUIREMENTS.md（可选但建议预留）
- docs/changelog/CHANGELOG.md
- docs/design/SPEC.md
- docs/decisions/ADR-0001.md（出现关键取舍时才要求维护）
- docs/testing/TEST_PLAN.md
- docs/release/RELEASE.md（发布与部署清单）

4) 创建 workspace 目录（若缺失）
- source/（工程代码）
- references/（历史资料、素材、用户背景输入，只读参考）
  - references/ideas/（初始想法、概念）
  - references/materials/（背景资料、参考文档）
  - references/requirements/（原始需求记录）

5) 写入“本项目偏好”
- UI 样式：默认 TailwindCSS；若项目模板已使用 UnoCSS 等，遵循项目
- 技术栈：不写死；仅记录约束、接口风格、工程边界等不随技术变化的规则

6) 双重确认
- 先自检：规则文件是否包含门禁、目录、产物、角色协作、代码风格约束
- 再请求用户确认：仅在用户确认后才进入下一阶段（需求/设计/开发/测试）

## 默认目录约定（可按项目调整）

- docs/：文档单一来源（本仓库的最新版本）
- source/：工程代码（仅在此目录内改代码）
- references/：历史资料、素材、用户背景输入（只读参考）

## 输出要求

- 输出 AGENTS.md 的完整内容或补丁
- 输出新增文件清单与路径
- 不输出与项目无关的技术栈细节

## 示例

- 用户：使用 teamwork-dev-entry 初始化一个新项目
- 你：创建 references/ docs/ source/，生成规则文件，补齐文档目录骨架
