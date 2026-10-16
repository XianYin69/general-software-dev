# CHANGELOG
## 0.1.2 2026-10-16
**添加 Scope 节**
- 新增 [Scope.md](Scope.md)：明确本体横切职责（编排/脚手架/架构决策/打包/测试/远端）与禁止持有的专项实现边界；
- [SKILL.md](SKILL.md) frontmatter 版本号 0.1.1→0.1.2，description 追加范围摘要，正文加 Scope 入口链接；
- 动机：响应红线17·批23委托，完善技能范围声明，便于调度方理解本体边界。

## 0.1.1 2026-10-08
**子技能位由占位转实体（伞形接线）**
- `branch/打包发布/`→packaging-and-release、`branch/软件测试/`→software-testing、`branch/git远端管理/`→git-remote-management：只写交接接口与门禁口径，不复制子技能内容（[伞形不重复约束](resistance/伞形不重复约束/伞形不重复约束.md)）；
- `dependence/deps.json` 增三 `local://` 子技能声明（共 12 条，全部实核）；
- `branch/子技能路由/` 路由表增三行：打包发布／测试门禁／远端管理；
- `SKILL.md` 去 `branch/流程/` 去掉「仅占位」口径，版本 0.1.0→0.1.1；
- 三条 `planned_tasks/pt-general-software-dev-gen-*.json` 置 `paused`（实体已生成，避免到期重复生成；恢复即重排复审）。

## 0.1.0 2026-10-07
**新建（Skill_Generator 创建路径，伞形技能）**
- 初始化：SKILL.md（KiloCode frontmatter）＋ agent/ 四格式＋asset/ ＋ dependence/ ＋planned_tasks/ ＋MIT `LICENSE`；git 功能分支 `feature/init-skeleton`；
- 流程 `branch/`：流程总览＋初始化/需求确认/经验查询/编排设计/路由执行/知识库构建/约束编写/整体审查/收尾/修改流程/子技能路由，加三条*占位*子技能位（打包发布、软件测试、git远端管理）；
- 约束 `resistance/`：伞形不重复、子技能位占位、路由派发、五大机制＋git 工作流（含双仓模型与可见性）、降级策略、审查约束、约束部分、沙盒机制；
- 脚本 `scripts/`：check_links / check_len / lint_deps / deps_check / chain_store / logic_chain / process_chain / penalty / garbage_collect / context_compress / self_update / sandbox（链状态落用户缓存目录，不写 skill）；
- 依赖：`deps.json` 声明本地技能 general-programming（必附）及路由目标，全部 `local://<id>`，`lint_deps.py` 通过；
- 计划任务：三个子技能位生成任务，SMS 侧置 `paused`。
