# GitBook 主题

> 主题 ID：`gitbook` · 预览：[preview.tangly1024.com/?theme=gitbook](https://preview.tangly1024.com/?theme=gitbook)

## 简介

文档与手册式侧栏目录结构。

## 主题特性

- **定位**：文档与手册式侧栏目录结构。
- **适用场景**：技术文档、手册侧栏目录
- **配置前缀**：`GITBOOK_*`（共 **11** 项，见下方配置表）
- **在线预览**：[preview.tangly1024.com/?theme=gitbook](https://preview.tangly1024.com/?theme=gitbook)

## 适用场景

技术文档、手册侧栏目录

## 启用方式

1. Notion Config 表：`THEME` = `gitbook`
2. 环境变量：`NEXT_PUBLIC_THEME=gitbook`
3. `blog.config.js` 的 `THEME`

## 配置说明

配置文件：[`themes/gitbook/config.js`](https://github.com/notionnext-org/NotionNext/blob/main/themes/gitbook/config.js)  
也可在 **Notion Config** 表中填写同名键（对象/数组用 JSON）。

<!-- theme-config-table -->

### 主要配置项

| 配置键 | 说明 |
| --- | --- |
| `GITBOOK_INDEX_PAGE` | 见 config.js |
| `GITBOOK_AUTO_SORT` | 见 config.js |
| `GITBOOK_LATEST_POST_RED_BADGE` | 见 config.js |
| `GITBOOK_MENU_CATEGORY` | 见 config.js |
| `GITBOOK_BOOK_MENU_TAG` | 见 config.js |
| `GITBOOK_MENU_ARCHIVE` | 见 config.js |
| `GITBOOK_MENU_SEARCH` | 见 config.js |
| `GITBOOK_EXCLUSIVE_COLLAPSE` | 见 config.js |
| `GITBOOK_FOLDER_HOVER_EXPAND` | 见 config.js |
| `GITBOOK_WIDGET_REVOLVER_MAPS` | 见 config.js |
| `GITBOOK_WIDGET_TO_TOP` | 见 config.js |

<!-- /theme-config-table -->

## 相关

- [内置主题全览](./THEMES_CATALOG.md)
- [如何配置站点](../config-site.md)
- [菜单 Menu / SubMenu](../menu-secondary.md)
