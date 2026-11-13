## What this is
A static personal website published at **www.melax.com**, combining a current character-selection landing page and profile page with an archive of game-development and graphics/physics writeups. It is aimed at visitors browsing the site and developers looking for explanations, sample code, and older demos.

### Stack
- **Language(s):** HTML, CSS, JavaScript, and a small C++ example
- **Framework / runtime:** Static pages served by a web server; no application framework
- **Notable libraries:** None required. Some pages load fonts from Google Fonts.

## How it's organized
```text
/
  index.html       Character-selection landing page; links to profile pages
  Cassandra.html   “Coming soon” page; the detailed profile is under /cassandra
  Jean.html        “Coming soon” profile page
  Mackenzie.html   “Coming soon” profile page
  Nala.html        “Coming soon” profile page
  Stan.html        “Coming soon” profile page
  diag.html        Quaternion-based diagonalization of symmetric 3×3 matrices
  volint.html      Mesh volume, center-of-mass, and inertia-tensor calculations
  bsp/             BSP collision-detection paper, demos page, and images
  cassandra/       Cassandra’s profile page and its assets
  dspring/         Spring-derivative and cloth-simulation writeup, with illustrations
  minigames/       Pages describing the Teeter and Tea Party games
  tetris/          Reinforcement-learning writeup, C++ example, and illustrations
  Background.png   Landing-page background
  Melaxlogo.png    Landing-page logo
  CNAME            Custom domain configuration
```

**How it fits together:** The root `index.html` links visitors to profile pages, while the technical articles and demonstrations are separate static pages under their own paths. The writeups cross-link related topics—for example, `volint.html` links to `diag.html`, and the Tetris article links to `learning.html` and the C++ example. There is no shared application or build pipeline tying the sections together.

## How to run it
There is no README, package/build manifest, or test command in the repository. To preview the static site locally:

```bash
git clone https://github.com/melax/melax.github.io.git
cd melax.github.io
python3 -m http.server 8000
```

Then open `http://localhost:8000`. The repository’s `CNAME` points to `www.melax.com`, consistent with static-site hosting.

## Try asking
- How does `tetris/tetris.cpp` update its state-value table while it plays?
- How do `volint.html` and `diag.html` work together to calculate principal axes?
- Which downloadable files referenced by `bsp/index.html` and `minigames/index.html` are present in the repository?
