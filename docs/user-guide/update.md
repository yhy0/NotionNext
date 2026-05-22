# NotionNext 升级教程

> 迁移自：[NotionNext-升级教程](https://docs.tangly1024.com/article/how-to-update-notionnext)  
> 仓库内另见：[UPDATE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/UPDATE.md)（双分支策略）

## 版本号

三位数字如 `4.9.5`：

- 第一位：大版本 / 架构变更，需谨慎。  
- 第二位：新功能，可能改动 `blog.config.js`、主题 config。  
- 第三位：补丁与 bug 修复。

## 升级前建议

- 大量自定义代码：备份或专用分支；或尽量用 **Notion Config** 减少改代码。  
- Vercel 每次部署保留源码快照，可在 Deployment → 旧记录 → View Source 找回。

## 简单更新（GitHub Fork）

仓库页可能显示：

1. **Fetch upstream** → **Fetch and merge**  
2. **Sync fork** → **Update branch**  
3. 有冲突：需手动处理（见下）

### 冲突时

- **Discard commits**：放弃本地修改以同步上游（先备份 `blog.config.js` 等）。  
- **Open Pull Request**：向官方提交贡献。

不熟悉 Git：备份配置 → 重新 Fork → 填回 `NOTION_PAGE_ID` 与环境变量（文章在 Notion 中，重建较快）。

## 部署未更新

1. 看 Vercel **Deployments** 是否 **Error**。  
2. 点开记录查看构建日志，按报错改代码后 Redeploy。  
3. 页面版本号旧：确认成功部署的是最新 commit。

## 寻求帮助

- [留言反馈](https://docs.tangly1024.com/article/how-to-question)  
- 官方社群（见源站「获取帮助」栏目）

## 原文链接

https://docs.tangly1024.com/article/how-to-update-notionnext
