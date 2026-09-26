# Ivy Liu — Academic website

## 查看效果

完整解压 ZIP，双击 `index.html` 即可，不需要安装 Hexo 或运行构建命令。Blog 现在打开的是迁移后的完整文章目录。CV 支持下载或在浏览器打开。

## 迁移结果

- 全部 10 篇文章已迁入 `blog/`，保留原文、标题、日期及语言。
- 保留 91 个已渲染的 SVG 公式，不需要在线 MathJax。
- 导入全部 8 个旧 PDF 及图片资源；CV PDF 另外保留在 assets 中。
- 修复 Deodhar 文章中原来指向不存在的 pic 目录的图片链接，改为仓库中实际存在的图片。
- 旧 `/2024/.../` 和 `/2025/.../` 地址仍展示对应文章。归档、标签、分类入口展示新博客总目录。
- 原站内部链接已改为本网站内的相对链接，不再依赖旧站在线。网易云和第三方思维导图仍需要联网。
- 压缩包没有 Markdown；它包含 Hexo 生成后的网页。已发布正文可以完整保留，但原始 Markdown 和 LaTeX 编辑源码无法无损恢复。

## 发布到 GitHub Pages

旧站备份已推送到 GitHub，新站位于 main，Pages 从 main 的根目录发布。原 main 内容已保存在 old-site-backup-2026-09-25；其他旧分支备份也保留。后续更新及恢复方法见 [发布与旧站备份说明](DEPLOY.md)。

## 内容维护

- index.html：简介和联系方式。
- 首页 Publications and Preprints：三篇文稿，两篇已加入 arXiv 链接；Research 页面已移除。
- talks.html：仅含 CV 上的九项报告；已有 slides 链接放在题目上。
- cv.html / assets/Ivy-Liu-CV.pdf：简历。
- non-math.html：网易云音乐人入口。
- blog/index.html：按原站摘要展开的完整博客，横线分隔文章。
- blog/文章名/index.html：文章正文。修改后应同步旧年份目录中的对应页面，以保持两个入口的内容一致。
- assets/style.css：全站样式。

文章里的公式是原站的 SVG。未来若修改公式，建议找回原 Markdown 或重新输入 LaTeX 并使用相应的渲染流程。日常发布这个静态网站无需 Hexo。
