# 佳硕 · 个人作品集网站

线上地址：**https://sunjiashuo-69.github.io**

托管方式：GitHub Pages（main 分支根目录，push 即自动部署，约 1 分钟生效；CDN 偶有 1-2 分钟延迟，验证时加 `?v=N` 参数强刷）。无构建步骤、无依赖、无框架。

## 文件结构

```
index.html        # 首页（全部样式内嵌，无构建）
hok.html          # HOK KIS4 项目详情页（金色系 STAR 结构）
kayou.html        # 卡游 × MLBB 项目详情页（黄色系 STAR 结构）
assets/
  hok_bg.jpg      # HOK 详情页首屏背景（1920×1080）
  mlbb_char.png   # 卡游页英雄立绘
  slide-hok.png   # HOK 复盘 PPT 原片（1600×900）
  slide-kayou.png # 卡游复盘 PPT 原片（1600×900）
README.md         # 本说明
```

## 修改内容速查

| 想改什么 | 在哪里改 |
|---|---|
| 首页主标题/简介 | `index.html` 的 `<h1>` 和 `.hero p.sub`（两段） |
| Open to work 徽章 | `index.html` 的 `.badge` |
| 项目卡片 | `index.html` 的 `<section id="projects">` 里 `<article class="card">` |
| AI 工作流板块 | `index.html` 的 `.ai-band` 里 `.ai-item` |
| 联系方式/寻求新机会 | `index.html` 的 `<section id="contact">`（QQ/Gmail 为 mailto 直达，微信点击复制 s1264024887） |
| 详情页 STAR 内容 | `hok.html` / `kayou.html` 里搜 `SITUATION / TASK`（S/T 卡片）、`ACTION`（打法）、`RESULT`（成果）、`TAKEAWAY`（方法论） |
| 详情页主色 | 各文件 `:root` 的 `--accent`（HOK 金色 #ffd100，卡游黄色 #ffd100） |
| 复盘 PPT 原片图 | `assets/slide-hok.png` / `slide-kayou.png`（直接替换同名文件，1600×900） |
| 页面标题/SEO | 各文件 `<title>` 和 `<meta name="description">` |

## 本机免登录说明（重要）

这台电脑已配置好 GitHub 推送凭证，任何 AI 工具（WorkBuddy / Codex / Claude Code 等）**无需再登录**：

- macOS 钥匙串存有 Personal Access Token（账户 `sunjiashuo-69`，名为 `catpaw-github-push`），标准 git 凭证条目也已写入，`git push` 直接可用；
- 环境变量 `GH_TOKEN` 已在 `~/.zshrc` / `~/.zprofile` 配置（从钥匙串读取），沙箱环境里拿不到钥匙串时可以用它；
- 网络偶发抖动时，用 `git -c http.version=HTTP/1.1 push` 重试 2-3 次即可。

## 在 WorkBuddy 上承接修改（推荐流程）

1. **打开项目**：让 WorkBuddy 把工作目录指向本文件夹（`~/Desktop/雅思学习计划/portfolio-site`）。它就是 git 仓库本身，不需要重新 clone。
2. **直接说需求**：例如「把首页 hero 的第二段简介改成……」「卡游详情页加一条打法」。改动只涉及 HTML 纯文本，任何 AI 都能处理。
3. **让它提交推送**：「commit 并 push 到 GitHub」。push 成功后约 1 分钟线上生效。
4. **验收**：浏览器打开 https://sunjiashuo-69.github.io 强刷（Cmd+Shift+R），或加 `?v=1` 参数绕过 CDN 缓存。

如果是全新环境（换了电脑），先 `git clone https://github.com/sunjiashuo-69/sunjiashuo-69.github.io.git`，再让 AI 引导完成一次 GitHub 授权（HTTPS Personal Access Token，repo 权限即可）。

## 注意事项

- 内容保持脱敏：不放公司内部系统名、客户敏感信息、未脱敏数据。
- 纯静态单文件是刻意的：任何工具都能改，不需要 Node/构建环境，永不失效。
- 想换更高级的技术栈（如 Astro/Next）也可以，但请确保 GitHub Pages 的部署配置仍然可用。
