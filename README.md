# 佳硕 · 个人作品集网站

线上地址：**https://sunjiashuo-69.github.io**

托管方式：GitHub Pages（main 分支根目录，push 即自动部署，约 1 分钟生效）。无构建步骤、无依赖、无框架。

## 文件结构

只有两个文件需要关心：

- `index.html` — 整个网站（HTML + CSS 内嵌，无 JS）。改内容只动这一个文件。
- `README.md` — 本说明，给后续维护者（人或 AI）看。

## 修改内容速查

| 想改什么 | 在 index.html 里找 |
|---|---|
| 主标题/一句话介绍 | `<h1>` 和 `.hero p.sub` |
| 三个项目卡片 | `<section id="projects">` 里的 `<article class="card">` |
| AI 能力板块 | `<section id="ai">` 里的 `.ai-item` |
| 联系方式（目前是占位符） | `<section id="contact">` 里的 `your-email@example.com` / `your-wechat-id` |
| 主色（美团黄） | CSS `:root` 里的 `--accent: #ffd100` |
| 页面标题/SEO | `<title>` 和 `<meta name="description">` |

## 标准修改流程（给 AI 工具 / 开发者）

```bash
# 1. 克隆（首次）
git clone https://github.com/sunjiashuo-69/sunjiashuo-69.github.io.git
cd sunjiashuo-69.github.io

# 2. 修改 index.html 后本地预览：直接双击 index.html 或
open index.html

# 3. 提交并推送（push 后网站自动更新）
git add index.html
git commit -m "update: 修改说明"
git push
```

推送需要 GitHub 身份验证（HTTPS Personal Access Token，repo 权限即可；或 SSH key）。首次在本机用 AI 工具操作时，让 AI 引导你完成 GitHub 登录授权即可。

## 注意事项

- 内容保持脱敏：不放公司内部系统名、客户敏感信息、未脱敏数据。
- 纯静态单文件是刻意的：任何工具都能改，不需要 Node/构建环境，永不失效。
- 想换更高级的技术栈（如 Astro/Next）也可以，但请确保 GitHub Pages 的部署配置仍然可用。
