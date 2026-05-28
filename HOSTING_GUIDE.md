# How to Put Your Portfolio Live on GitHub Pages

This guide takes you from zero — no GitHub account, no coding experience — to a live portfolio URL you can share with anyone.

By the end you will have a URL that looks like:
`https://your-username.github.io/undergrad-eportfolio-tutorial/`

---

## What You Need

- A laptop or desktop computer (Windows, Mac, or Linux)
- A browser
- An email address to create a GitHub account

That's it. You don't need to install anything.

---

## Part 1 — Understand the Folder Structure

Before anything else, understand what the files are and where things go.

```
undergrad-eportfolio-tutorial/
│
├── index.html          ← Your HOME PAGE. This is what loads when someone visits your URL.
├── projects.html       ← Projects page
├── skills.html         ← Skills page
├── resume.html         ← Resume / timeline page
├── contact.html        ← Contact page
│
├── css/
│   └── style.css       ← The stylesheet that controls ALL the colours and layout
│
├── images/             ← CREATE THIS FOLDER for your photos and project screenshots
│   ├── profile.jpg     ← Your profile photo (name it exactly this, or update the HTML)
│   ├── project1.png    ← Screenshot of your first project
│   └── project2.png    ← Screenshot of your second project
│
├── resume.pdf          ← Your CV as a PDF (name it exactly this, or update the HTML)
│
├── templates/          ← The 6 themed starter templates
│   ├── index.html      ← Gallery page showing all 6 themes
│   ├── template-cs.html
│   ├── template-design.html
│   ├── template-data.html
│   ├── template-bio.html
│   ├── template-business.html
│   └── template-arch.html
│
├── README.md           ← This is shown on the GitHub repo page
├── AI_PROMPTS.md       ← Prompts to help you customise with ChatGPT / Claude
└── HOSTING_GUIDE.md    ← You are reading this
```

**The most important rule about file names and folders:**

> HTML, CSS, and images are linked by their file path. If you put your profile photo in a folder called `images/` and name it `profile.jpg`, the HTML needs to say `src="images/profile.jpg"`. If the name or folder is different, the image won't show up.

Use lowercase letters and no spaces in file names. `profile-photo.jpg` is fine. `Profile Photo.jpg` will cause problems.

---

## Part 2 — Create a GitHub Account

1. Go to **github.com**
2. Click **Sign up**
3. Enter your email, create a password, and choose a username

**Choosing your username:** This becomes part of your portfolio URL. Pick something professional — your real name or initials works well. `yashsukhdeve` or `yash-sukhdeve` are both fine.

Once you're in, you're on the GitHub dashboard. Leave this tab open.

---

## Part 3 — Fork This Repository

"Forking" means making your own copy of this project. It takes 10 seconds.

1. Make sure you're logged into GitHub
2. Go to: `https://github.com/Yash-Sukhdeve/undergrad-eportfolio-tutorial`
3. In the top-right corner, click **Fork**
4. On the next page, you can change the repository name if you want — or leave it as is
5. Click **Create fork**

You now have your own copy at `https://github.com/YOUR-USERNAME/undergrad-eportfolio-tutorial`

---

## Part 4 — Turn on GitHub Pages

This is what makes the files accessible as a website.

1. In your forked repo, click the **Settings** tab (top of the page)
2. In the left sidebar, scroll down and click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select **main** and keep the folder as **/ (root)**
5. Click **Save**

GitHub will show a message like: *"Your site is being built"*

Wait about 60 seconds, then refresh the page. You should see:

> Your site is live at `https://your-username.github.io/undergrad-eportfolio-tutorial/`

Click that link. Your portfolio is now live on the internet.

---

## Part 5 — Edit the Files to Make It Yours

Now you need to replace the placeholder text with your real information.

### Option A: Edit directly on GitHub (easiest, no install needed)

1. In your repo, click on `index.html`
2. Click the **pencil icon** (Edit this file) in the top-right corner of the file view
3. Make your changes in the editor
4. Scroll down to **Commit changes**, write a short note like *"Update name and bio"*, and click **Commit changes**
5. Your live site updates in about 30–60 seconds

Repeat this for each file you want to edit.

### Option B: Download, edit locally, upload back (more control)

1. In your repo, click the green **Code** button
2. Click **Download ZIP**
3. Unzip the folder on your computer
4. Open the files in any text editor — Notepad works, but **VS Code** is free and much better: code.visualstudio.com
5. Make your changes
6. To upload back: in your repo on GitHub, go into the file, click the pencil icon, select all existing text, paste your edited version, and commit

### What to change first

Open `index.html` and find these lines — replace the placeholder text:

```html
<!-- Replace "Your Name" everywhere -->
<title>Your Name — E-Portfolio</title>

<!-- Replace the bio paragraph -->
<p>Undergrad student in Computer Science at [Your University]...</p>

<!-- Replace the stats -->
<strong>3+</strong><span>Projects</span>

<!-- Replace GitHub and LinkedIn links -->
<a href="https://github.com/YourUsername">GitHub</a>
<a href="https://linkedin.com/in/yourhandle">LinkedIn</a>
```

