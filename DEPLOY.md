# GitHub Pages 发布与备份记录

网站地址：https://iiivyliu.github.io/

新网站分支：main。GitHub Pages 使用 Deploy from a branch，目录为 /(root)。无需 Hexo 或本地构建。

## 旧站备份

2026-09-25 已在远程创建并逐一核对以下备份，包含对应分支的文件及提交历史：

- old-site-backup-2026-09-25：原 main，34de031a26b2481ae68b00ec2f0ba9d3c53c7e9b
- old-gh-pages-backup-2026-09-25：原 gh-pages，1c5f59ca05329e18200562ed76ebb8e0cde34541
- old-master-backup-2026-09-25：原 master，40be7a91bc2d61ff1f0e18becd859c3d7b5604a5

2026-09-26：新版网站及最新 CV 已合并到 main；GitHub Pages 从 main 根目录发布。旧 main 的内容完整保存在 old-site-backup-2026-09-25，其他旧分支备份同样保留。

## 后续更新

在 GitHub 仓库选择 main 分支，编辑对应网页或上传替换文件并提交。GitHub Pages 会自动更新。

本地维护可克隆 main 分支，再修改、提交、推送。请确保 Git 已正常登录；这次上传绕过了电脑上故障的代理与凭据组件，没有修改全局 Git 设置。

## 恢复旧站

在仓库 Settings → Pages 中将发布分支改为 old-site-backup-2026-09-25，目录保持 /(root)，保存后等待部署完成即可。
