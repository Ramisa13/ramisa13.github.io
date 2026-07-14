# Personal Portfolio Site

A single-page academic/research portfolio site, built as plain HTML, CSS,
and a few lines of JS — no build step, no framework, deploys directly on
GitHub Pages.

## Deploying on GitHub Pages

GitHub Pages serves a personal site from a repository with a very
specific name: `<your-github-username>.github.io`. It has to match your
username exactly, or Pages will serve it as a project site under a
subpath instead of at the root domain.

1. Create a new repository on GitHub named exactly:
   ```
   Ramisa13.github.io
   ```
   (replace `<your-github-username>` with your actual GitHub username —
   e.g. if your username is `ramisamridha`, the repo must be named
   `ramisamridha.github.io`).

2. Push this project to it:
   ```bash
   cd ramisa-portfolio
   git init
   git add .
   git commit -m "Initial commit: personal portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-github-username>/<your-github-username>.github.io.git
   git push -u origin main
   ```

3. In the repository on GitHub, go to **Settings → Pages**, and under
   "Build and deployment," set **Source** to "Deploy from a branch,"
   branch `main`, folder `/ (root)`. Save.

4. Your site will be live within a minute or two at:
   ```
   https://<your-github-username>.github.io
   ```

No further configuration is needed — GitHub Pages serves `index.html`
directly from the repo root.

## Before you publish: things to fill in

**Add your photo and CV.** The hero and contact sections both reference
`assets/profile.jpg`, and the hero has a "Download CV" button pointing at
`assets/CV.pdf`. Neither file exists yet — drop your own headshot in as
`assets/profile.jpg` (a square-ish crop works best, since it's displayed
in a circle) and your CV as `assets/CV.pdf`. Until you add `CV.pdf`, that
button will 404, so either add the file or remove the button:
```html
<a href="assets/CV.pdf" class="pill pill-solid" target="_blank" rel="noopener">Download CV</a>
```

Search the project for `YOUR-GITHUB-USERNAME` and `YOUR-LINKEDIN` in
`index.html` and replace them with your actual GitHub username and
LinkedIn handle — these appear in the hero links, contact section, and
every project card's link.

Also double check:
- The email address in the two `mailto:` links is current.
- The project links point at repositories you've actually pushed
  (`dr-transfer-learning`, `faceforge-dcgan`, `threadnet-fashion-cnn`,
  `puregrad-fashion-mnist`, `adcurve-linear-regression`) — if any aren't
  public yet, either make them public or remove that card.
- The research section's wording matches what you're comfortable making
  public — it currently describes the thesis and benchmarking manuscript
  in general terms, consistent with keeping architecture-level details
  unpublished until the papers are out.

## Structure
```
ramisa-portfolio/
├── index.html      all page content and section markup
├── style.css        design system: colors, type, layout, the scan-line hero motif
├── script.js          sets the footer year
└── assets/            (empty — drop a resume PDF or headshot here if you want one linked)
```

## Local preview
No build tooling required — just open `index.html` in a browser, or serve
it locally:
```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Design notes
The layout uses a clinical, editorial palette (cool off-white background,
navy ink, a single teal accent) rather than a generic dark-mode or
warm-cream template, and the hero's horizontal "scan lines" with a
sweeping highlight are a nod to the MRI-slice imagery central to the
research the site describes — a deliberate, subject-specific detail
rather than decoration. Motion respects `prefers-reduced-motion`, and all
interactive elements have visible keyboard focus states.

Fonts are loaded from Google Fonts (Spectral for headings, IBM Plex Sans
for body text, IBM Plex Mono for labels and metadata) — swap the
`<link>` tags in `index.html` and the `--font-*` variables in `style.css`
if you'd rather self-host or use different typefaces.
