# Vercel 部署 NotionNext

> 迁移自：[Vercel部署NotionNext](https://docs.tangly1024.com/article/vercel-deploy-notion-next)

## 概要

Vercel 对个人站点免费额度通常足够。NotionNext 将 Notion 笔记渲染为博客；部署三步：**复制模板 → Fork 代码 → Vercel 导入**。

预览站点：[preview.tangly1024.com](https://preview.tangly1024.com/)

## 一、Notion 模板与页面 ID

1. 打开 [官方模板](https://tanghh.notion.site/02ab3b8678004aa69e9e415905ef32a5)，右上角 **Duplicate** 复制到你的工作区。  
2. 打开该页 **Share → Publish → Share to web**。  
3. 从 URL 中取 **32 位** `NOTION_PAGE_ID`（仅字母数字，不含 `?v=` 等后缀）。  
   - 示例：`02ab3b8678004aa69e9e415905ef32a5`

## 二、Fork 源代码

Fork 仓库：[notionnext-org/NotionNext](https://github.com/notionnext-org/NotionNext)（或你维护的 fork）。  
建议使用 Gmail 等国际邮箱注册 GitHub，避免 Vercel 注册受限。

## 三、Vercel 部署

1. 打开 [vercel.com/new](https://vercel.com/new)，导入你的 NotionNext 仓库。  
2. **先不要急着点 Deploy**：在 **Environment Variables** 添加：  
   - `NOTION_PAGE_ID` = 上一步的页面 ID  
3. 点击 **Deploy**，等待构建完成。  
4. 在 Dashboard → **Visit** 或 **Domains** 查看访问地址。

## 部署后无法拉取数据

1. Notion 页面是否已发布到 Web。  
2. Vercel 中 `NOTION_PAGE_ID` 是否正确；修改后需 **Redeploy**。  
3. 刷新页面 1～2 次（有 ISR/缓存时属正常）。

## 自定义站点

部署成功后，标题、菜单、主题等见 [如何配置站点](./config-site.md) 与 [菜单管理](./menu-secondary.md)。

## 费用与静态部署

访客暴增可能导致 Vercel 额度问题；可考虑静态导出方案（牺牲部分动态能力）。  
参考源站：[Vercel 静态部署](https://docs.tangly1024.com/article/vercel-deploy-notion-next-static)。

## 原文链接

https://docs.tangly1024.com/article/vercel-deploy-notion-next
