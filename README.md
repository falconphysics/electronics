# Electronics with Microcontrollers — Textbook Site

A static website version of the **Pre-Engineering: Electronics with
Microcontrollers** course, built to be hosted on **GitHub Pages**. Every
chapter and tutorial from the original repository has been converted into a
styled, navigable web page with a sidebar, prev/next paging, syntax-highlighted
Arduino code, **embedded YouTube videos**, and a responsive (mobile-friendly)
layout.

You can visit my version of the site here: [https://falconphysics.github.io/electronics/index.html](https://falconphysics.github.io/electronics/index.html). Or follow the instrucitons below to make your own.

## What's inside

```
.
├── index.html              ← home / cover page
├── ch2.html … sensors.html ← chapter overview pages
├── blink.html, …           ← individual lesson pages
├── 404.html                ← themed not-found page
├── assets/
│   ├── style.css           ← the entire theme (one file)
│   └── img/                ← all circuit photos
└── .nojekyll               ← tells GitHub Pages to serve assets/ as-is
```

Everything is plain HTML/CSS — no build step, no JavaScript framework, no
dependencies. It works by just opening `index.html` in a browser. Videos are
embedded via privacy-friendly `youtube-nocookie.com` players.

## Deploy to GitHub Pages

You have two easy options.

### Option A — publish from a branch (simplest)

1. Create a new repository (or reuse your `electronics` repo).
2. Copy **the contents of this folder** into the repository root
   (so `index.html` sits at the top level, next to `assets/`).
3. Commit and push to the `main` branch.
4. In the repo, go to **Settings → Pages**.
5. Under **Build and deployment → Source**, choose **Deploy from a branch**.
6. Pick branch **`main`** and folder **`/ (root)`**, then **Save**.
7. Wait ~1 minute. Your site will be live at
   `https://<your-username>.github.io/<repo-name>/`.

### Option B — put the site in a `/docs` folder

If you'd rather keep the site separate from other repo files, drop everything
into a `docs/` folder instead, then in **Settings → Pages** choose branch
`main` and folder **`/docs`**.

## Notes

- The **`.nojekyll`** file is important — keep it. Without it, GitHub's default
  Jekyll processor can ignore folders and break the `assets/` path.
- All internal links are **relative**, so the site works under a project
  subpath (`/electronics/`) without any configuration.
- Embedded videos require an internet connection to load; the rest of the site
  works fully offline.

## Credits

Serial-communication material adapted from Arduino tutorials by Limor Fried
(ladyada) under [CC BY-SA 2.5](http://creativecommons.org/licenses/by-sa/2.5/).
Originally a [WordPress course](http://www.highschoolmaker.com/electronics-with-micro-controllers/).
