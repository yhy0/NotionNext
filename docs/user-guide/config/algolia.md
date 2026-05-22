# Algolia 全文搜索

> 迁移自：[Algolia搜索引擎](https://docs.tangly1024.com/article/notion-next-algolia)

## 何时需要

**纯静态部署**（Vercel `yarn export`、Cloudflare Pages 等）无法使用依赖服务端动态拉取的站内搜索，可接入 Algolia 提供全文检索。

## 配置概要

在环境变量或 Notion Config 中配置 Algolia 的 App ID、Search-Only API Key、Index 名称等（键名以 `conf/` 中搜索相关配置为准）。

构建或定时任务需将文章索引同步到 Algolia（详见源站图文步骤）。

## 原文链接

https://docs.tangly1024.com/article/notion-next-algolia
