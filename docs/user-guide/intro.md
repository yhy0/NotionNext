# NotionNext 介绍与建站理由

> 迁移自：[NotionNext-快速免费建站](https://docs.tangly1024.com/about) · 文档已按 **4.9.5.2** 修订，请以本仓库 [参考手册](./reference/) 为准

## 旧版升级提醒

2026 年起 Notion 侧数据结构多次升级，过旧源码可能无法完整拉取页面。请将站点代码同步到主线最新发行版（参见 [升级教程](./update.md) 与仓库 `package.json` 版本号）。

## NotionNext 是什么

NotionNext 基于 **Next.js**，将 **Notion 笔记** 渲染为静态站点，无需自购服务器即可建站。  
源码开源：[notionnext-org/NotionNext](https://github.com/notionnext-org/NotionNext)。

## 建站模板

复制官方数据库模板（含 Config、Menu 等页面）：

- 模板页：[https://tanghh.notion.site/02ab3b8678004aa69e9e415905ef32a5](https://tanghh.notion.site/02ab3b8678004aa69e9e415905ef32a5)
- 环境变量 `NOTION_PAGE_ID` 填分享链接中的 **32 位页面 ID**（见 [Vercel 部署](./deploy-vercel.md)）

## 五个理由（摘要）

1. **Notion 写作**：发布只在 Notion 完成，支持多端；数据可导出备份。  
2. **Next.js**：SSR/SEO 友好，性能较好。  
3. **完全自有**：源码、域名、部署在你手中。  
4. **部署简单**：Fork + Vercel 等方案成熟。  
5. **多主题**：内置 **25** 款主题，见 [主题全览](./themes/THEMES_CATALOG.md)；在线预览 [preview.tangly1024.com](https://preview.tangly1024.com/)。

## 部署与配置下一步

- 部署：[Vercel 部署 NotionNext](./deploy-vercel.md) · [部署索引](./deploy/)  
- 配置：[如何配置站点](./config-site.md) · [全站功能索引](./reference/features.md)  
- 写作与字段：[Notion 数据库](./notion-database.md) · [Notion 4.x 能力](./reference/notion-4x.md)  
- 主题：[25 个主题全览](./themes/THEMES_CATALOG.md)

## 参与社区

项目由 **[notionnext-org](https://github.com/notionnext-org)** 维护。若你想提问、改进文档或贡献代码，请参阅 **[参与社区](./community-participate.md)**（含 Discussions、第一次 PR、维护者路径）。

## 原文链接

https://docs.tangly1024.com/about
