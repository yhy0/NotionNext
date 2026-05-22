# Heo 主题

> 主题 ID：`heo` · 预览：[preview.tangly1024.com/?theme=heo](https://preview.tangly1024.com/?theme=heo)  
> 迁移自：[HEO主题](https://docs.tangly1024.com/article/notionnext-heo)

## 简介

致敬张洪 Heo，丰富的模块化组件。

## 主题特性

- **定位**：致敬张洪Heo,丰富的 模块化组件。
- **适用场景**：模块化首页、通知与英雄区
- **配置前缀**：`HEO_*`（共 **58** 项，见下方配置表）
- **在线预览**：[preview.tangly1024.com/?theme=heo](https://preview.tangly1024.com/?theme=heo)

## 适用场景

模块化首页、通知与英雄区

## 启用方式

1. Notion Config 表：`THEME` = `heo`
2. 环境变量：`NEXT_PUBLIC_THEME=heo`
3. `blog.config.js` 的 `THEME`

## 要求与页面结构

- 需要 NotionNext **4.0+**。视觉参考 Acrylic-Promote 风格。
- **顶栏通知**：可滚动通知条
- **英雄区**：左侧标签卡片（默认链到标签归档）、右侧推荐置顶文
- **文章列表**：分类与公告
- **移动端**：精简英雄区

Notion Config 中复杂值需 **JSON 格式**（双引号）。菜单开关使用 `HEO_MENU_*`（归档、搜索、分类、标签等）。更多实现细节见源码注释：[themes/heo/index.js](https://github.com/notionnext-org/NotionNext/blob/main/themes/heo/index.js)。

## 配置说明

配置文件：[`themes/heo/config.js`](https://github.com/notionnext-org/NotionNext/blob/main/themes/heo/config.js)  
也可在 **Notion Config** 表中填写同名键（对象/数组用 JSON）。

<!-- theme-config-table -->

### 主要配置项

| 配置键 | 说明 |
| --- | --- |
| `HEO_HOME_POST_TWO_COLS` | 见 config.js |
| `HEO_LOADING_COVER` | 见 config.js |
| `HEO_HOME_BANNER_ENABLE` | 见 config.js |
| `HEO_SITE_CREATE_TIME` | 见 config.js |
| `HEO_NOTICE_BAR` | 见 config.js |
| `HEO_HERO_REVERSE` | 见 config.js |
| `HEO_HERO_BODY_REVERSE` | 见 config.js |
| `HEO_HERO_TITLE_1` | 见 config.js |
| `HEO_HERO_TITLE_2` | 见 config.js |
| `HEO_HERO_TITLE_3` | 见 config.js |
| `HEO_HERO_TITLE_4` | 见 config.js |
| `HEO_HERO_TITLE_5` | 见 config.js |
| `HEO_HERO_TITLE_LINK` | 见 config.js |
| `HEO_HERO_COVER_TITLE` | 见 config.js |
| `HEO_HERO_CATEGORY_1` | 见 config.js |
| `HEO_HERO_CATEGORY_2` | 见 config.js |
| `HEO_HERO_CATEGORY_3` | 见 config.js |
| `HEO_HERO_RECOMMEND_POST_TAG` | 见 config.js |
| `HEO_HERO_RECOMMEND_POST_SORT_BY_UPDATE_TIME` | 见 config.js |
| `HEO_HERO_RECOMMEND_COVER_ENABLE` | 见 config.js |
| `HEO_INFOCARD_GREETINGS` | 见 config.js |
| `HEO_INFO_CARD_URL1` | 见 config.js |
| `HEO_INFO_CARD_ICON1` | 见 config.js |
| `HEO_INFO_CARD_URL2` | 见 config.js |
| `HEO_INFO_CARD_ICON2` | 见 config.js |
| `HEO_INFO_CARD_URL3` | 见 config.js |
| `HEO_INFO_CARD_TEXT3` | 见 config.js |
| `HEO_GROUP_ICONS` | 见 config.js |
| `HEO_SOCIAL_CARD` | 见 config.js |
| `HEO_SOCIAL_CARD_TITLE_1` | 见 config.js |
| `HEO_SOCIAL_CARD_TITLE_2` | 见 config.js |
| `HEO_SOCIAL_CARD_TITLE_3` | 见 config.js |
| `HEO_SOCIAL_CARD_URL` | 见 config.js |
| `HEO_POST_COUNT_TITLE` | 见 config.js |
| `HEO_SITE_TIME_TITLE` | 见 config.js |
| `HEO_SITE_VISIT_TITLE` | 见 config.js |
| `HEO_SITE_VISITOR_TITLE` | 见 config.js |
| `HEO_MENU_INDEX` | 见 config.js |
| `HEO_MENU_CATEGORY` | 见 config.js |
| `HEO_MENU_TAG` | 见 config.js |

共 **58** 项，上表列出前 40 项，完整列表见 [config.js](https://github.com/notionnext-org/NotionNext/blob/main/themes/heo/config.js)。

<!-- /theme-config-table -->

## 相关

- [内置主题全览](./THEMES_CATALOG.md)
- [如何配置站点](../config-site.md)
- [菜单 Menu / SubMenu](../menu-secondary.md)

## 原文链接

https://docs.tangly1024.com/article/notionnext-heo
