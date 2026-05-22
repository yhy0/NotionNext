# Netlify 部署 NotionNext

> 迁移自：[Netlify云函数部署](https://docs.tangly1024.com/article/deploy-notion-next-with-netlify)

## 说明

自 **NotionNext 4.0.9** 起支持 Netlify。相对 Vercel：免费额度更宽松，国内访问速度往往更好。

- 构建环境：**Node 20**（与仓库 README、`.nvmrc` 一致）  
- 包管理：**Yarn**（`yarn`、`yarn build`）

## 步骤

1. 打开 [netlify.com](https://www.netlify.com/)，用 GitHub 登录  
2. **Import an existing project**，选择你的 NotionNext 仓库  
3. 配置环境变量 `NOTION_PAGE_ID` 等（与 Vercel 相同）  
4. 部署完成后在 **Domain settings** 绑定域名并配置 CNAME

## 原文链接

https://docs.tangly1024.com/article/deploy-notion-next-with-netlify
