# ljj_skill

个人自制技能的统一维护仓库。

## 目录约定

所有技能放在 `skills/<技能名>/` 下，每个技能包含一个 `SKILL.md`。需要时，在技能目录内添加 `scripts/`、`references/`、`assets/` 或 `agents/`。

## 已收录技能

- [session-handoff](skills/session-handoff/SKILL.md)：将当前会话整理成供新会话接续的交接摘要。

## 本机使用

本仓库是技能内容的唯一源；安装位置使用符号链接指向对应技能目录。以后直接修改仓库文件即可让安装入口读到相同内容。

当前 `session-handoff` 的安装入口：

```text
~/.codex/skills/session-handoff → <本仓库>/skills/session-handoff
```

新增技能时，先在 `skills/<技能名>/` 中创建完整技能，再按需要链接到用户的技能安装目录。确认安装位置没有同名文件或目录后，可参照：

```sh
ln -s "/绝对路径/ljj_skill/skills/技能名" "$HOME/.codex/skills/技能名"
```

移动或重命名仓库后，需要更新对应符号链接。
