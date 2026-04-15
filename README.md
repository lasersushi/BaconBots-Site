# BaconBots Website

The official site for **BaconBots** — a FIRST Tech Challenge robotics team.

Static HTML/CSS/JS. No build step. Hosts anywhere.

## Run locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in your browser.

## Project structure

```
.
├── index.html        # Home / hero
├── about.html        # Team, mentors, history
├── robots.html       # Past seasons / robots
├── sponsors.html     # Sponsor tiers + pitch
├── contact.html      # Contact card + mailto form
├── css/styles.css    # Shared design system + page styles
├── js/main.js        # Nav toggle, active-page highlight, reveal animations
└── assets/           # Logo + favicon
```

## Swapping placeholders

The site ships with clearly-marked placeholder content. To make it yours, search & replace these strings across all `.html` files:

| Placeholder              | Replace with                            |
| ------------------------ | --------------------------------------- |
| `Team #XXXX`             | Your real FTC team number               |
| `team@baconbots.example` | Your team email address                 |
| `20XX`                   | Real season years on robots page        |
| Member names + bios      | In `about.html` — student & mentor tiles |
| Robot names + specs      | In `robots.html` — robot tiles          |
| Sponsor names            | In `sponsors.html` — sponsor tiles      |

For real photos, replace the gradient `tile-image` blocks with `<img>` tags pointing at images in `assets/`.

## Theming

All colors live as CSS custom properties at the top of `css/styles.css`. To re-skin the site, change those values — everything else cascades.

## Deploying

This is a plain static site. It works as-is on:

- **GitHub Pages** — push and enable Pages on the branch
- **Netlify / Vercel** — drag the folder in, no config needed
- **Any static web host** — upload all files, set `index.html` as the default

## Notes

- Header and footer markup is duplicated across the 5 HTML files (no build step). When you change the nav or footer, update all 5.
- The contact form uses a `mailto:` action — no backend required, but it opens the visitor's email client. Swap to a form service (Formspree, Netlify Forms, etc.) if you'd rather have submissions land in an inbox automatically.
- FIRST<sup>®</sup>, FTC<sup>®</sup>, and FIRST<sup>®</sup> Tech Challenge are trademarks of FIRST.
