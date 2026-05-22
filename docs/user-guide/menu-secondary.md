# 菜单管理（Menu / SubMenu）

> 迁移自：[菜单管理-二级菜单](https://docs.tangly1024.com/article/notion-next-secondary-menu)

## 背景

3.12 前：类型为 **Page** 的条目出现在导航栏。  
3.13+：推荐 **Menu / SubMenu**，`CUSTOM_MENU=true` 时用自定义菜单**覆盖**默认项（归档、搜索等需自行在 Notion 里添加）。

## 开启自定义菜单

- `blog.config.js`：`CUSTOM_MENU: true`（默认多为 true）  
- 或环境变量 `NEXT_PUBLIC_CUSTOM_MENU=true`  
- 或 Notion Config 表中配置 `CUSTOM_MENU`

## 添加 Menu

在 Notion 数据库新建一行：

| 字段 | 示例 |
| --- | --- |
| type | `Menu` |
| title | `首页` |
| status | `Published` |
| slug | `/` |
| icon | `fas fa-home`（Font Awesome） |

## 添加 SubMenu

- **SubMenu 必须紧跟在对应 Menu 后面**。  
- 挂有 SubMenu 的 **Menu 不能点击跳转**，仅作展开。  
- 不能 Menu 套 Menu，SubMenu 套 SubMenu。  
- 孤立的 SubMenu 不会显示。

## 路径写法

使用 **绝对路径**：`/about`。  
勿用 `about`（在子路径页面会变成相对路径，导致 404）。

## 五种常见用法

| 用法 | title 示例 | slug 示例 |
| --- | --- | --- |
| 单页 | 关于 | `/about`（需存在对应 Page） |
| 文章 | 某文 | `/article/example-1` |
| 分类 | 分类名 | `/category/test` |
| 标签 | 标签名 | `/tag/test` |
| 归档 | 归档 | `/archive` |
| 外链 | 博客 | `https://example.com` |

Menu/SubMenu 行本身**不必写正文**，仅作跳转配置。

## 菜单缓存

各页面有缓存；改菜单后建议多刷新或 Vercel **Redeploy** 清缓存。

## 主题差异（Proxio）

Proxio 右上角导航逻辑见 [Proxio 主题：右上角导航](./themes/proxio.md#右上角导航定制)。

## 原文链接

https://docs.tangly1024.com/article/notion-next-secondary-menu
