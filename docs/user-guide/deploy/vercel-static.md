# Vercel 静态部署 NotionNext

> 迁移自：[Vercel静态部署NotionNext](https://docs.tangly1024.com/article/vercel-deploy-notion-next-static)

## 适用场景

站点访客暴增导致 Vercel **Function Execution** 用量超标时，可改为**纯静态导出**：Vercel 只托管 HTML/资源，不再每次请求都跑函数拉 Notion。

代价：文章更新后需手动 **Redeploy**（或配置 Webhook），无法像 ISR 那样自动增量更新。

## 配置方式

Vercel 项目 **Settings → General → Build Command** 改为：

```bash
yarn export
```

（与默认 `yarn build` 不同，会生成静态站点。）

构建若出现 Notion API 过慢或 `timeout of 300 seconds`，见 **[构建性能调优](./build-tuning.md)**。

## 另一种静态方案

[Cloudflare Pages 静态部署](./cloudflare-pages.md) 同样为导出后部署，更新内容后需重新构建。

## 重新部署

内容变更后：Vercel **Deployments → Redeploy**。详见源站 [vercel-redploy](https://docs.tangly1024.com/article/vercel-redploy)。

## 原文链接

https://docs.tangly1024.com/article/vercel-deploy-notion-next-static