Then open `projects.html`, `skills.html`, `resume.html`, and `contact.html` and do the same.

---

## Part 6 — Add Your Photo

1. Take a photo or find one you want to use
2. Rename it `profile.jpg` (or `profile.png`)
3. In your repo on GitHub, navigate to the root folder
4. Click **Add file → Upload files**
5. Drag your photo in, or click to browse
6. Click **Commit changes**

Then in `index.html`, find this line and update the `src`:

```html
<img src="https://via.placeholder.com/180/..." alt="Profile photo" class="hero-photo"/>
```

Change it to:

```html
<img src="images/profile.jpg" alt="Your Name" class="hero-photo"/>
```

If you put the photo in an `images/` folder, make sure to create that folder first on GitHub (you can do this by uploading a file into a path that includes the folder name — GitHub creates it automatically).

---

## Part 7 — Add Your Resume PDF

1. Export your resume as a PDF from Word, Google Docs, or Canva
2. Name the file `resume.pdf`
3. Upload it to your GitHub repo (same way as the photo — **Add file → Upload files**)
4. In `resume.html`, find the download button and update the link:

```html
<!-- Change this: -->
<a href="#" class="btn" download>Download PDF</a>

<!-- To this: -->
<a href="resume.pdf" class="btn" download>Download PDF</a>
```

---

## Part 8 — Use a Theme Template Instead

If you want one of the six themed templates (CS Terminal, Design Studio, etc.) instead of the default template:

1. Go to `templates/` in your repo
2. Open the template you want (e.g., `template-cs.html`)
3. Click the pencil icon to edit
4. Select all the text (Ctrl+A / Cmd+A), copy it
5. Go back to your root folder and open `index.html`
6. Select all text and paste the template code over it
7. Commit the change

Or: just use the template file directly as your index page by renaming it. In your repo:
1. Click on `template-cs.html`
2. Click the pencil icon
3. Click the three dots (...) menu → **Rename**
4. Rename to `index.html` (you'll need to delete or rename the existing `index.html` first)

---

## Part 9 — Activate the Contact Form

The contact form uses a free service called Formspree. Without this step, the form shows up but doesn't actually send you anything.

1. Go to **formspree.io** and sign up for a free account
2. Click **New Form**
3. Give it a name (e.g., "Portfolio Contact"), enter your email, and click **Create Form**
4. You'll see a form ID — it looks like `xbjnkqwz`
5. In your `contact.html`, find this line:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

6. Replace `YOUR_FORM_ID` with your actual ID:

```html
<form action="https://formspree.io/f/xbjnkqwz" method="POST">
```

7. Commit the change

Now when someone fills in the form and submits, Formspree sends their message to your email.

---

## Part 10 — Rename Your Live URL (Optional)

Right now your URL ends in `/undergrad-eportfolio-tutorial/`. You can shorten this.

In your repo's **Settings → General**, scroll down to **Repository name** and change it to something like `portfolio`. Your URL becomes:

`https://your-username.github.io/portfolio/`

You can even use just your username as the repo name (e.g., `your-username.github.io`) and the URL becomes simply `https://your-username.github.io/`. To do this:

1. Create a new repo named exactly `YOUR-USERNAME.github.io`
2. Copy your portfolio files into it
3. Turn on GitHub Pages as before

---

## Common Problems

**My changes aren't showing up on the live site.**

GitHub Pages can take 1–3 minutes to update. Wait and refresh. If it's been more than 5 minutes, check:
- Settings → Pages: is it still turned on?
- Did you commit your changes? (Editing and leaving without committing doesn't save.)

**My image isn't showing.**

Check three things:
1. Is the file actually uploaded to the repo? Go to the repo and look.
2. Is the file name in your HTML exactly the same as the actual file name? `Profile.jpg` and `profile.jpg` are different.
3. Is the folder path correct? If the image is in `images/profile.jpg`, the `src` must say `images/profile.jpg`, not just `profile.jpg`.

**The contact form says "This form is not active" or doesn't send anything.**

You haven't connected Formspree yet. Follow Part 9.

**The page looks unstyled / broken.**

Check that `css/style.css` is still in your repo and that the `<link>` tag in your HTML files hasn't been accidentally deleted. Every HTML file has this near the top:
```html
<link rel="stylesheet" href="css/style.css" />
```

**I accidentally deleted something and can't fix it.**

GitHub keeps a full history of every change. Go to your repo, click **Commits** (the clock icon), find the last version that worked, and click **Browse files** on that commit to see what it looked like. You can copy the old content and paste it back in.

---

## That's It

Once your site is live, the URL never changes (unless you rename the repo). You can keep editing the files and the site updates automatically every time you commit.

Share the link on your resume, LinkedIn, and email signature.
