# DSH 技能索引（仅索引页）

本仓库**只做一件事**：托管一份静态索引页，方便在手机或任何设备上翻看技能清单。

👉 **在线查看：https://axiaodai.github.io/dsh-skills-catalog/**

## 这里有什么 / 没有什么

| 有 | 没有 |
| --- | --- |
| 技能名称、一句话用途、文件数与体积 | ❌ 任何技能的实现文件（`SKILL.md`、脚本、参考资料） |
| 第三方技能的上游仓库链接与授权标注 | ❌ 任何第三方代码或素材 |
| 搜索框（纯前端，离线可用） | ❌ 任何后端或账号 |

技能本体存放在**私有**归档仓库 `axiaodai/dsh-skills` 中；本页里的「目录」链接指向那里，
因此**只有该私有仓库的协作者**点开才有效——这是有意的设计：公开的只是目录信息。

## 页面从哪来

索引页由私有仓库里的 `tools/build-site.ps1` 生成：

1. 扫描 `skills/*/SKILL.md` 的 YAML frontmatter（名称、描述）；
2. 结合 `tools/site-notes.json` 里人手写的一句话摘要（避免照抄他人描述）；
3. 输出单文件、无外部依赖、带搜索的 `site/index.html`；
4. 每次技能同步（计划任务 `DSH-Sync-Skills`，登录时 + 每 30 分钟）自动重建，并复制到本仓库。

## 关于第三方技能

本页出现的第三方技能（bys-travel-plan、handraw-style、book-to-skill、harness-anything）
版权归各自作者所有，授权情况见私有仓库中的 `ATTRIBUTION.md`。本页仅列出名称、用途与上游链接，
属于事实性说明，不包含其代码。
