# general-software-dev

通用软件开发**总控（伞形/中枢）**技能：设计 → 实现 → 打包发布 → 测试 → 版本控制与远端。
本体只负责跨领域编排与横切环节，专项实现一律派发给既有专家技能，不复制其内容。

## 结构

- [`SKILL.md`](SKILL.md)：入口（KiloCode YAML frontmatter，可直接注入 agent）。
- [`agent/`](agent/)：四格式提示词（CLAUDE.md / .cursorrules / instructions.md /
  agent_prompt.md），各一句话。
- [`branch/`](branch/branch.md)：流程分支库——主干
  [`branch/流程/`](branch/流程/流程.md)，含子技能路由与三个占位子技能位。
- [`scripts/`](scripts/scripts.md)：脚本库（英文名，链接/行数/依赖校验＋五机制）。
- [`dependence/`](dependence/dependence.md)：依赖声明＋
  [`deps.json`](dependence/deps.json)（每条必附 `source_url`）。
- [`planned_tasks/`](planned_tasks/README.md)：计划任务（一任务一文件，SMS 调度器执行）。
- [`references/`](references/references.md)：跨领域知识库（编排判例卡片）。
- [`resistance/`](resistance/resistance.md)：约束库（伞形不重复、占位、路由、五机制、git）。
- [`update/`](update/update.md)：自更新接口（本体唯一写盘通道）。
- [`asset/`](asset/asset.md)：技能包资产。
- [`CHANGELOG.md`](CHANGELOG.md) / [`CONTRIBUTORS.md`](CONTRIBUTORS.md) /
  [`LICENSE`](LICENSE)：版本记录、贡献者、MIT 许可。

## 快速自检

```
python scripts/check_links.py
python scripts/check_len.py
python scripts/lint_deps.py
python scripts/deps_check.py
```

## 红线摘要

悬空链接＝0；`.md` ≤50 行；依赖必附原始链接；子技能位仅占位（内容由后续任务生成）；
不复制专家技能内容；不静默写盘。
