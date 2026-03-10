# 个人求职网站 — Quarto Portfolio Site

一个专业、精美的个人求职网站，基于 Quarto 搭建，适合数据科学家、工程师等技术岗位求职使用。

---

## 📁 项目结构

```
portfolio-site/
├── _quarto.yml        # Quarto 项目配置（导航栏、主题、元数据）
├── styles.scss        # SCSS 主题变量（字体、颜色、基础样式）
├── custom.css         # 完整自定义样式（Hero、卡片、时间线等）
├── index.qmd          # 首页（Hero + 数据亮点 + 精选项目 + 技能）
├── about.qmd          # 关于我（简介 + 经历 + 教育 + 证书）
├── projects.qmd       # 项目展示（精选 + 更多项目卡片）
├── resume.qmd         # 简历页（一页式简历 + PDF 下载）
├── contact.qmd        # 联系方式（Email / LinkedIn / GitHub / Twitter）
└── README.md          # 本文件
```

---

## 🚀 快速开始

### 1. 安装 Quarto

前往 [quarto.org/docs/get-started](https://quarto.org/docs/get-started/) 下载并安装 Quarto CLI。

### 2. 本地预览

```bash
cd portfolio-site
quarto preview
```

浏览器会自动打开 `http://localhost:4000`，支持热更新。

### 3. 构建静态站点

```bash
quarto render
```

输出文件在 `_site/` 目录中，可直接部署。

---

## ✏️ 如何自定义

### 必须修改的内容

1. **`_quarto.yml`** — 把所有 `Your Name`、`yourusername`、`your.email@example.com` 替换为你自己的信息
2. **`index.qmd`** — 修改 Hero 区域的姓名、职位描述、数据亮点（年经验、项目数等）
3. **`about.qmd`** — 替换个人简介、工作经历、教育背景、证书
4. **`projects.qmd`** — 替换为你真实的项目（名称、描述、技术栈、链接）
5. **`resume.qmd`** — 替换简历内容，并放入真实的 PDF 下载链接
6. **`contact.qmd`** — 替换联系方式

### 添加头像

在 `about.qmd` 中，将 `.profile-photo-placeholder` 替换为真实图片：

```html
<!-- 替换这个 div -->
<img src="images/photo.jpg" alt="Your Name" 
     style="width:260px;height:320px;object-fit:cover;border-radius:12px;box-shadow:0 12px 40px rgba(0,0,0,0.08);">
```

### 修改颜色主题

在 `custom.css` 顶部的 `:root` 中修改 CSS 变量：

```css
:root {
  --color-primary: #1a1a2e;    /* 主色 */
  --color-accent: #4a6cf7;     /* 强调色 */
  --color-text: #2c2c3a;       /* 正文颜色 */
}
```

---

## 🌐 部署方式

### GitHub Pages（推荐）

1. 在 GitHub 创建仓库 `yourusername.github.io`
2. 将 `_site/` 内容推送到 `main` 分支，或使用 `gh-pages` 分支
3. 在仓库 Settings → Pages 中启用 GitHub Pages

```bash
quarto publish gh-pages
```

### Netlify

```bash
# 在 Netlify 设置中：
# Build command: quarto render
# Publish directory: _site
```

### Quarto Pub

```bash
quarto publish quarto-pub
```

---

## 🎨 设计特点

- **Playfair Display + DM Sans** 字体搭配：衬线标题 + 无衬线正文，专业且高级
- **柔和渐变 Hero** 区域，避免了 AI 生成的廉价紫色渐变
- **卡片式项目展示**，含标签、链接、hover 动效
- **时间线布局**，清晰展示职业与教育经历
- **全响应式设计**，在手机、平板、桌面端均表现良好
- **CSS 变量系统**，便于全局换色
- **纯 CSS 动效**，不依赖 JS 库，确保稳定性

---

## 📝 License

MIT — 随意使用和修改。
