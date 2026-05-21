# WOPSitemapFetch

这个仓库用于自动抓取、提取和托管 **纸上书 (Write On Paper)** 网站的站点地图（sitemap.xml）中的链接。

## 它做什么

- 每天自动从 WOP 源站抓取一次 sitemap.xml
- 将源文件中的url输出为文本，且最新文件只会列出旧文件中不存在的url
- 将修复后的文件通过 Cloudflare Pages 分发，以便管理人员手动提交索引。

## 为什么需要这个

WOP 源站的 sitemap.xml 文件格式有问题，导致 Google、Bing 等搜索引擎无法正确读取。这个仓库用于自动化的抓取相关url，并让网站管理人员可以手动提交。


## 说明

- 每天凌晨 3 点自动运行（GitHub Actions）
- 内容无变化时不更新
- 旧版本归档，保留 30 天后自动删除
