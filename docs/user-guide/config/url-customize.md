# URL 风格自定义

> 迁移自：[URL风格自定义](https://docs.tangly1024.com/article/notion-next-url-customize)

## 文章前缀

通过 `POST_URL_PREFIX` 控制 Post 路径，例如 `/article/`、`/post/` 或留空。

## 语义化变量

支持在前缀中使用变量（以仓库 `blog.config.js` / Notion Config 为准），例如：

- `%category%`、`%year%`、`%month%`、`%day%`

## 分类英文映射

中文分类可映射为英文 slug（如 `知行合一` → `learning`），便于 SEO 友好 URL。配置项见 `POST_URL_PREFIX_MAPPING_CATEGORY` 相关说明。

## 原文链接

https://docs.tangly1024.com/article/notion-next-url-customize
