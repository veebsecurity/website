# ShieldSmart — GitHub Pages Setup

Drop these files into your GitHub repository root and enable GitHub Pages.

## Quick Setup

### 1. Edit `_config.yml`
Update these two lines with your actual details:
```yaml
url: "https://yourusername.github.io"   # or your custom domain
baseurl: ""                              # set to "/repo-name" if not an org/user page
```

### 2. Enable GitHub Pages
In your repo: **Settings → Pages → Source → Deploy from a branch → `main` / `(root)`**

Your site will be live at `https://yourusername.github.io` (or `/repo-name`).

### 3. Local preview (optional)
```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

---

## Adding Content

### New blog post
Create `_posts/YYYY-MM-DD-title.md`:
```markdown
---
layout: post
title: "Your Title"
date: 2024-05-01
category: "Passwords"
excerpt: "One-line summary."
read_time: 5
difficulty: beginner
takeaway: "The one thing to remember."
related_tools:
  - "Bitwarden"
---
Your content here...
```

**Valid categories:** Passwords, Phishing, Updates, Privacy, Two-Factor Auth, Devices, Backups

### New tool
Add to `_data/tools.yml`:
```yaml
- name: "Tool Name"
  category: "VPN"
  price: "free"          # free | freemium | paid
  platforms: ["Windows", "macOS", "iOS", "Android", "Browser"]
  description: "Plain-language description."
  link: "https://example.com"
  rating: 4              # 1–5
```

---

## File Structure
```
.
├── _config.yml
├── Gemfile
├── index.md              ← Homepage
├── about.md              ← About/FAQ
├── blog/index.md         ← Blog listing
├── tools/index.md        ← Tools directory
├── _posts/               ← Add tip articles here
├── _data/tools.yml       ← Add tools here
├── _layouts/             ← Page templates (don't edit unless customising)
├── _includes/            ← Nav + footer partials
└── assets/css/style.css  ← All styles
```
