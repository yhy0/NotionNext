# NotionNext 开发先导

> 迁移自：[NotionNext开发先导](https://docs.tangly1024.com/article/how-to-develop-with-notion-next)

⚠️ **更完整的开发者文档**请以本仓库为准：

- [docs/developer/GETTING_STARTED.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/GETTING_STARTED.md)  
- [docs/ARCHITECTURE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/ARCHITECTURE.md)  
- [docs/PROJECT_STRUCTURE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/PROJECT_STRUCTURE.md)  
- [CONTRIBUTING.md](https://github.com/notionnext-org/NotionNext/blob/main/CONTRIBUTING.md)

## 环境

- **Node 20**（见 `.nvmrc`、`README`）  
- **Yarn**：`yarn` → `yarn dev`  
- 编辑器：VS Code 推荐

## 配置入口

- `blog.config.js` + `conf/*.config.js`  
- 各主题 `themes/<name>/config.js`  
- 自定义脚本：`public/js/custom.js`、`public/css/custom.css` 或 `CUSTOM_EXTERNAL_*`

## 云开发（Codespaces）

GitHub 仓库 → **Code** → **Codespaces** → Create → 终端 `yarn` → `yarn dev`。

## 本地开发

1. Clone 仓库（GitHub Desktop 或 `git clone`）  
2. `yarn` 安装依赖  
3. `.env.local` 配置 `NOTION_PAGE_ID` 等  
4. `yarn dev` → 浏览器打开 `http://localhost:3000`  

VS Code 可用 `.vscode/launch.json` 调试 Server / Client / Full Stack。

## 技术栈

- **Next.js**（Pages Router）— [Next.js 中文文档](https://www.nextjs.cn/docs/getting-started)  
- **Tailwind CSS** — 实用类样式  
- 主题代码主要在 `themes/`

## 代码规范

项目使用 ESLint + Prettier，保存时格式化（见源站 VS Code 插件说明）。

## 原文链接

https://docs.tangly1024.com/article/how-to-develop-with-notion-next
