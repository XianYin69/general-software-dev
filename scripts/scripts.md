# scripts（脚本库）

脚本一律**英文名称**；行数不限，但禁裸 except、禁 print 调试残留、
禁 >100 字符长行、禁超长函数；缓存与状态文件落用户缓存目录，不写本目录。

## 清单

| 脚本 | 职责 |
|---|---|
| [check_links.py](check_links.py) | 全目录 markdown 悬空链接校验（须＝0） |
| [check_len.py](check_len.py) | `.md` ≤50 行红线校验 |
| [lint_deps.py](lint_deps.py) | `dependence/deps.json` 每条须附 `source_url` |
| [deps_check.py](deps_check.py) | 依赖可达性与本地技能存在性自检 |
| [logic_chain.py](logic_chain.py) | 逻辑链 add／debate（正反双链辩论） |
| [process_chain.py](process_chain.py) | 过程链 save／load／interrupt／resume |
| [penalty.py](penalty.py) | 惩罚计数 hit／reset（达 10 熔断） |
| [garbage_collect.py](garbage_collect.py) | tmp 回收（默认预览） |
| [context_compress.py](context_compress.py) | 长文本压缩为摘要卡片 |
| [sandbox.py](sandbox.py) | 未指定目标时的固定路径沙盒 |
| [self_update.py](self_update.py) | report／compare／release／clean（唯一写盘通道） |

## 用法约定

`python scripts/<name>.py --help` 看参数；写盘类默认 `--dry-run`，需 `--yes` 才落地。

## 相关

- [../SKILL.md](../SKILL.md) · [../update/update.md](../update/update.md)
