# How to Create New Content

Your website supports both **Blog Posts** and **Portfolio Items**.

## 1. Quick Start (Terminal)
The easiest way is to use the Hugo command line.

### Create a New Blog Post
Run this command from the root of your project:
```bash
hugo new content/english/post/my-new-post-title.md
```

### Create a New Portfolio Item
```bash
hugo new content/english/portfolio/my-project-name.md
```

---

## 2. Editing Your Content
Open the newly created file in your editor (VS Code, etc.). You will see a "front matter" block at the top, like this:

```yaml
---
title: "My New Post Title"
date: 2025-12-15T19:54:00+05:30
draft: true
---
```

### Important Fields
- **title**: The title that appears on the page.
- **date**: The publication date.
- **draft**: Set this to `false` when you are ready to publish! If safe as `true`, it will only show up when running `hugo server -D`.

### Adding Content
Write your article content below the second `---` line using standard Markdown.

```markdown
## Introduction
This is my new post content...

- Point 1
- Point 2
```

---

## 3. Previewing
Run the local server to see your changes immediately:
```bash
hugo server -D
```
*(The `-D` flag allows you to see draft posts)*

## 4. Publishing
When you are ready to go live:
1.  Change `draft: true` to `draft: false` in your file.
2.  Run these commands in your terminal:

```bash
git add .
git commit -m "Add new post: My New Post Title"
git push origin main
```
Your GitHub Actions workflow will automatically deploy the changes.
