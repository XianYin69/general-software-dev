# Scope（范围声明）

本技能（general-software-dev）作为通用软件开发总控，职责边界如下：

## 本体持有（横切环节）

- **编排设计**：项目骨架、目录结构、命名约定、架构分层与接口契约；
- **脚手架搭建**：README/CHANGELOG/LICENSE 基线、配置分层策略；
- **架构决策**：模块边界取舍、依赖方向、跨栈权衡（每岔路走双链辩论）；
- **打包发布**：版本规则意图、产物清单、发布通道选择、门禁口径定义；
- **测试策略**：验收标准输入、覆盖率阈值设定、证据门禁消费；
- **git 远端管理**：分支策略、PR 描述意图、仓库可见性判定（PUBLIC/PRIVATE）。

## 禁止持有（专项实现）

以下能力一律派发至对应专家技能，本体不复制其内容：

- Python/C++/C/前端/数据库专项实现 → python-expert / cpp-expert / c-expert / frontend-dev / database-management
- Web 端到端测试 → webapp-testing
- PR 协作 → pull-request-flow
- 打包发布实体流程 → packaging-and-release（子技能位）
- 测试执行实体流程 → software-testing（子技能位）
- 远端仓库操作实体流程 → git-remote-management（子技能位）

## 判据

**「换个语言栈还成立才留本体」**——凡依赖特定语言/框架的细节归专项技能；
横切环节的抽象规则（流程、门禁、路由、约束）归本体。

## 相关

- [伞形不重复约束](resistance/伞形不重复约束/伞形不重复约束.md)
- [路由派发约束](resistance/路由派发约束/路由派发约束.md)
- [子技能路由](branch/子技能路由/子技能路由.md)
