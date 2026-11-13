# melax.github.io

A static personal website published at **www.melax.com**. It combines a character-selection landing page and profile page with an archive of game-development, graphics, physics, and AI writeups. The site is mostly standalone HTML documents, with CSS, JavaScript, media assets, and a small C++ example.

## Contents

- **Personal pages:** a character-selection homepage and profile/placeholder pages.
- **Graphics and physics notes:** mesh volume and mass properties, matrix diagonalization, spring derivatives, and BSP collision detection.
- **AI example:** an explanation and C++ implementation of a reinforcement-learning Tetris experiment.
- **Game demos:** pages documenting the Teeter and Tea Party mini-games.

## Repository layout

```text
/
  index.html              Character-selection landing page
  Cassandra.html          Placeholder page; full profile is under cassandra/
  Jean.html               Placeholder profile page
  Mackenzie.html          Placeholder profile page
  Nala.html               Placeholder profile page
  Stan.html               Placeholder profile page
  diag.html               Quaternion-based diagonalization of symmetric 3x3 matrices
  volint.html             Mesh volume, center-of-mass, and inertia-tensor calculations
  Background.png          Landing-page background
  Melaxlogo.png           Site logo
  CNAME                   Custom domain configuration

  bsp/                    BSP collision-detection article, paper, and images
  cassandra/              Cassandra profile page and assets
  dspring/                Spring-derivative writeup and illustrations
  minigames/              Teeter and Tea Party game descriptions
  tetris/                 Reinforcement-learning writeups, C++ example, and images
```

### Notable pages and files

- `index.html` links to the profile pages and uses the root-level images for its visual design.
- `cassandra/index.html` contains a profile page; `Cassandra.html` is a separate “Coming soon” page.
- `volint.html` presents code and background for computing the volume, center of mass, and inertia tensor of a triangle mesh. It links to `diag.html`, which describes diagonalizing the symmetric tensor to obtain its principal moments and axes.
- `dspring/dspring.html` explains spring force derivatives and their use in simulation.
- `bsp/index.html` describes dynamic plane-shifting BSP traversal and links to `bsp/melaxbsp.pdf`. It also refers to a demo archive, `BSPdemos2001.zip`.
- `tetris/learning.html` introduces reinforcement learning; `tetris/tetris.html` documents the experiment; `tetris/tetris.cpp` contains the example program.
- `minigames/index.html` describes Teeter and Tea Party and refers to `teeter.zip` and `teaparty.zip`.

## Stack and tooling

- **Languages:** HTML, CSS, JavaScript, and a small amount of C++.
- **Runtime:** static files served by a web server; no application framework.
- **Dependencies/build:** no package manager, dependency manifest, or build step is required. Some pages request fonts from Google Fonts.
- **Tests:** no automated test suite is provided.

## Preview locally

With Python 3 installed, serve the repository root:

```bash
git clone https://github.com/tuliolivas/melax.github.io.git
cd melax.github.io
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Publishing

The root `CNAME` file contains `www.melax.com`, indicating the configured custom domain. The pages are static and can be served directly by a compatible static host; no compilation is needed.

## Download availability

The repository includes `bsp/melaxbsp.pdf`. The demo archives linked from the pages—`bsp/BSPdemos2001.zip`, `minigames/teeter.zip`, and `minigames/teaparty.zip`—are referenced by the HTML but are not present in the repository.

## License

No repository-wide license is specified in the root files. Check with the maintainer before reusing content or assets if you need explicit permission.
