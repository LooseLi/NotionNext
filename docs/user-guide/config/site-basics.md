# 站点基础配置（功能总览）

> 迁移自：[基础信息](https://docs.tangly1024.com/article/notion-next-guide)  
> **完整配置键列表**见 [reference/features.md](../reference/features.md)（与 `conf/*.config.js` 同步）

本文补充 [如何配置站点](../config-site.md) 未展开的日常选项。

## 站点信息与社交

- 作者、站点 URL、联系方式：Notion Config 或 `conf/contact.config.js`  
- Hexo / Next 等主题会在侧栏展示 `CONTACT_*` 配置的社交按钮（Font Awesome 类名见 [fontawesome.com](https://fontawesome.com/search?m=free)）  
- **LINK** 用于分享条、RSS、Sitemap，务必设为真实域名

## 多语言

- 默认语言：`LANG`（`blog.config.js` / 环境变量）  
- 支持：`en-US`、`zh-CN`、`zh-HK`、`zh-TW`、`fr-FR`、`tr-TR`、`ja-JP` 等  
- 预览：`https://preview.tangly1024.com/?lang=en-US`  
- **两个 Notion 数据库之间的正文同步**（可选 CLI，会先 `--dry-run` 再写入）：见 [双语库翻译 CLI](../notion/bilingual-translator.md)

## 站点图标

替换 `public/favicon.ico`（可用在线 ICO 生成工具，建议 48×48）。

## 自定义 CSS / JS

| 方式 | 位置 |
| --- | --- |
| 全局外链 | `CUSTOM_EXTERNAL_CSS` / `CUSTOM_EXTERNAL_JS` |
| 仓库文件 | `public/css/custom.css`、`public/js/custom.js` |
| 主题样式 | `public/css/theme-<主题名>.css` |
| Notion Config | `GLOBAL_CSS`、`GLOBAL_JS`（4.2.0+） |

## 文章路径

- 默认：`/article/[slug]`（由 `POST_URL_PREFIX` 等控制）  
- `POST_URL_PREFIX` 为空 → `/[slug]`；为 `post` → `/post/[slug]`  
- 语义化 URL、分类映射见 [URL 自定义](./url-customize.md)

## Notion 字段名

可在配置中把 Notion 属性名改为中文表头，见 `blog.config.js` 中 `NOTION_PROPERTY_NAME`。

## 菜单

见 [菜单管理](../menu-secondary.md)。

## 伪静态与缓存

- 页面本身为 Next 静态/ISR 输出  
- `NEXT_REVALIDATE_SECOND`：缓存多久后从 Notion 再同步  
- `PSEUDO_STATIC=true`：URL 以 `.html` 结尾（视觉更像传统静态站）

## 列表与代码块

- 分页 / 无限滚动、`POSTS_PER_PAGE`、列表是否显示摘要  
- `PRISM_THEME_PATH`：代码高亮主题（见 [prism-themes](https://github.com/PrismJS/prism-themes)）  
- `CODE_MAC_BAR`、`CODE_LINE_NUMBERS`：Mac 窗口装饰、行号

## Notion 隐私

已发布到 Web 的页面他人默认只有**查看**权限，除非您主动开放编辑/评论。

## 原文链接

https://docs.tangly1024.com/article/notion-next-guide
