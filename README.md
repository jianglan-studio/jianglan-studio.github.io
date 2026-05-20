# 774279441aa-beep.github.io

个人摄影/艺术作品集，纯静态 HTML + CSS，部署在 GitHub Pages。

URL: <https://774279441aa-beep.github.io/>

## 怎么改

### 换姓名 / 简介 / 联系方式

打开 `index.html`，搜索 `TODO` 注释，把对应位置改成你自己的内容：
- 网站标题（H1）
- 一句话定位（tagline）
- About 段落
- Email / Instagram / GitHub 链接

### 换图片

#### 方案 A：换 Unsplash 的图（最快）
打开 `index.html`，找到 `<img src="...">`，把 URL 里 `photo-XXXXX` 那一段换成另一张 Unsplash 图片的 ID。

#### 方案 B：用自己的图（推荐长期方案）
1. 把图片放进 `images/` 目录（比如 `images/01.jpg`、`images/02.jpg`）
2. 建议尺寸 1200×1500 px、JPEG/WebP、< 300 KB
3. 把 `index.html` 里对应 `<img src="https://...">` 改成 `<img src="images/01.jpg">`
4. 别忘了改 `alt` 属性，描述图片内容（无障碍 + SEO）

### 加新作品

在 `index.html` 的 `<ul class="grid">` 里复制粘贴一个 `<li class="work">...</li>` 块即可。

### 改风格

`styles.css` 顶部 `:root` 是所有可调参数：
- `--bg` / `--ink` / `--ink-soft` / `--line` — 配色
- `--font-serif` / `--font-sans` — 字体
- `--s-1` ~ `--s-5` — 间距阶梯

## 发布更新

```bash
cd ~/774279441aa-beep.github.io
git add .
git commit -m "update works"
git push
```

push 后 GitHub Pages 会在 1-2 分钟内自动更新线上版本。

## 本地预览

```bash
cd ~/774279441aa-beep.github.io
python3 -m http.server 8000
```

然后浏览器打开 <http://localhost:8000>。
