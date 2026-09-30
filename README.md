# 我的 Codex Skills

这个仓库用于保存我根据自己的工作习惯和工作流程编写的可复用 Skill。每个 Skill 独立存放，便于单独安装、修改和测试。

仓库是源码存放处；把仓库上传到 GitHub 不会自动将其中的 Skill 安装到 Codex。

## 目录结构

```text
my-codex-skills/
├── skills/
│   ├── .gitkeep           # 让尚未添加 Skill 的目录可被 Git 跟踪
│   └── <skill-name>/
│       ├── SKILL.md          # 必需：名称、触发描述和操作说明
│       ├── references/       # 可选：较长的参考资料
│       ├── scripts/          # 可选：需要执行的脚本
│       └── assets/           # 可选：模板和其他资源
├── templates/
│   └── SKILL.template.md     # 新建 Skill 时复制；它本身不是 Skill
├── AGENTS.md                 # 在本仓库内协作时的约定
├── .gitignore
├── LICENSE
└── README.md
```

`skills/` 目前尚无正式 Skill。以后每新增一个 Skill，就在下面的清单中补上一行：

| Skill | 适用场景 | 入口 |
| --- | --- | --- |
| 暂无 | 新 Skill 创建后更新此表 | — |

## 新建一个 Skill

1. 在 `skills/` 下创建以小写字母、数字和连字符命名的目录，例如 `skills/meeting-notes/`。
2. 将 `templates/SKILL.template.md` 复制为该目录的 `SKILL.md`，按自己的实际流程填写。也可以在 Codex 中使用 `$skill-creator` 起草。
3. 将 `name` 改为目录名；在 `description` 中同时说明**能做什么**和**什么时候应使用**。
4. 只在需要时添加 `references/`、`scripts/` 或 `assets/`。在 `SKILL.md` 中写明何时读取或运行这些文件。
5. 用一个明确点名 Skill 的任务、一个不点名但符合适用场景的任务，以及一个不应触发它的任务进行试用。
6. 更新上面的 Skill 清单，再提交到 GitHub。

本仓库公开。提交前请检查 Skill、示例和脚本，不要上传令牌、密码、私有文件或真实工作数据。

## 在 Codex 中使用

可以让 Codex 从本仓库的 `skills/<skill-name>` 路径安装指定 Skill 到个人全局目录 `~/.codex/skills/`。也可以克隆仓库后在 Windows PowerShell 中手动复制：

```powershell
git clone https://github.com/sunzhe1216/my-codex-skills.git
Set-Location my-codex-skills
Copy-Item -Recurse -Force .\skills\your-skill "$HOME\.codex\skills\"
```

将示例中的 `your-skill` 换成实际目录名。复制安装的 Skill 是独立副本；仓库更新后，需要重新复制对应目录。安装后可在 Codex 中通过 `$skill-name` 明确调用，也可以让 Codex 在适合的任务中按需选用。

## 许可

本仓库采用 [MIT License](LICENSE)。
