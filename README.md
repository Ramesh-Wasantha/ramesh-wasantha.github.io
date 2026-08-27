# Ramesh Wasantha — Hugo Terminal Portfolio

This is a Hugo-based replacement for the previous Jekyll Minimal portfolio. It uses the **panr/hugo-theme-terminal v4.2.3** theme with a professional dark blue/cyan customization for a DevOps / Platform / AI Infrastructure portfolio.

## What changed

- Replaced the old Jekyll `_config.yml` setup with `hugo.toml`.
- Reorganized the portfolio into Home, Projects, Experience, Skills, Certifications, About, and Contact.
- Converted the long online-CV layout into a recruiter-friendly project portfolio.
- Added a GitHub Actions workflow that builds Hugo and deploys the generated `public/` site to GitHub Pages.
- Added a custom Terminal color palette and portfolio-specific CSS.

## Repository setup

Copy the contents of this folder into your `ramesh-wasantha.github.io` repository.

### 1. Remove the old Jekyll theme config

Delete the old `_config.yml` once you switch to Hugo. The new configuration is `hugo.toml`.

### 2. Keep your profile photo (optional)

Your old Jekyll config referenced:

`/assets/img/propic.png`

If that image already exists in your repository, move it to:

`static/assets/img/propic.png`

The home page checks for this file automatically. If it is missing, the site still renders correctly without a photo.

### 3. Enable GitHub Actions for Pages

In GitHub:

**Repository → Settings → Pages → Build and deployment → Source → GitHub Actions**

Then push these files to `main`. The workflow in `.github/workflows/hugo.yml` builds and deploys the site automatically.

## Local preview

Install Hugo Extended and Go, then run:

```bash
hugo mod get github.com/panr/hugo-theme-terminal/v4@v4.2.3
hugo server -D
```

Open `http://localhost:1313/`.

## Main files

- `hugo.toml` — site configuration and navigation
- `content/_index.md` — homepage / hero section
- `content/projects/` — featured projects
- `content/experience.md` — work experience
- `content/skills.md` — technical skills
- `content/certifications.md` — certifications
- `content/about.md` — professional summary and education
- `content/contact.md` — social/contact links
- `static/terminal.css` — Terminal theme palette
- `static/style.css` — portfolio styling overrides
- `.github/workflows/hugo.yml` — GitHub Pages deployment

## Before publishing

Review the dates and project descriptions to make sure they match your CV and LinkedIn exactly.
