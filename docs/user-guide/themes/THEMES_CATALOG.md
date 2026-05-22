# 内置主题全览（25 个）

> 与 `themes/` 目录及 `conf/themeSwitch.manifest.js` 同步 · 当前版本 **4.9.5.2**  
> **每个主题均有独立说明** → [主题目录](./)

预览：`https://preview.tangly1024.com/?theme=<id>`（`id` 为下表「ID」，小写）

切换方式：`NEXT_PUBLIC_THEME=<id>`、Notion Config 的 `THEME`、或开启 `THEME_SWITCH` 挂件。

---

## 一览表

| ID | 名称 | 定位 | 说明文档 |
| --- | --- | --- | --- |
| `simple` | Simple | 默认极简文字博客 | [simple.md](./simple.md) |
| `hexo` | Hexo | 经典双栏博客 | [hexo.md](./hexo.md) |
| `heo` | Heo | 模块化首页、通知条、英雄区 | [heo.md](./heo.md) |
| `gitbook` | GitBook | 文档/手册侧栏目录 | [gitbook.md](./gitbook.md) |
| `next` | Next | 双栏 + 移动悬浮目录 | [next.md](./next.md) |
| `medium` | Medium | Medium 风阅读 | [medium.md](./medium.md) |
| `matery` | Matery | Material 卡片列表 | [matery.md](./matery.md) |
| `nobelium` | Nobelium | 极简 | [nobelium.md](./nobelium.md) |
| `fukasawa` | Fukasawa | 多栏高密度 | [fukasawa.md](./fukasawa.md) |
| `fuwari` | Fuwari | 日系双栏色板 | [fuwari.md](./fuwari.md) · [FUWARI.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/themes/FUWARI.md) |
| `typography` | Typography | 排版优先 | [typography.md](./typography.md) |
| `nav` | Nav | 导航站/聚合 | [nav.md](./nav.md) |
| `plog` | Plog | 图文/轻博客 | [plog.md](./plog.md) |
| `photo` | Photo | 摄影相册 | [photo.md](./photo.md) |
| `movie` | Movie | 影视海报墙 | [movie.md](./movie.md) |
| `game` | Game | 游戏像素风 | [game.md](./game.md) |
| `landing` | Landing | 单页着陆 | [landing.md](./landing.md) |
| `starter` | Starter | 营销落地页区块 | [starter.md](./starter.md) |
| `proxio` | Proxio | 作品集/品牌站 | [proxio.md](./proxio.md) |
| `commerce` | Commerce | 商品展示 | [commerce.md](./commerce.md) |
| `magzine` | Magazine | 杂志封面风（目录名 `magzine`） | [magzine.md](./magzine.md) |
| `claude` | Claude | 文档风 + 贡献热力图首页 | [claude.md](./claude.md) · [CLAUDE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/themes/CLAUDE.md) |
| `endspace` | Endspace | 终末工业风加载与侧栏 | [endspace.md](./endspace.md) · [ENDSPACE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/themes/ENDSPACE.md) |
| `example` | Example | 主题开发骨架 | [example.md](./example.md) |
| `thoughtlite` | ThoughtLite | 时间线首页 + Latest 卡片 | [thoughtlite.md](./thoughtlite.md) · [THOUGHTLITE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/themes/THOUGHTLITE.md) |

---

## 按场景选型

| 场景 | 推荐主题 | 说明 |
| --- | --- | --- |
| 个人文字博客 | `simple`、`hexo`、`nobelium`、`typography` | [simple](./simple.md) · [hexo](./hexo.md) |
| 文档/知识库 | `gitbook`、`claude` | [gitbook](./gitbook.md) · [claude](./claude.md) |
| 作品集 / 品牌 | `proxio`、`starter`、`landing` | [proxio](./proxio.md) · [starter](./starter.md) |
| 图片 / 相册 | `plog`、`photo` | [plog](./plog.md) · [photo](./photo.md) |
| 导航聚合 | `nav` | [nav](./nav.md) |
| 杂志/视觉 | `magzine`、`heo` | [magzine](./magzine.md) · [heo](./heo.md) |
| 阅读体验 | `medium`、`fuwari`、`thoughtlite` | [medium](./medium.md) · [thoughtlite](./thoughtlite.md) |

---

## 主题切换挂件

`NEXT_PUBLIC_THEME_SWITCH=true` 时，使用 `THEME_SWITCH_MANIFEST` 中的名称、简介与 `public/images/themes-preview/<id>.png|webp`。

新增主题贡献需提交预览图并更新 manifest，见 [THEME_MIGRATION_GUIDE.zh-CN.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/THEME_MIGRATION_GUIDE.zh-CN.md)。

## 维护说明

修改 `themes/<id>/config.js` 后，运行 `node scripts/generate-theme-user-docs.mjs` 可刷新对应 `docs/user-guide/themes/<id>.md` 中的配置表。

## 主题菜单键（HEO 命名遗留）

部分主题（含 **Proxio**）用 `HEO_MENU_ARCHIVE` 等控制默认顶栏四项，与是否使用 HEO 主题无关。见 [proxio.md](./proxio.md#右上角导航定制)。
