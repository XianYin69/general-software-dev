---
name: general-software-dev
version: 0.1.1
description: >
  通用软件开发总控（伞形/中枢）技能：设计→实现→打包发布→测试→版本控制与远端；
  只做跨领域编排与横切环节（脚手架、架构决策、打包发布、测试、git 远端），
  专项子任务一律派发给既有专家技能（general-programming / python-expert / cpp-expert /
  c-expert / frontend-dev / database-management / webapp-testing / create-pull-request 等），
  禁止复制它们的内容；子技能位 packaging-and-release / software-testing / git-remote-management
  已生成实体，本体只做路由与门禁（0.1.1）。
license: MIT
metadata:
  category: development
---

# general-software-dev

使用 `general-software-dev` skill 来完成用户请求。

## 工作原则

1. **按流程执行**：不跳步、不静默越权；决策节点留逻辑链。
2. **伞形不重复**：本体只持横切环节，能力经 [dependence/](dependence/dependence.md)
   与 [branch/子技能路由/](branch/子技能路由/子技能路由.md) 声明与派发，只传意图＋参数。
3. **双链辩论**：审查节点运行正反双链（`python scripts/logic_chain.py debate`）。
4. **返回机制**：审查失败记中断（`python scripts/process_chain.py interrupt`），修复后 resume；
   任一路径完成＝收口返回调度方整合续排。
5. **惩罚熔断**：重试达 10 次即熔断（`python scripts/penalty.py hit`），回退或求助用户。
6. **垃圾回收**：tmp 经 compare→release 释放后删除；未指定目录时沙盒作业。

## 执行路径

**创建路径**：[初始化](branch/初始化/初始化.md)→[需求确认](branch/需求确认/需求确认.md)→
[经验查询](branch/经验查询/经验查询.md)→[编排设计](branch/编排设计/编排设计.md)→
[路由执行](branch/路由执行/路由执行.md)→[知识库构建](branch/知识库构建/知识库构建.md)→
[约束编写](branch/约束编写/约束编写.md)→[整体审查](branch/整体审查/整体审查.md)→
[收尾](branch/收尾/收尾.md)→**完成**
**修改路径**：[初始化](branch/初始化/初始化.md)→[修改流程](branch/修改流程/修改流程.md)→**完成**

**子技能位（已实体化）**：[打包发布](branch/打包发布/打包发布.md)
（packaging-and-release）· [软件测试](branch/软件测试/软件测试.md)（software-testing）·
[git远端管理](branch/git远端管理/git远端管理.md)（git-remote-management）。

总览与步骤表：[branch/流程/](branch/流程/流程.md)；约束兜底：[resistance/](resistance/resistance.md)。
