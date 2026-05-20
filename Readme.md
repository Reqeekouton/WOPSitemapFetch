# WOPSitemapFetch

这个仓库用于自动抓取、修复和托管 **纸上书 (Write On Paper)** 网站的站点地图（sitemap.xml）。

## 它做什么

- 每天自动从 WOP 源站抓取一次 sitemap.xml
- 修复源文件格式不正确的部分
- 将修复后的文件通过 Cloudflare Pages 分发，提供一个搜索引擎能正确识别的 sitemap 地址

## 为什么需要这个

WOP 源站的 sitemap.xml 文件格式有问题，导致 Google、Bing 等搜索引擎无法正确读取。这个仓库解决了这个问题。


## 说明

- 每天凌晨 3 点自动运行（GitHub Actions）
- 内容无变化时不更新
- 旧版本归档，保留 30 天后自动删除