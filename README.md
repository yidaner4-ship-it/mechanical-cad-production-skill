# 机械制造装配建模

按方案、现有 CAD 或专利资料建立和修订面向制造与装配的机械三维模型。默认使用 Autodesk Fusion，也适用用户指定的 Rhino 或其他机械 CAD。交付深度依据实际完成的几何、装配和工况验证。

## 可复制提示词

```text
使用「机械制造装配建模」技能，按我提供的资料建立或修订机械三维模型。
逐件区分自制件与采购件，将真实安装、定位、紧固和拆装接口建入实体。
按实际工艺落实必要的加工圆角、倒角、孔槽和装配间隙，并按使用环境补齐所需密封或防护。
检查安装、全行程升降或其他实际运行工况，以及拆卸路径。局部改模要连查受影响的零件和工况。
交付可编辑总装和 STEP，重开成品复验，标明已核范围和仍需实测的项目。
这套要求适用于本案采用的机械 CAD。
```

## 从 GitHub 安装和更新

当前版本为 **0.1.0**。安装和更新均使用同一 [GitHub 仓库](https://github.com/yidaner4-ship-it/mechanical-cad-production-skill)。

1. 使用支持插件目录的 Codex CLI 添加 GitHub 来源。

   ```sh
   codex plugin marketplace add yidaner4-ship-it/mechanical-cad-production-skill --ref main
   ```

2. 在 Codex 桌面版的插件目录选择「机械制造装配建模」，安装插件后在新对话中调用技能。实际建模使用当前环境可用的 CAD。
3. 发布者将新版本推送到 `main` 后，运行以下命令刷新已跟踪的来源。

   ```sh
   codex plugin marketplace upgrade mechanical-cad-production-toolkit
   ```

如果当前对话仍显示旧版本，可新开对话，必要时重启客户端。参见 [OpenAI 插件市场命令](https://developers.openai.com/plugins/build/plugins#add-a-marketplace-from-the-cli)。

具备插件管理功能的 ChatGPT 工作区，可由管理员从 GitHub 导入此插件市场、跟踪发布分支并设置成员可用范围。新导入的市场每天自动检查更新，管理员也可立即同步。参见 [工作区 GitHub 同步](https://learn.chatgpt.com/docs/enterprise/plugin-management#keep-plugins-up-to-date)。

也可下载仓库 ZIP，将解压后的 `plugins/fusion-production-modeling/skills/fusion-production-modeling` 文件夹复制到用户目录的 `.agents/skills/`。ZIP 对应下载时的版本，升级时需另行下载。参见 [Codex 本地技能位置](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)。
