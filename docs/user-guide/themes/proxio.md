# Proxio 主题

> 主题 ID：`proxio` · 预览：[preview.tangly1024.com/?theme=proxio](https://preview.tangly1024.com/?theme=proxio)  
> 迁移自：[Notion next proxio](https://docs.tangly1024.com/article/notion-next-proxio)

## 简介

作品集与个人品牌展示增强。Proxio 为产品落地页风格主题（Landing-2），适合 SaaS / 作品集首页。

## 主题特性

- **定位**：作品集与个人品牌展示增强。
- **适用场景**：作品集、SaaS 品牌站
- **配置前缀**：`PROXIO_*`（共 **99** 项，见下方配置表）
- **在线预览**：[preview.tangly1024.com/?theme=proxio](https://preview.tangly1024.com/?theme=proxio)

## 适用场景

作品集、SaaS 品牌站

## 启用方式

1. Notion Config 表：`THEME` = `proxio`
2. 环境变量：`NEXT_PUBLIC_THEME=proxio`
3. `blog.config.js` 的 `THEME`

## 落地页与常用区块

常见配置前缀（完整键名见下方配置表或 `themes/proxio/config.js`）：

- `PROXIO_HERO_*` — 英雄区文案与按钮
- `PROXIO_BLOG_*` — 首页博文区块
- `PROXIO_WELCOME_COVER_ENABLE` — 进站欢迎层（点击后进入）
- `PROXIO_*_ENABLE` — 各区块开关（About、Features、CTA 等）

## 右上角导航定制

Proxio 顶栏右侧菜单由 **`themes/proxio/components/MenuList.js`** 渲染，数据来自构建时注入的 `customNav`（Notion **Page**）与 `customMenu`（Notion **Menu / SubMenu**）。

### 数据从哪来

| 来源 | Notion `type` | 何时生效 |
| --- | --- | --- |
| `customNav` | `Page`（已发布） | `CUSTOM_MENU` 关闭，或自定义菜单为空时，与默认项合并 |
| `customMenu` | `Menu` / `SubMenu` | `CUSTOM_MENU=true` **且** 至少有一条 Menu 时，**完全覆盖**顶栏链接 |
| 默认项 | — | 归档、搜索、分类、标签（由 `HEO_MENU_*` 开关控制，见下） |

组装逻辑（简化）：

```js
  const navLinks = Array.isArray(customNav) ? customNav : []
  const menuLinks = Array.isArray(customMenu) ? customMenu : []

  let links = navLinks.length > 0 ? navLinks.concat(defaultLinks) : defaultLinks

  // 如果 开启自定义菜单，则覆盖Page生成的菜单
  if (siteConfig('CUSTOM_MENU', BLOG.CUSTOM_MENU) && menuLinks.length > 0) {
    links = menuLinks
  }
```

Notion 侧解析见 `lib/db/SiteDataApi.js` 的 `getCustomMenu` / `getCustomNav`。

### 推荐做法：Notion Menu / SubMenu

1. 在站点数据库新建行，`type` = `Menu`，`status` = `Published`。
2. `title` 为显示文字；`slug` 为路径或外链（**建议绝对路径** `/about`）。
3. `icon` 可填 Font Awesome，如 `fas fa-home`（见 `MenuItem.js` 渲染）。
4. 二级菜单：紧挨 Menu 下方添加 `SubMenu` 行（规则见 [菜单管理](../menu-secondary.md)）。
5. 确认 `CUSTOM_MENU` 为 `true`（`blog.config.js`、环境变量或 Notion Config 表）。

开启自定义菜单后，归档/搜索等**不会自动出现**，需在 Notion 里自行添加对应 Menu 项（如 slug `/archive`）。

### 仅用 Page 做导航（旧方式）

- 将 `CUSTOM_MENU` 设为 `false`，或 Notion 中不写 Menu。
- 已发布的 `Page` 会进入 `customNav`，并与默认四项合并显示。

### 显示 / 隐藏默认四项

Proxio 复用 HEO 主题的配置键名（历史命名，与是否使用 HEO 主题无关）：

| 配置键 | 默认链接 |
| --- | --- |
| `HEO_MENU_ARCHIVE` | `/archive` |
| `HEO_MENU_SEARCH` | `/search` |
| `HEO_MENU_CATEGORY` | `/category` |
| `HEO_MENU_TAG` | `/tag` |

可在 Notion Config 表、`blog.config.js` 或 `NEXT_PUBLIC_HEO_MENU_*` 环境变量中设为 `false` 隐藏。

### 改样式或结构（开发者）

| 文件 | 作用 |
| --- | --- |
| `themes/proxio/components/Header.js` | 顶栏容器，向 `MenuList` 传 `customNav` / `customMenu` |
| `themes/proxio/components/MenuList.js` | 链接合并、移动端折叠 |
| `themes/proxio/components/MenuItem.js` | 单项与 SubMenu 下拉 |

修改后本地 `yarn dev` 验证；部署到 Vercel 后若菜单未更新，可 **Redeploy** 清缓存。

## 配置说明

配置文件：[`themes/proxio/config.js`](https://github.com/notionnext-org/NotionNext/blob/main/themes/proxio/config.js)  
也可在 **Notion Config** 表中填写同名键（对象/数组用 JSON）。

<!-- theme-config-table -->

### 主要配置项

| 配置键 | 说明 |
| --- | --- |
| `PROXIO_WELCOME_COVER_ENABLE` | 见 config.js |
| `PROXIO_WELCOME_TEXT` | 见 config.js |
| `PROXIO_HERO_ENABLE` | 见 config.js |
| `PROXIO_HERO_TITLE_1` | 见 config.js |
| `PROXIO_HERO_TITLE_2` | 见 config.js |
| `PROXIO_HERO_BUTTON_1_TEXT` | 见 config.js |
| `PROXIO_HERO_BUTTON_1_URL` | 见 config.js |
| `PROXIO_HERO_BUTTON_2_TEXT` | 见 config.js |
| `PROXIO_HERO_BUTTON_2_URL` | 见 config.js |
| `PROXIO_HERO_BUTTON_2_ICON` | 见 config.js |
| `PROXIO_HERO_BANNER_IMAGE` | 见 config.js |
| `PROXIO_HERO_BANNER_IFRAME_URL` | 见 config.js |
| `PROXIO_BLOG_ENABLE` | 见 config.js |
| `PROXIO_BLOG_TITLE` | 见 config.js |
| `PROXIO_BLOG_COUNT` | 见 config.js |
| `PROXIO_BLOG_TEXT_1` | 见 config.js |
| `PROXIO_BLOG_PLACEHOLDER_IMG_URL_1` | 见 config.js |
| `PROXIO_BLOG_PLACEHOLDER_IMG_URL_2` | 见 config.js |
| `PROXIO_BLOG_PLACEHOLDER_IMG_URL_3` | 见 config.js |
| `PROXIO_BLOG_PLACEHOLDER_IMG_URL_4` | 见 config.js |
| `PROXIO_ANNOUNCEMENT_ENABLE` | 见 config.js |
| `PROXIO_FEATURE_ENABLE` | 见 config.js |
| `PROXIO_FEATURE_TITLE` | 见 config.js |
| `PROXIO_FEATURE_TEXT_1` | 见 config.js |
| `PROXIO_FEATURE_TEXT_2` | 见 config.js |
| `PROXIO_FEATURE_1_ICON_CLASS` | 见 config.js |
| `PROXIO_FEATURE_1_ICON_IMG_URL` | 见 config.js |
| `PROXIO_FEATURE_1_TITLE_1` | 见 config.js |
| `PROXIO_FEATURE_1_TEXT_1` | 见 config.js |
| `PROXIO_FEATURE_2_ICON_CLASS` | 见 config.js |
| `PROXIO_FEATURE_2_ICON_IMG_URL` | 见 config.js |
| `PROXIO_FEATURE_2_TITLE_1` | 见 config.js |
| `PROXIO_FEATURE_2_TEXT_1` | 见 config.js |
| `PROXIO_FEATURE_3_ICON_CLASS` | 见 config.js |
| `PROXIO_FEATURE_3_ICON_IMG_URL` | 见 config.js |
| `PROXIO_FEATURE_3_TITLE_1` | 见 config.js |
| `PROXIO_FEATURE_3_TEXT_1` | 见 config.js |
| `PROXIO_FEATURE_BUTTON_TEXT` | 见 config.js |
| `PROXIO_FEATURE_BUTTON_URL` | 见 config.js |
| `PROXIO_CAREER_ENABLE` | 见 config.js |

共 **99** 项，上表列出前 40 项，完整列表见 [config.js](https://github.com/notionnext-org/NotionNext/blob/main/themes/proxio/config.js)。

<!-- /theme-config-table -->

## 相关

- [内置主题全览](./THEMES_CATALOG.md)
- [如何配置站点](../config-site.md)
- [菜单 Menu / SubMenu](../menu-secondary.md)
- [Notion 数据库字段](../notion-database.md)

## 原文链接

https://docs.tangly1024.com/article/notion-next-proxio
