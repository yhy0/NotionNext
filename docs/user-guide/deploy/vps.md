# VPS / 本地服务器部署

> 迁移自：[VPS本地服务器](https://docs.tangly1024.com/article/deploy-notion-next-on-vps)

## 说明

自有服务器可完全掌控进程与域名。新版 NotionNext 建议 **Node.js 20+**；生产环境推荐用 **Docker** 运行，避免系统 Node 版本不一致。

## 基本流程（概要）

1. 服务器安装 Docker（或 Node 20 + Yarn）  
2. 克隆仓库，配置 `.env.local`（`NOTION_PAGE_ID` 等）  
3. `yarn` → `yarn build` → `yarn start`（或使用项目提供的 Docker 配置）  
4. 用 Nginx/Caddy 反代并配置 HTTPS

具体命令以仓库 [GETTING_STARTED.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/GETTING_STARTED.md) 与 Docker 相关文件为准。

## 原文链接

https://docs.tangly1024.com/article/deploy-notion-next-on-vps
