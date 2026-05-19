# 最新版本与更新日志

> 当前主线：**4.9.5.3**（见根目录 `package.json`）

## 4.9.5.x 近期要点（相对旧版文档）

| 领域 | 变化 |
| --- | --- |
| **组织与仓库** | 主仓库迁至 [notionnext-org/NotionNext](https://github.com/notionnext-org/NotionNext) |
| **主题** | 新增 **ThoughtLite**；主题切换 manifest 与预览图规范 |
| **Notion** | 数据源/集合解析兼容；外部媒体（含 **Apple Music** 嵌入）规范化 |
| **构建** | `staticPaths` 缓存与导出稳定性；不可写缓存目录时回退 tmp；多站点 `NOTION_PAGE_ID` 构建期 `ENAMETOOLONG` 修复（缓存/锁文件短名） |
| **评论** | Notion Config 支持 **WALINE_*** 键名 |
| **置顶** | 全局 **TOP_TAG** 多置顶排序 |
| **安全** | 文章密码 **SHA256**（兼容旧 md5） |
| **Hexo** | 推荐卡片全图遮罩可读性修复 |
| **文档** | 仓库内 `docs/user-guide/` 用户手册、`DEPLOYMENT.md`、维护哲学文档 |

完整提交见 [GitHub Releases](https://github.com/notionnext-org/NotionNext/releases)。

## 如何升级

- 站长：[update.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/UPDATE.md)
- 开发者：[UPDATE.md（GitHub）](https://github.com/notionnext-org/NotionNext/blob/main/docs/developer/UPDATE.md)

## 历史版本全文

- [v4-history.md](./v4-history.md)（索引）
- 源站：https://docs.tangly1024.com/article/v4.0

## 原文链接

https://docs.tangly1024.com/article/latest
