# 评论插件总览

> 迁移自：[评论插件说明](https://docs.tangly1024.com/article/notion-next-comment-plugin) · 配置键见 [features.md](../reference/features.md) 评论章节与 `conf/comment.config.js`

## 支持列表

NotionNext 可同时启用多种评论（`conf/comment.config.js`），评论区以 Tab 切换：

| 插件 | 特点 | 文档 |
| --- | --- | --- |
| Cusdis | 部署最快 | [Cusdis](./cusdis.md) |
| Utterances | GitHub Issues，部署快 | [Utterances](./utterances.md) |
| Twikoo | 体验好，页内管理 | [Twikoo](./twikoo.md) |
| Waline | Valine 升级版 | [Waline](./waline.md) |
| Valine | LeanCloud | [Valine](./valine.md) |
| Giscus | GitHub Discussions | [Giscus](./giscus.md) |
| Artalk | 自托管 | [Artalk](./artalk.md) |
| Gitalk | GitHub | 见 `COMMENT_GITALK_*` 配置 |

## 启用方式

在 Vercel / `.env.local` / Notion Config 中填写对应 `NEXT_PUBLIC_*` 变量后 Redeploy。具体键名见各子文档与 `conf/comment.config.js`。

## 关闭单篇文章评论

**4.5.4+**：在 Notion 数据库添加属性 `comment`（Select），选项含 `Hide`；该文为 Hide 时不显示评论区。详见 [notion-4x.md](../reference/notion-4x.md)。

**4.9.x**：Notion Config 表可直接配置 `WALINE_*` 等评论键（与 Vercel 环境变量等价，优先级见 [config-site.md](../config-site.md)）。

## 原文链接

https://docs.tangly1024.com/article/notion-next-comment-plugin
