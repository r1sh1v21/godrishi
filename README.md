# God Rishi

A minimalist, early-web / gothic personal static blog generator built with **Hugo**, pure **Raw CSS**, and automated deployment to **GitHub Pages**.

## Aesthetic & Architecture

- **Visuals**: Pure black (`#000000`), off-white typography (`#e0e0e0`), 1px structural borders (`#1a1a1a`).
- **Typography**: `UnifrakturMaguntia` for headings and titles, `Georgia` / `Times New Roman` for longform body prose.
- **Layout**: 3-column brutalist grid (80px empty sidebars + main content column).
- **Zero dependencies**: No CSS frameworks, no JavaScript bloat, no external animations or gradients.

## Adding New Posts

All posts are located in `content/posts/` as standard Markdown files.

### 1. Using the Hugo CLI:
```bash
hugo new content posts/my-new-post.md
```

### 2. Or manually create a `.md` file in `content/posts/`:
```markdown
---
title: "On the Nature of Solitude"
date: 2026-08-17T12:00:00Z
category: "Philosophy"
excerpt: "A short one-line summary of the essay."
draft: false
---

Your post content here in Markdown...
```

### 3. Images:
Place images in `static/images/` and reference them with standard Markdown:
```markdown
![Descriptive alt text](/images/monolith.jpg)
```

## Running Locally

To preview your site with live reloading:
```bash
hugo server -D
```
Open [http://localhost:1313/](http://localhost:1313/) in your browser.

## Deployment to GitHub Pages

1. Push your repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of God Rishi blog"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   git push -u origin main
   ```
2. In your GitHub repository settings:
   - Navigate to **Settings** > **Pages**
   - Under **Build and deployment** > **Source**, select **GitHub Actions**
3. On every push to the `main` branch, the `.github/workflows/deploy.yml` action will automatically build and publish your blog.
