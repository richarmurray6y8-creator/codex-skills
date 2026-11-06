# codex-skills

My collection of reusable Agent Skills.

## Handoff

一份通用的交接 skill，适用于 Codex 和 Claude Desktop。它会记录任务目标、当前进度、已有授权和接下来的操作，帮助另一个智能体继续工作。

- [查看 skill 源文件](handoff/SKILL.md)
- [下载 Claude Desktop 安装包](https://github.com/richarmurray6y8-creator/codex-skills/raw/refs/heads/main/handoff-claude.zip)

### 在 Claude Desktop 使用

1. 下载上面的 handoff-claude.zip。
2. 打开 Claude 的 Customize → Skills，选择创建并上传 skill，上传这个 ZIP。
3. 启用后，让 Claude 使用 handoff 生成交接文档。

使用 Claude 自定义 skill 需要在设置中启用代码执行和文件创建。详见 [Claude 官方使用说明](https://support.claude.com/en/articles/12512180-use-skills-in-claude)。

### 在 Codex 使用

1. 下载本仓库并解压，将整个 handoff 文件夹复制到 skills 目录：
   - Windows：%USERPROFILE%\.codex\skills\handoff
   - macOS / Linux：~/.codex/skills/handoff
2. 在 Codex 中输入 $handoff 调用。必要时重新打开 Codex 以刷新 skill 列表。

两个平台使用相同的 SKILL.md；Claude 安装包只包含通用文件，Codex 文件夹额外保留自身的界面配置。实际可用的工具和文件位置取决于所在环境。