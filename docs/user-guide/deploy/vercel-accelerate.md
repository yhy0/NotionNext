# Vercel 域名加速（国内访问）

> 迁移自：[Vercel域名加速](https://docs.tangly1024.com/article/vercel-accelerate)

## 要点

- CNAME 使用 **`cname-china.vercel-dns.com`**（优于默认 `cname.vercel-dns.com`）  
- 根域 A 记录可指向 `76.76.21.21` 或 `76.223.126.88` 等（以 Vercel 当前提示为准）  
- 配合 [Cloudflare](./vercel-domain.md) 与 SSL 完全加密

也可使用社区 CDN 方案进一步优化大陆访问（见源站正文）。

## 原文链接

https://docs.tangly1024.com/article/vercel-accelerate
