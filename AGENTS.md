# 本仓库约定

本仓库保存个人编写的 Codex Skills。用户对具体工作流程的要求优先。

- 正式 Skill 放在 `skills/<skill-name>/SKILL.md`；目录名使用小写字母、数字和连字符，`SKILL.md` 的 `name` 与目录名一致。
- `description` 写清 Skill 的工作内容和触发场景；正文保持可执行、具体，不要把普通项目规则写成无条件触发的 Skill。
- 较长资料、脚本和资源分别放在该 Skill 内的 `references/`、`scripts/`、`assets/`，并从 `SKILL.md` 指明使用条件。
- 新增、重命名或删除正式 Skill 时，同步更新根目录 `README.md` 中的清单。
- 模板只放在 `templates/`，不要把未完成的占位模板放进 `skills/`。
- 提交前测试明确调用、自然语言触发和不应触发的场景；检查所有引用路径与脚本。
- 仓库公开，不提交密钥、凭据、私人文件或真实工作数据。
