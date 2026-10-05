# Beyond the Clinic: AI for Patient-Driven Health

Website for the proposed ICLR 2027 workshop. Plain static HTML/CSS with no build step, served by
GitHub Pages.

```
index.html        all page content, one commented block per section
css/style.css     styling (colors are variables at the top)
js/main.js        sticky nav and mobile menu
img/sf.jpg        hero photo (add this; the hero falls back to a gradient without it)
img/favicon.svg   browser-tab icon
```

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Editing

- **Hero photo:** save a landscape photo (about 2400 px wide, under ~500 KB) as `img/sf.jpg`, and
  put its credit in the `<p class="credit">` line in the footer.
- **People:** copy an `<article class="person">` block. To add a headshot, replace
  `<div class="avatar">AB</div>` with `<img class="avatar" src="img/people/name.jpg" alt="">`
  (square images work best).
- **After acceptance:** change "Proposed workshop" in the hero kicker and footer, add the
  OpenReview link, and fill in the exact workshop day.

## Deploy (GitHub Pages, free)

1. Create a free GitHub organization (github.com, then **+**, then **New organization**, Free plan),
   e.g. `my-workshop`, and invite the co-organizers.
2. In it, create an empty **public** repo named exactly `my-workshop.github.io`.
3. Push this folder:

   ```bash
   git init -b main
   git add .
   git commit -m "Initial workshop site"
   git remote add origin https://github.com/my-workshop/my-workshop.github.io.git
   git push -u origin main
   ```

4. In the repo, open **Settings, then Pages**, and set the source to **Deploy from a branch**,
   `main`, `/ (root)`. The site appears at `https://my-workshop.github.io` within a minute or two.
