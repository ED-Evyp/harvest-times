# 🌾 Harvest Times

An earthy, editorial-style agricultural news website — built to be hosted for free on **GitHub Pages**.

## Project Structure

```
harvest-times/
├── index.html          ← The entire website (one file)
├── articles.json       ← Index of all articles (edit this when adding new ones)
├── articles/
│   ├── 2026-03-18-spring-planting-guide.md
│   ├── 2026-03-10-olive-oil-prices.md
│   └── 2026-03-05-bee-recovery.md
└── README.md
```

---

## 🚀 How to Publish on GitHub Pages

### First time setup

1. **Create a GitHub account** at [github.com](https://github.com) if you don't have one.

2. **Create a new repository**:
   - Go to github.com → click **"New"** (green button)
   - Name it: `harvest-times` (or anything you like)
   - Set it to **Public**
   - Click **"Create repository"**

3. **Upload your files**:
   - Click **"uploading an existing file"** on the repo page
   - Drag and drop ALL the files and the `articles/` folder
   - Click **"Commit changes"**

4. **Enable GitHub Pages**:
   - Go to your repo → **Settings** → **Pages** (left sidebar)
   - Under "Branch", select `main` → `/ (root)` → click **Save**
   - Wait ~1 minute, then your site will be live at:
     `https://YOUR-USERNAME.github.io/harvest-times/`

---

## ✍️ How to Add a New Article

### Step 1 — Create the Markdown file

Create a new file in the `articles/` folder. Name it with the date and a short title:

```
articles/2026-04-01-new-article-title.md
```

Every article starts with a **front matter block** (the bit between the `---` lines), followed by the article body in Markdown:

```markdown
---
title: Your Article Title Here
date: 2026-04-01
author: Your Name
category: Seasonal Guide
excerpt: A one or two sentence summary of the article shown on the home page.
image: https://images.unsplash.com/photo-XXXXXXXXX?w=800&q=80
---

Your article content goes here. Write in **Markdown** format.

## A Section Heading

A paragraph of text. You can use **bold**, *italic*, and more.

- Bullet point one
- Bullet point two
```

**Category options** (or create your own):
- `Seasonal Guide`
- `Market Watch`
- `Ecology`
- `Technology`
- `Policy`

**Free images**: Get a URL from [Unsplash](https://unsplash.com) — right-click any photo → "Copy image address", then add `?w=800&q=80` at the end.

### Step 2 — Add it to `articles.json`

Open `articles.json` and add a new entry at the **top** of the list (so it appears first):

```json
{
  "file": "articles/2026-04-01-new-article-title.md",
  "title": "Your Article Title Here",
  "date": "2026-04-01",
  "author": "Your Name",
  "category": "Seasonal Guide",
  "excerpt": "A one or two sentence summary shown on the home page.",
  "image": "https://images.unsplash.com/photo-XXXXXXXXX?w=800&q=80"
}
```

### Step 3 — Upload to GitHub

Go to your repository on GitHub, click **"Add file"** → **"Upload files"**, upload your new `.md` file and the updated `articles.json`. That's it — the site updates automatically.

---

## 📝 Markdown Quick Reference

| What you type | What it looks like |
|--------------|-------------------|
| `**bold**` | **bold** |
| `*italic*` | *italic* |
| `## Heading` | A section heading |
| `- item` | • Bullet list item |
| `[link text](https://url.com)` | A hyperlink |

---

*Built with love for the land. No frameworks, no build step — just HTML, CSS, and Markdown.*
