# Twikoo 评论

> 迁移自：[Twikoo](https://docs.tangly1024.com/article/notionnext-twikoo)

## NotionNext 配置

| 变量名 | 值 |
| --- | --- |
| `NEXT_PUBLIC_COMMENT_ENV_ID` | 已部署的 Twikoo 服务地址（Vercel 填域名） |

可选：`NEXT_PUBLIC_COMMENT_TWIKOO_COUNT_ENABLE` 在列表显示评论数（耗性能，默认关）。

## 部署 Twikoo 后台

数据存储在 MongoDB。**请以 [Twikoo 官方文档](https://twikoo.js.org/backend.html) 为准**（源站 2022 年图文可能过时）。

概要：

1. [MongoDB Atlas](https://cloud.mongodb.com/) 免费集群，Network Access 允许 `0.0.0.0/0`（或按需收紧）  
2. 获取连接串，替换用户名密码  
3. Vercel 一键部署 Twikoo（见官方模板），设置 `MONGODB_URI`  
4. **Deployment Protection** 关闭，确保 API 可公开访问  
5. 将 Twikoo 域名填入 NotionNext 的 `NEXT_PUBLIC_COMMENT_ENV_ID` 并 Redeploy  

页内点击齿轮可设管理员密码。支持从 Valine 导入数据。

## 视频

[B 站 Twikoo Vercel 部署教程](https://www.bilibili.com/video/BV1Fh411e7ZH/)

## 原文链接

https://docs.tangly1024.com/article/notionnext-twikoo
