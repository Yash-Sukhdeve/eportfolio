# AI Prompts for Your Portfolio

These are prompts you can paste into ChatGPT, Claude, Gemini, or any other AI assistant to help build and customise your portfolio. Replace anything inside `[ ]` with your own details.

The prompts are specific on purpose — vague prompts get vague answers. The more context you give the AI, the less editing you'll need to do afterward.

---

## Contents

1. [Starting out](#1-starting-out)
2. [Hero section](#2-hero-section)
3. [Projects](#3-projects)
4. [Skills](#4-skills)
5. [Resume and timeline](#5-resume-and-timeline)
6. [Contact page](#6-contact-page)
7. [Colours and fonts](#7-colours-and-fonts)
8. [Dark mode](#8-dark-mode)
9. [Animations](#9-animations)
10. [Adding new sections](#10-adding-new-sections)
11. [Fixing things](#11-fixing-things)
12. [Adding JavaScript](#12-adding-javascript)

---

## 1. Starting out

### Build a portfolio from scratch

```
I'm a [year, e.g. "third-year"] undergrad studying [your major] at [your university].
I want a personal portfolio website using only HTML and CSS — no JavaScript
frameworks, no npm, no build tools.

My name is [Your Name]. I'm interested in [e.g. machine learning, web dev, open source].
I've done [number] projects and [number] internships.

Please generate:
1. index.html — hero section with my name, a short bio, and a button linking to my projects
2. css/style.css — clean stylesheet using CSS custom properties so I can change the
   colour scheme by editing one line

Accent colour: [your hex colour, e.g. #2563eb]
Responsive using CSS Grid. No JavaScript.
```

---

### Fill in the template I already have

```
I have an HTML/CSS portfolio template. Here's my index.html:

[paste index.html here]

Please update the content with my details:
- Name: [Your Name]
- University: [university], [city]
- Degree: [e.g. B.Tech Computer Science]
- Graduating: [year]
- Bio (2–3 sentences): [write something here or ask it to write one based on your details]
- Interests: [list them]
- Accent colour: [hex]

Don't change the HTML structure or CSS classes. Only update the text content
and the --accent variable.
```

---

## 2. Hero section

### Write your bio

```
Write a 3-sentence bio for a portfolio website.

About me:
- Studying [major] at [university]
- I've worked on [project or internship] where I [what you did]
- I want to work on [type of work] after graduating

Write it in first person. Don't use words like "passionate", "leverage", or
"dynamic". Keep it under 60 words and make it sound like a real person wrote it.
```

---

### Typewriter animation on your name (CSS only)

```
I have this heading in my portfolio:

  <h1>Hi, I'm <span>Your Name</span></h1>

Add a CSS-only typewriter animation to the <span> so the name types out on
page load. Use @keyframes with the steps() function. No JavaScript.
Show me the CSS to add and where it goes in the stylesheet.
```

---

### Add a circular profile photo

```
I want to add a profile photo to my portfolio hero section. The file is photo.jpg
in the project root.

Add an <img> tag that:
- Shows as a circle (border-radius)
- Has a coloured ring border using my --accent CSS variable
- Has a small drop shadow
- Shrinks on mobile without breaking the layout

My --accent colour is [hex]. Show me the HTML and the CSS to add.
```

---

## 3. Projects

### Add a project card

```
Add one project card to my projects.html. The card should match the existing style:
white background, rounded corners, shadow on hover, tech stack as pill badges.

Project:
- Title: [project title]
- What it does: [one sentence]
- Stack: [e.g. Python, Flask, PostgreSQL]
- GitHub: [URL]
- Live demo: [URL, or say "none"]

Give me just the HTML block to paste inside the .grid div. No new CSS.
```

---

### Mark one project as Featured

```
I want to add a "Featured" label to one of my project cards — a small badge
in the top-right corner of the card.

The card already has position: relative.
No JavaScript. The badge should say "Featured" in white text on my --accent colour.

Show me the HTML to add inside the card and the CSS to add to my stylesheet.
```

---

### Add a Live Demo button

```
My project cards have one button: "View on GitHub" with class .btn-outline.
I want to add a second button: "Live Demo" that opens [your URL] in a new tab.

Make the Live Demo button use .btn (filled) and keep GitHub as .btn-outline,
so the two buttons look distinct next to each other.

Show me the updated HTML for the button row of one card.
```

---

## 4. Skills

### Add more skill bars

```
I have CSS skill progress bars in skills.html. Here's one:

  <div class="skill-item">
    <label><span>Python</span><span>90%</span></label>
    <div class="skill-bar">
      <div class="skill-bar-fill" style="width:90%"></div>
    </div>
  </div>

Add these skills in the same format:
- [Skill 1]: [percentage]%
- [Skill 2]: [percentage]%
- [Skill 3]: [percentage]%

Return just the HTML blocks.
```

---

### Use star ratings instead of bars

```
I want to replace my CSS skill bars with 5-star ratings. CSS only — no JavaScript,
no image files, no icon libraries.

Stars up to the rating should use --accent colour. Empty stars should be light grey.
Example: Python — 4.5 out of 5 stars.

Show me the HTML for one skill item and the CSS to add.
```

---

### Add a tools grid

```
Below my skill bars I want a "Tools I Use" section as a responsive icon grid.
HTML and CSS only.

Tools: [list your tools, e.g. VS Code, Git, Docker, AWS, Figma, Linux]

The grid should show 4–5 columns on desktop and 2 on mobile, using CSS Grid
auto-fit/minmax. Each cell is a small card with the tool name centred.
Highlight with --accent colour on hover.

Show me the HTML for skills.html and the CSS for style.css.
```

---

## 5. Resume and timeline

### Add a timeline entry

```
Add an entry to my resume timeline. Here's an existing entry for reference:

  <div class="timeline-item">
    <div class="timeline-dot"></div>
    <h4>Software Engineering Intern</h4>
    <p class="meta">Company Name | May 2025 – Jul 2025</p>
    <p>Description.</p>
  </div>

New entry:
- Title: [role or degree name]
- Organisation: [company or university]
- Dates: [e.g. Jun 2024 – Aug 2024]
- Description: [what you did, one concrete result if you have one]

Return just the HTML block.
```

---

### Write bullet points for a job

```
Write 2–3 resume bullet points for this position:

- Company: [name]
- Role: [title]
- Dates: [start – end]
- What I did: [describe in plain English]
- Measurable result (if any): [e.g. cut build time by 40%]

Start each bullet with an action verb in past tense. Keep each one under 20 words.
Don't use "contributed to", "assisted with", or "helped". Be specific.
```

---

### Download CV button

```
I want a "Download PDF" button on my resume page that triggers a file download
of resume.pdf from the project root (not just opening it in the browser).

Use the existing .btn CSS class. Add a small download symbol before the text
using a Unicode character — no icon library.

Show me the HTML only.
```

---

## 6. Contact page

### Connect the Formspree form

```
My contact form has this action:

  <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">

My Formspree form ID is: [your ID]

1. Update the action URL.
2. Add a hidden field to redirect the user back to contact.html after they submit.
3. Add a honeypot field (_gotcha) to cut down on spam.

Show me just the updated form opening tag and the hidden fields to add inside it.
```

---

### Show a thank-you message after submission (no JavaScript)

```
When someone submits my Formspree form, Formspree redirects back to my page
with ?success=true in the URL. I want to show a "Thanks, I'll get back to you!"
message using only HTML and CSS.

Suggest the simplest CSS-only approach for this and show me what to add to contact.html.
```

---

## 7. Colours and fonts

### Get colour scheme suggestions

```
My portfolio uses these CSS variables:

  :root {
    --accent:      #2563eb;
    --accent-dark: #1d4ed8;
    --bg:          #f8fafc;
    --surface:     #ffffff;
  }

Suggest 3 alternative colour schemes. For each give me:
- A name
- The 4 hex values
- One sentence on the mood or impression it creates

I study [your field]. I want it to feel [adjective, e.g. calm and minimal / bold and creative].
```

---

### Switch to a dark theme

```
I have a light-theme CSS portfolio with these root variables:

  :root {
    --accent:      #2563eb;
    --accent-dark: #1d4ed8;
    --bg:          #f8fafc;
    --surface:     #ffffff;
    --text:        #1e293b;
    --muted:       #64748b;
    --border:      #e2e8f0;
  }

Give me a soft dark theme (think GitHub dark or Notion dark — not pure black).
Keep the blue accent. Show me just the updated :root block.
```

---

### Change the font

```
My portfolio currently uses:

  --font: 'Segoe UI', system-ui, sans-serif;

I want to switch to a Google Font. Suggest 3 options that work for a [your field]
student portfolio. For each give me:
1. The font name and why it fits
2. The <link> tag for the <head>
3. The updated --font variable

I want it to feel [e.g. modern / warm / technical / approachable].
```

---

## 8. Dark mode

### Auto dark mode that follows the OS setting

```
I have a CSS portfolio with this :root:

[paste your :root block]

Add a @media (prefers-color-scheme: dark) block that switches to a dark theme.
Use roughly:
- Background: #0f172a
- Cards: #1e293b
- Text: #f1f5f9
- Keep the blue accent unchanged
- Borders visible but not harsh

Show me just the @media block to append to style.css. No HTML changes needed.
```

---

### Manual dark/light toggle button (no JavaScript)

```
I want a dark/light toggle switch in my nav. CSS only — use the checkbox trick.

The toggle should look like a pill/switch (not a raw checkbox).
Use ☀ and ☽ Unicode characters for the icons — no icon fonts.
When checked, it should flip the :root CSS variables to dark mode values.

Show me the HTML to add to my nav and the CSS to add to my stylesheet.
Keep the CSS under 40 lines.
```

---

## 9. Animations

### Fade-in cards on scroll (CSS only)

```
I want my portfolio cards to fade in as the user scrolls down.
CSS only — no JavaScript.

Cards are inside a .grid div. Each card should:
- Start transparent and slightly lower than its final position
- Animate into place over 0.4s with ease-out
- Stagger so they come in one after another

If animation-timeline scroll has poor browser support, use animation-delay staggering
as a fallback. Show me the CSS to add.
```

---

### Better card hover effect

```
My project cards currently have this hover state:

  .card:hover { transform: translateY(-3px); box-shadow: 0 6px 18px rgba(0,0,0,.12); }

Give me 3 different hover effect options. For each, show the CSS and describe the effect
in one sentence. CSS only. Subtle enough for a job-search portfolio — nothing flashy.
```

---

## 10. Adding new sections

### Writing / blog list

```
I want a simple "Writing" section on my portfolio. No backend — just links to
separate .html files for each post.

Each entry should show:
- Post title (linked)
- Date
- One-sentence summary

Display it as a list, not cards. Add the HTML to index.html and any new CSS to style.css.
Match the existing design (same font, same CSS variables).
```

---

### Open source contributions

```
I want a compact "Open Source" section listing repos I've contributed to.
Don't use a card grid — use a list or table so I can fit 6–8 entries without
the page feeling heavy.

Each entry: repo name (linked to GitHub), what I contributed (one line),
language badge (same .badge style as the rest of the page), star count with a ★.

Show me the HTML and any new CSS needed.
```

---

### Certifications

```
I want to add a certifications section to my portfolio. Each cert should show:
- Name
- Issuing organisation
- Date
- Verification link (optional)

I have badge images saved as cert-aws.png, cert-google.png, etc.
Show each badge as a small thumbnail next to the text.

Show me the HTML and CSS. Keep the same visual style as the rest of the page.
```

---

### Currently reading / bookshelf

```
I want a small "Currently Reading" section on my home page showing 2–3 books.
Each book: cover image, title, author. That's it — no stars or reviews.

Cover images are book1.jpg, book2.jpg, book3.jpg in the project root.

Show me the HTML and CSS. Use flexbox. It should sit inside a section on the page,
not take over the full width.
```

---

## 11. Fixing things

### Layout breaks on mobile

```
My portfolio looks fine on desktop but something goes wrong on mobile.
Here's the CSS that's probably involved:

[paste the CSS]

Here's the HTML:

[paste the HTML]

The problem: [describe it — e.g. "cards overflow the screen", "nav links overlap the logo",
"the hero image is too big and pushes everything down"]

Fix the CSS so it works on screens narrower than 600px. Tell me what was wrong
and what you changed.
```

---

### Low contrast after changing colours

```
I changed my --accent to [colour] and now some text is hard to read.

Here's my :root:

[paste it]

Check the contrast ratios for:
1. Body text (--text) on the page background (--bg)
2. Muted text (--muted) on --bg
3. White button text on --accent

WCAG AA needs 4.5:1 for normal text and 3:1 for large text.
Tell me which ones fail and give me replacement hex values that pass.
```

---

### Explain a CSS rule I don't understand

```
There's a CSS rule in my stylesheet I don't fully understand. Please explain it
line by line, as if I know basic CSS but haven't seen this pattern before:

[paste the CSS here]
```

---

## 12. Adding JavaScript

### Scroll progress bar

```
I want a thin bar at the very top of the page that fills from 0% to 100% as
the user scrolls down (like a reading indicator).

Show me:
1. The HTML (just one div)
2. The CSS (fixed position, colour from --accent)
3. The JavaScript that updates the bar width on scroll

Vanilla JS only, under 10 lines. No libraries.
```

---

### Copy email button

```
On my contact page I show my email as plain text. I want a small "Copy" button
next to it that copies the address to the clipboard.

Show me:
1. The updated HTML
2. CSS for the button that matches my .btn-outline style
3. Vanilla JS (under 10 lines) that copies the text and changes the button label
   to "Copied!" for 2 seconds

No jQuery.
```

---

### Filter projects by tech tag

```
My projects.html has cards with badge spans like:
  <span class="badge">Python</span>

I want filter buttons at the top — "All", "Python", "JavaScript", "ML" — that
show only cards matching the selected tag.

Show me:
1. The HTML for the filter button row
2. The CSS
3. Vanilla JavaScript under 20 lines that handles the filtering

No frameworks. Walk me through what each line of the JS does.
```

---

## A few things that help

**Give the AI your actual code.** Copy and paste your HTML or CSS when asking it to modify something. "Here's my current card HTML:" gets much better results than a vague description.

**Ask why, not just what.** Add "explain what this does" to any prompt. You'll need to explain your own portfolio in interviews.

**One change at a time.** Asking for a single focused change is easier to review than asking for five things at once. If something looks wrong, paste it back and ask the AI to fix it.

**Read before you paste.** Skim the code before adding it to your project. If a line confuses you, ask about it. It's your portfolio — you should understand every part of it.
