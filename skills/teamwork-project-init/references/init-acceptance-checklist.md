# 初始化验收清单（项目根目录）

目标：初始化完成后，项目具备“可按流程推进”的最小能力，且文档路径一致、门禁可执行。

## 规则文件

- [ ] 项目根目录存在 AGENTS.md
- [ ] AGENTS.md 包含目录约定：references/、docs/、source/
- [ ] AGENTS.md 的阶段顺序包含：需求→设计→开发→测试→部署
- [ ] AGENTS.md 的默认工作流包含：
  - [ ] docs/requirements/PRD.md
  - [ ] docs/changelog/CHANGELOG.md
  - [ ] docs/design/SPEC.md
  - [ ] docs/testing/TEST_PLAN.md
  - [ ] docs/release/RELEASE.md
  - [ ] docs/decisions/（关键取舍时）
- [ ] AGENTS.md 声明双重确认：AI 自检 + 用户确认
- [ ] AGENTS.md 声明“先文档后代码”门禁
- [ ] AGENTS.md 声明用户点名角色优先级高于自动识别
- [ ] AGENTS.md 包含环境与配置约定（不提交密钥）
- [ ] AGENTS.md 包含启动与运行指引（可先留占位命令）
- [ ] AGENTS.md 包含测试与质量门禁（可先留占位命令）

## 文档骨架

- [ ] docs/requirements/PRD.md 存在
- [ ] docs/changelog/CHANGELOG.md 存在
- [ ] docs/design/SPEC.md 存在
- [ ] docs/testing/TEST_PLAN.md 存在
- [ ] docs/release/RELEASE.md 存在
- [ ] docs/decisions/ADR-0001.md 存在或明确为“按需创建”

## 目录骨架

- [ ] references/ 存在（允许为空）
- [ ] docs/ 存在
- [ ] source/ 存在

## 一致性检查

- [ ] AGENTS.md 中所有文档路径与实际目录一致
- [ ] docs/ 下文档命名与路由规则一致（PRD/SPEC/TEST_PLAN/RELEASE）
- [ ] 若项目已存在 UnoCSS 等样式体系：AGENTS.md 的样式规则已以“遵循项目”为准
