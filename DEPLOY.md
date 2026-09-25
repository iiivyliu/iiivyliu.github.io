# 发布与旧站备份

下面按旧仓库使用 main 分支编写（你提供的 ZIP 名为 iiivyliu.github.io-main.zip）。若仓库的旧站位于其他分支，将命令中的 main 改为实际分支。需要电脑已安装 Git；推送时按提示登录 GitHub。

1. 在一个用于存放网站的文件夹打开 PowerShell，运行：

```powershell
git clone --branch main https://github.com/iiivyliu/iiivyliu.github.io.git website-publish
cd website-publish
git branch old-site-backup-2026-09-25
git push origin old-site-backup-2026-09-25
```

确认最后一条命令成功，再继续。GitHub 仓库分支菜单中可以找到 old-site-backup-2026-09-25，里面保留旧网站的文件和提交历史。此时 main 未改变。

2. 创建新版网站分支：

```powershell
git switch -c academic-site
```

3. 解压最新版 Ivy-Liu-academic-website.zip，将里面 academic-website 文件夹的**全部内容**复制到刚克隆的 website-publish 文件夹，同名文件选择替换。不要把外层 academic-website 文件夹一起复制，也不要改动 .git 文件夹。不必清空旧文件。确保 index.html 位于 website-publish 根目录，并包含 .nojekyll。

4. 在同一个 PowerShell 窗口运行：

```powershell
git add .
git commit -m "Publish new academic website"
git push -u origin academic-site
```

这会上传新分支，不会修改 main 或备份分支。不要执行 force push，也不需要合并进 main。

5. 打开 GitHub 仓库的 Settings → Pages。在 Build and deployment 中选择：

- Source：Deploy from a branch
- Branch：academic-site
- Folder：/(root)

点击 Save，等待 Actions 中 Pages 部署成功，再访问 https://iiivyliu.github.io/ 。本地文件夹名和发布分支名不会进入网站网址。若显示旧缓存，按 Ctrl+F5。

若旧仓库存在自动部署 Hexo 的 Actions 工作流，请检查它是否会在新分支推送时运行；停用旧的 Hexo 部署工作流，避免覆盖。Pages 自己的部署流程应保留。

以后更新：修改 website-publish 中的文件，重复 git add、git commit、git push。恢复旧站：把 Settings → Pages 的发布分支改为 old-site-backup-2026-09-25，目录仍选 /(root)。

GitHub 官方 Pages 配置说明：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

本说明只提供操作步骤；GitHub 远端备份和发布尚未由助手执行。
