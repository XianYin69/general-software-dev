# git 远端管理（子技能位 · 实体）
**状态：实体**——由子技能 [`git-remote-management`](../../../git-remote-management/SKILL.md) 承担，
本体只保留分支策略与推送前判定，不复制其脚本。

## 交接接口
- 本体交付：仓库可见性意图（PUBLIC/PRIVATE）、分支基线（dev/main）、待推送范围；
- 子技能交付：远端审计 → 分支守卫 → 提交卫生 → 密钥扫描 → 可见性门禁；
- 声明位置：[../../dependence/deps.json](../../dependence/deps.json) 条目
  `local://git-remote-management`；PR 描述由子技能再派 `create-pull-request`。

## 本体职责边界
1. 推送与可见性判定见 [git工作流约束](../../resistance/git工作流约束/git工作流约束.md)
   第 9、10 条：推送须用户确认，疑似违规/涉密转 PRIVATE；
2. 本体不执行 git 写操作，全部经子技能脚本（默认只读，`--yes` 才写）；
3. 附属双仓模型（本体 PUBLIC ＋ `private/` 伴生私有仓）由子技能细则持有。

## 兄弟位
[打包发布/](../打包发布/打包发布.md) · [软件测试/](../软件测试/软件测试.md)
