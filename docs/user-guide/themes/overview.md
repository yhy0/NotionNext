# 主题功能说明

> 基于当前主线 **4.9.5.2** · 完整列表见 **[内置主题全览](./THEMES_CATALOG.md)**（25 个主题，一个不漏）

## 快速理解

- 主题 ID = `themes/` 下**文件夹名**（小写），如 `simple`、`hexo`、`thoughtlite`。
- 默认主题：`simple`（`blog.config.js` 的 `THEME`）。
- 在线预览：[preview.tangly1024.com](https://preview.tangly1024.com/) → `?theme=<id>`。

## 切换默认主题

1. Notion Config 表 `THEME`（推荐）
2. 环境变量 `NEXT_PUBLIC_THEME`
3. `blog.config.js` 的 `THEME`

## 在线切换（预览）

`NEXT_PUBLIC_THEME_SWITCH=true`（`conf/widget.config.js`），页面显示可拖拽主题面板，元数据来自 `conf/themeSwitch.manifest.js`。

## 主题目录结构

每个主题通常含：`components/`、`config.js`、`index.js`、`style.js`。

## 配置主题

- 全站键： [features.md](../reference/features.md)
- 单主题键：打开 `themes/<id>/config.js`，或在 Notion Config 用**同名键**（复杂值用 JSON）
- 无代码改样式：[custom-style.md](../development/custom-style.md)

## 各主题说明（25 篇）

- **完整列表**：[主题目录](./)（每主题一篇 `<id>.md`）  
- **选型总表**：[THEMES_CATALOG.md](./THEMES_CATALOG.md)  
- **开发者深度文档**（Claude 全局 `_app.js` 等）：`docs/developer/themes/` 下 CLAUDE、ENDSPACE 等；站长向以本目录 `<id>.md` 为准

## 自建主题

[development/own-theme.md](../development/own-theme.md) · [THEME_MIGRATION_GUIDE.zh-CN.md](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/THEME_MIGRATION_GUIDE.zh-CN.md)

## 历史原文

https://docs.tangly1024.com/article/notion-next-themes
