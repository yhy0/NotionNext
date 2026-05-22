 <div align="center">

<img src="https://github.com/user-attachments/assets/c111204d-2016-4343-92e4-83357cac4b19" width="96" height="96" alt="NotionNext Logo" />

# NotionNext

一个使用 Next.js + Notion API 构建的高颜值静态博客系统

为 Notion 与所有创作者设计 ✨

<p>
  <a href="https://preview.tangly1024.com/">
    在线预览
  </a>
  ·
  <a href="https://notionnext.tangly1024.com/">
    使用说明文档站
  </a>
  ·
  <a href="https://notionnext.tangly1024.com/user-guide/help/legacy-docs">
    旧版手册入口
  </a>
  ·
  <a href="./CONTRIBUTING.md">
    参与贡献
  </a>
  ·
  <a href="./docs/user-guide/community-participate.md">
    参与社区
  </a>
  ·
  <a href="./GOVERNANCE.zh-CN.md">
    项目治理
  </a>
</p>

</div>

---
# 使用说明文档站（新）

自 **2026 年起**，站长向教程在仓库内维护，并发布为独立静态站：

| | |
| --- | --- |
| **在线阅读** | [https://notionnext.tangly1024.com](https://notionnext.tangly1024.com) |
| **源码目录** | [docs/](https://github.com/notionnext-org/NotionNext/tree/main/docs)（[`docs/README.md`](./docs/README.md) 含维护与部署说明） |
| **参与修改** | 文档页底部「在 GitHub 上维护此页」→ 编辑后合并 `main` 即自动部署 |

本地预览文档站：`yarn docs:site:dev` · 构建：`yarn docs:site:build`

---

# 帮助教程

- **在线文档站（推荐）**：[notionnext.tangly1024.com](https://notionnext.tangly1024.com) · 仓库目录 [docs/user-guide/](./docs/user-guide/)
- **4.9.x 参考手册**：[全站配置索引](./docs/user-guide/reference/features.md) · [25 个主题说明](./docs/user-guide/themes/) · [本地预览文档站](./docs/user-guide/WEBSITE.md)（`yarn docs:site:dev`）
- **文档维护工作流**：[docs/user-guide/MAINTENANCE_WORKFLOW.md](./docs/user-guide/MAINTENANCE_WORKFLOW.md)（目录秩序、检查清单、注意事项）
- **维护策略**：[docs/DOCUMENTATION_POLICY.md](./docs/DOCUMENTATION_POLICY.md)
- **旧版手册**：[docs.tangly1024.com](https://docs.tangly1024.com/) · [slug 对照与迁移索引](./docs/user-guide/help/legacy-docs.md)（重要章节已迁入 `docs/user-guide/`）

> 本项目为免费、公开资源，仅限个人学习使用，禁止利用本教程建立的博客发布非法内容、进行违法犯罪活动。

Notion是一个能让效率暴涨的生产力引擎，可以帮你书写文档、管理笔记，搭建知识库，甚至可以为你规划项目、时间管理、组织团队、提高生产力、还有当前最强大的AI技术加持。

# NotionNext

<p>
  <a aria-label="GitHub commit activity" href="https://github.com/notionnext-org/NotionNext/commits/main" title="GitHub commit activity">
    <img src="https://img.shields.io/github/commit-activity/m/notionnext-org/NotionNext?style=for-the-badge"/>
  </a>
  <a aria-label="GitHub contributors" href="https://github.com/notionnext-org/NotionNext/graphs/contributors" title="GitHub contributors">
    <img src="https://img.shields.io/github/contributors/notionnext-org/NotionNext?color=orange&style=for-the-badge"/>
  </a>
  <a aria-label="Build status" href="#" title="Build status">
    <img src="https://img.shields.io/github/deployments/notionnext-org/NotionNext/Production?logo=Vercel&style=for-the-badge"/>
  </a>
  <a aria-label="Powered by Vercel" href="https://vercel.com?utm_source=Craigary&utm_campaign=oss" title="Powered by Vercel">
    <img src="https://www.datocms-assets.com/31049/1618983297-powered-by-vercel.svg" height="28"/>
  </a>
</p>

中文文档 | [README in English](./README_EN.md)

<hr/>

一个使用 NextJS + Notion API 实现的，部署在 Vercel 上的静态博客系统。为Notion和所有创作者设计。

**仓库托管：** 主仓库现由 GitHub 组织 **[notionnext-org](https://github.com/notionnext-org)** 维护（canonical：`https://github.com/notionnext-org/NotionNext`）。欢迎参与贡献并关注组织内协作说明；若在转让前已克隆本地仓库，建议执行 `git remote set-url origin https://github.com/notionnext-org/NotionNext.git` 后使用 `git remote -v` 确认。

支持多种部署方案

## 新开发者 3 分钟上手

```bash
# 1) 使用 Node 20（建议先安装 nvm）
nvm use || nvm install

# 2) 安装 Yarn（若未安装）
npm i -g yarn

# 3) 安装依赖并启动开发
yarn
yarn dev
```

常用命令：

- 本地开发：`yarn dev`
- 打包构建：`yarn build`
- 静态导出：`yarn export`

说明：本地开发保持简单（`yarn` 即可）；锁文件一致性由 CI 严格校验。

## 参与社区

项目由 **[notionnext-org](https://github.com/notionnext-org)** 托管，欢迎站长与开发者共同维护。

| | |
| --- | --- |
| **参与指南** | [docs/user-guide/community-participate.md](./docs/user-guide/community-participate.md)（在线：[参与社区](https://notionnext.tangly1024.com/user-guide/community-participate)） |
| **贡献代码/文档** | [CONTRIBUTING.zh-CN.md](./CONTRIBUTING.zh-CN.md) |
| **项目治理** | [GOVERNANCE.zh-CN.md](./GOVERNANCE.zh-CN.md) · [MAINTAINERS.md](./MAINTAINERS.md) |
| **行为准则** | [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) |
| **维护者手册** | [MAINTAINER_RUNBOOK](./docs/developer/MAINTAINER_RUNBOOK.zh-CN.md) |
| **讨论** | [GitHub Discussions](https://github.com/notionnext-org/NotionNext/discussions) |

## 开发者文档导航

为方便新贡献者快速上手，项目已补充文档导航与协作规范：

- [文档导航入口（中文）](./docs/README.md)
- [开发者文档](./docs/developer/README.md)
- [贡献入口（中文）](./CONTRIBUTING.zh-CN.md)
- [贡献入口（英文）](./CONTRIBUTING.md)
- [RFC 与大改动流程](./docs/developer/rfc/README.md)

## 主题与预览

- **在线切换主题**：[preview.tangly1024.com](https://preview.tangly1024.com/)（左下角挂件）
- **25 个内置主题说明**：[docs/user-guide/themes/THEMES_CATALOG.md](./docs/user-guide/themes/THEMES_CATALOG.md)
- 想贡献新主题？见 [CONTRIBUTING.zh-CN.md](./CONTRIBUTING.zh-CN.md) 与 [主题迁移指南](./docs/developer/THEME_MIGRATION_GUIDE.zh-CN.md)

## 致谢

感谢Craig Hart发起的Nobelium项目

<table><tr align="left">
  <td align="center"><a href="https://github.com/craigary" title="Craig Hart"><img src="https://avatars.githubusercontent.com/u/10571717" width="64px;"alt="Craig Hart"/></a><br/><a href="https://github.com/craigary" title="Craig Hart">Craig Hart</a></td>
</tr></table>

## 贡献者

致敬每一位开发者！

[![Contributors](https://contrib.rocks/image?repo=notionnext-org/NotionNext)](https://github.com/notionnext-org/NotionNext/graphs/contributors)

## 引用技术

- **框架**: [Next.js](https://nextjs.org)
- **样式**: [Tailwind CSS](https://www.tailwindcss.cn/)
- **渲染**: [React-notion-x](https://github.com/NotionX/react-notion-x)
- **评论**: [Twikoo](https://github.com/imaegoo/twikoo), [Giscus](https://giscus.app/zh-CN), [Gitalk](https://gitalk.github.io), [Cusdis](https://cusdis.com), [Utterances](https://utteranc.es)
- **图标**: [Fontawesome](https://fontawesome.com/v6/icons/)

## 🔗 友情链接

- [Elog](https://github.com/LetTTGACO/elog) Markdown 批量导出工具、开放式跨平台博客解决方案，随意组合写作平台(语雀/Notion/FlowUs/飞书)和博客平台(Hexo/Vitepress/Halo/Confluence/WordPress等)

## License

The MIT License.

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=notionnext-org/NotionNext&type=Date)](https://star-history.com/#notionnext-org/NotionNext&Date)
