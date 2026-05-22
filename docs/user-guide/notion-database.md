# Notion 数据库的使用

> 迁移自：[Notion数据库的使用](https://docs.tangly1024.com/article/start-to-write)（slug: `start-to-write`）  
> 4.x 新增能力（多数据源、置顶、密码、评论 Hide 等）见 **[reference/notion-4x.md](./reference/notion-4x.md)**

## 基本操作

- **写作**：在表格 `title` 列点击 **OPEN**，或右上角 **New** 新建。  
- **排序**：拖拽行左侧六点手柄；部分主题支持置顶逻辑见 `top-tag` 配置。

## 字段说明

| 属性 | 必填 | 说明 |
| --- | --- | --- |
| `title` | 是 | 标题 |
| `status` | 是 | 仅 `Published` 会展示 |
| `type` | 是 | 见下表 |
| `summary` | 否 | 摘要（列表/搜索） |
| `date` | 否 | 发布日期 |
| `category` | 否 | 分类 |
| `tags` | 否 | 标签 |
| `slug` | 否 | 路径或外链（见下） |
| `icon` | 否 | 菜单图标（Page/Menu） |
| `password` | 否 | 文章密码锁 |

### type 类型

| type | 作用 |
| --- | --- |
| `Post` | 博文，出现在列表 |
| `Page` | 单页，不在博文列表；可作导航（旧方案） |
| `Menu` | 自定义菜单项 |
| `SubMenu` | 子菜单（紧跟在 Menu 后） |
| `Notice` | 公告 |
| `Config` | 配置中心表格 |

### slug 规则摘要

- **Menu / SubMenu**：跳转路径，建议 **绝对路径** `/about`；可写完整 URL 外链。  
- **Page**：单页路径，如 `about` → `https://域名/about`（勿多余前缀）。  
- **Post**：文章路径，默认常带前缀如 `/article/your-slug`（由 `POST_URL_PREFIX` 等配置决定）。

## 模板

使用官方复制模板：[tanghh.notion.site 模板](https://tanghh.notion.site/02ab3b8678004aa69e9e415905ef32a5)。

## 原文链接

https://docs.tangly1024.com/article/start-to-write
