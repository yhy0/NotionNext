# NotionNext 运行原理

> 迁移自：[NotionNext项目运行原理](https://docs.tangly1024.com/article/vercel-notionnext-notion)

## 三要素

| 组件 | 作用 |
| --- | --- |
| **Notion** | 内容数据库 |
| **GitHub** | 源码与版本 |
| **Vercel / Netlify 等** | 构建与托管 |

构建时通过 Notion API 拉取页面，生成静态/ISR 页面；访客访问时优先读缓存，过期后按 `NEXT_REVALIDATE_SECOND` 再同步。

## 开发者文档

详见 [ARCHITECTURE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/ARCHITECTURE.md)。

## 原文链接

https://docs.tangly1024.com/article/vercel-notionnext-notion
