# Mohammod Ashikur Rahman — Portfolio

A one-page research portfolio, built with plain HTML/CSS/JS — no build step, no
npm, no dependencies. That means it can be opened directly in a browser and
hosted on GitHub Pages with zero configuration.

## What's inside

```
├── index.html                                 → the entire site (one page)
├── css/style.css                              → all styling (colors, type, layout)
├── js/script.js                               → mobile nav, active-link highlight, scroll-reveal
├── assets/
│   ├── profile.jpg                            → profile photo (pulled from the CV)
│   ├── favicon.svg                            → browser tab icon
│   └── Mohammod_Ashikur_Rahman_Resume.pdf     → powers the "Download CV" button
└── README.md
```

## 1. Open and preview in VS Code

1. Unzip this folder and open it in VS Code (`File → Open Folder…`).
2. Easiest preview option — install the **Live Server** extension (by Ritwick
   Dey) from the Extensions tab, then right-click `index.html` →
   **Open with Live Server**. It opens in your browser and reloads on save.
3. No-extension option — open a terminal in VS Code and run:
   ```bash
   python3 -m http.server 5500
   ```
   then visit `http://localhost:5500`.

## 2. Host it on GitHub Pages at ashikbuilds.github.io

Ashikur's GitHub username is `ashikbuilds`, so creating a repository with
**exactly that name** makes GitHub serve it automatically at
`https://ashikbuilds.github.io` — no separate Pages setup screen needed.

1. On GitHub, create a **new repository** named exactly:
   ```
   ashikbuilds.github.io
   ```
   Public, and leave "Add a README" unchecked (this folder already has one).

2. In VS Code's terminal, from inside this project folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/ashikbuilds/ashikbuilds.github.io.git
   git push -u origin main
   ```

3. Give it a minute, then visit **https://ashikbuilds.github.io**.
   If it isn't live yet, check the repo's **Settings → Pages** tab — on the
   very first push GitHub sometimes needs the source branch confirmed as
   `main` there before it deploys.

## Making changes later

- All copy lives directly in `index.html` — search for the section you want
  (`<section id="projects">`, `<section id="publications">`, etc.) and edit
  the text in place.
- Colors, fonts and spacing are defined once as CSS variables at the top of
  `css/style.css` under `:root` — most visual tweaks only need changing a
  value there rather than hunting through the file.
- To swap the photo or CV, just replace `assets/profile.jpg` or
  `assets/Mohammod_Ashikur_Rahman_Resume.pdf` with a new file of the same
  name.
- Every push to `main` redeploys the live site automatically within a
  minute or two — no extra step required.
