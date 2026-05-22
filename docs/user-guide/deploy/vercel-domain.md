# Vercel 绑定自定义域名

> 迁移自：[Vercel绑定自定义域名](https://docs.tangly1024.com/article/vercel-domain)

## 为什么要绑定

Vercel 默认 `*.vercel.app` 域名在大陆常被 DNS 污染，国内访问不稳定。绑定自己的域名可改善访问与 SEO。

## 购买域名

推荐 [NameSilo](https://www.namesilo.com/)（COM 约 $8.99/年，续费稳定，含免费隐私保护）。优惠码示例：`tangly1024a`（减 $1，以商家为准）。

支持支付宝 / PayPal / 信用卡。

## Vercel 添加域名

1. 项目 **Settings → Domains → Add**  
2. 输入域名后若显示 **Invalid Configuration**，按提示在 DNS 添加 **CNAME**（示例主机记录 `hexo` → `cname.vercel-dns.com`）

推荐使用 CNAME；大陆访问建议用 `cname-china.vercel-dns.com`（比默认 `cname.vercel-dns.com` 更快）。

## Cloudflare 托管（推荐）

将域名 **Nameserver** 改到 Cloudflare，在 CF 中：

1. 若无 A 记录：根域 **A** → `76.76.21.21`（Vercel）  
2. **CNAME** → `cname-china.vercel-dns.com`  
3. 若证书报错：先将代理改为「仅 DNS」（灰云），再在 **SSL/TLS** 开启 **完全（严格）** 加密

生效后 Vercel 域名卡片应显示正常。

## 根域名与 www

根域在 Vercel 添加后，DNS 将 `@` 解析到 `76.76.21.21`。个人博客常选：**www 重定向到根域**（如 `www.example.com` → `example.com`）。

## 写入 NotionNext

环境变量（Vercel **Settings → Environment Variables**，改后 Redeploy）：

| 变量名 | 示例 |
| --- | --- |
| `NEXT_PUBLIC_LINK` | `https://你的域名` |

也可在 Notion Config 表配置 `LINK`。

## 相关

- [Vercel 部署](./../deploy-vercel.md)  
- [Vercel 静态部署](./vercel-static.md)  
- [Vercel 域名加速](https://docs.tangly1024.com/article/vercel-accelerate)（源站）

## 原文链接

https://docs.tangly1024.com/article/vercel-domain
