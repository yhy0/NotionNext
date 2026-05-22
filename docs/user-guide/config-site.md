# 如何配置站点

> 迁移自：[如何配置站点](https://docs.tangly1024.com/article/how-to-config-notion-next) · 全量配置项见 **[参考手册](./reference/features.md)**（4.9.5.x）

部署成功后，可调整主题、评论、字体、动画等。配置来源**优先级**（高 → 低）：

1. **Notion Config 表**（`type = Config` 文档内的表格）  
2. **环境变量**（Vercel / `.env.local`）  
3. **`blog.config.js` 与 `conf/*.js`**  
4. **主题 `themes/<name>/config.js`**

## 1. 在 Notion 中修改

### 站点基础信息

图标、标题、描述、封面等默认从 **Notion 站点根页** 读取（与模板一致）。

### Notion Config（V4.1+）

在模板中复制 **type = Config** 的页面，用表格维护键值：

| 表头 | 说明 |
| --- | --- |
| 启用 | 勾选后生效 |
| 配置名 | 与代码中键名一致，如 `AUTHOR`、`THEME` |
| 配置值 | 字符串；对象/数组需 **JSON 双引号** 格式 |
| 配置备注 | 备忘 |
| 配置附件 | 图片类配置可上传 |

**注意**：`NOTION_PAGE_ID` **不能**在 Config 表中配置，必须在环境变量或代码中设置。

建议配置：`AUTHOR`、`LINK`、`CONTACT_EMAIL`（联系方式见 `conf/contact.config.js`）。

老用户可从模板复制「配置中心」页：[模板链接](https://tanghh.notion.site/02ab3b8678004aa69e9e415905ef32a5)。

## 2. 修改代码

主要入口：`blog.config.js`（V4.8+ 大量配置在 `conf/*.js`）。  
修改后 Vercel 会自动触发部署；失败时查看 Deployment 日志。

## 3. 环境变量

Vercel：**Settings → Environment Variables**，修改后 **Deployments → Redeploy**。

本地：项目根目录 `.env.local`。

示例：

| Key | Value | 说明 |
| --- | --- | --- |
| `NEXT_PUBLIC_THEME` | `proxio` | 主题名 = `themes/` 下文件夹名 |
| `NEXT_PUBLIC_AUTHOR` | 你的名字 | 作者 |
| `NEXT_PUBLIC_LINK` | `https://你的域名` | 站点 URL |

内置 **25** 个主题，完整列表与选型见 **[内置主题全览](./themes/THEMES_CATALOG.md)**（`magzine` 目录名拼写与 magazine 不同）。

主题切换挂件：`conf/widget.config.js` 中 `THEME_SWITCH` / `NEXT_PUBLIC_THEME_SWITCH`。

## 4. 主题个性化

各主题有独立 `themes/<theme>/config.js`，首页区块、Hero 文案等在此或 Notion Config 中配置。  
- 全主题说明：[THEMES_CATALOG.md](./themes/THEMES_CATALOG.md)  
- Proxio 顶栏：[proxio.md](./themes/proxio.md#右上角导航定制)  
- 站点功能索引：[features.md](./reference/features.md)

## 5. 延伸阅读

| 主题 | 文档 |
| --- | --- |
| Notion 字段与 4.x | [notion-4x.md](./reference/notion-4x.md) |
| 基础功能总览 | [site-basics.md](./config/site-basics.md) |
| URL / 搜索 | [url-customize.md](./config/url-customize.md)、[algolia.md](./config/algolia.md) |

## 原文链接

https://docs.tangly1024.com/article/how-to-config-notion-next
