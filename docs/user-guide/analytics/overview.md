# 站点统计总览

> 迁移自：[站点统计相关](https://docs.tangly1024.com/article/notion-next-analytics)

## 作用

了解访问量、来源、热门页面与转化，便于优化内容与推广。

## 常用方案

| 方案 | 说明 | 文档 |
| --- | --- | --- |
| Google Analytics | 免费、功能全 | 下文 GA |
| 百度统计 | 中文站常用 | `NEXT_PUBLIC_ANALYTICS_BAIDU_ID` |
| CNZZ / 友盟 | 国内统计 | `NEXT_PUBLIC_ANALYTICS_CNZZ_ID` |
| 51LA | 国内嵌入统计 | [51LA](./51la.md) |
| Ackee | 自托管开源 | [Ackee](./ackee.md) |
| Umami | 轻量隐私友好 | [Umami](./umami.md) |
| Clarity | 微软免费、含录屏 | [Clarity](./clarity.md) |
| Vercel Analytics | Vercel 面板统计 | `NEXT_PUBLIC_ANALYTICS_VERCEL` |
| 不蒜子 | 页面阅读量展示 | `NEXT_PUBLIC_ANALYTICS_BUSUANZI_ENABLE` |

配置集中在 `conf/analytics.config.js`，可通过环境变量 `NEXT_PUBLIC_*` 或 Notion Config 覆盖。

## Google Analytics（GA4）

Vercel 添加：

| 变量名 | 值 |
| --- | --- |
| `NEXT_PUBLIC_ANALYTICS_GOOGLE_ID` | `G-XXXXXXXXXX` |

衡量 ID 在 GA 后台「数据流」详情中获取。安装后可在页面源码中搜索 `googletagmanager.com/gtag/js?id=` 验证。

## FAQ

- **多久生效**：通常实时；F12 → Elements 搜索衡量 ID 可自检。

## 原文链接

https://docs.tangly1024.com/article/notion-next-analytics
