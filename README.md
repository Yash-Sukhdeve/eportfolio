# Undergrad E-Portfolio Tutorial

This is a plain HTML/CSS portfolio template built for a workshop talk. No frameworks, no npm, no build step — just files you open in a browser.

**Live demo:** `https://yash-sukhdeve.github.io/undergrad-eportfolio-tutorial/`

![QR code to live site](qr-code.png)

---

## Files

| File | What it is |
|------|------------|
| `index.html` | Home page — your name, bio, and a quick intro |
| `projects.html` | Project cards with tech badges and GitHub links |
| `skills.html` | Skill progress bars and a soft skills list |
| `resume.html` | Education and experience as a vertical timeline |
| `contact.html` | Contact form and links to your profiles |
| `css/style.css` | One stylesheet for all pages — change 4 variables to retheme |
| `templates/` | 6 themed templates — pick the one that suits your field |
| `AI_PROMPTS.md` | Prompts you can paste into ChatGPT or Claude to build/edit any part |
| `HOSTING_GUIDE.md` | Step-by-step guide to put your portfolio live — written for beginners |
| `generate_qr.py` | Regenerates `qr-code.png` if you change the URL |

---

## Themed templates

There are 6 ready-to-use templates for different fields, each with a distinct look:

| Template | Field | Theme |
|----------|-------|-------|
| `template-cs.html` | Computer Science / SWE | Dark · neon green · monospace |
| `template-design.html` | Design / UX / Creative Arts | Warm cream · bold coral · editorial serif |
| `template-data.html` | Data Science / ML | Deep navy · electric teal · dot-grid |
| `template-bio.html` | Biology / Life Sciences / Pre-Med | Warm organic · forest green · terracotta |
| `template-business.html` | Business / Finance / Consulting | Dark luxury · warm gold · classical serif |
| `template-arch.html` | Architecture / Civil / Urban Design | Stark Bauhaus · construction red · bold type |

Open `templates/index.html` to preview all six side by side, or click directly into any template file.

To use a template as your main page, copy its contents into `index.html` and replace the placeholder text.

---

## Getting started

**New to GitHub?** Read [`HOSTING_GUIDE.md`](HOSTING_GUIDE.md) first — it walks through everything from creating an account to adding photos and going live.

Quick version if you already know the basics:

1. **Fork** this repo (button top-right on GitHub).
2. Go to **Settings → Pages → Source → main branch / root** and hit save.
3. Your site goes live at `https://<your-username>.github.io/undergrad-eportfolio-tutorial/` in about a minute.
4. Edit the files and replace the placeholder text.

---

## Changing the colour scheme

At the top of `css/style.css` there are four variables. Change them and every button, link, and highlight on every page updates.

```css
:root {
  --accent:      #2563eb;   /* main colour */
  --accent-dark: #1d4ed8;   /* hover state */
  --bg:          #f8fafc;   /* page background */
  --surface:     #ffffff;   /* card background */
}
```

---

## Talk outline

| # | Topic |
|---|-------|
| 1 | Why bother with a portfolio — what employers and grad schools actually look for |
| 2 | What pages to include and what to put on each |
| 3 | HTML and CSS basics — structure vs style |
| 4 | Walkthrough of this template |
| 5 | Putting it live with GitHub Pages |
| 6 | How to make it your own |

---

## Customisation checklist

Work through this after you fork:

- [ ] Replace `Your Name` everywhere
- [ ] Add your photo in `index.html` (or remove the placeholder)
- [ ] Put your real projects in `projects.html`
- [ ] Fix the skill percentages in `skills.html`
- [ ] Add your actual education and experience in `resume.html`
- [ ] Update GitHub, LinkedIn, and email links in `contact.html`
- [ ] Sign up at [formspree.io](https://formspree.io), get a form ID, and paste it into `contact.html`
- [ ] Add a real `resume.pdf` and link it in `resume.html`
- [ ] Pick a colour — change `--accent` in `style.css`

---

## Why no JavaScript?

The mobile nav, progress bar animations, and hover effects all work with CSS only. This keeps the template simple to understand and edit — no node_modules to install, no build step to break, works offline. If you want to add JS later, `AI_PROMPTS.md` has prompts for scroll progress bars, copy buttons, and project filters.

---

## Regenerating the QR code

If you rename the repo, update the URL in `generate_qr.py` then run:

```bash
pip install qrcode[pil]
python generate_qr.py
git add qr-code.png && git commit -m "update qr code"
```
