# Life simulators

A shelf for the most popular free particle-life simulators. Each project stays in its own folder as a git submodule, with its original license and history intact. Nothing here is a rewrite — these are the upstream projects, mirrored onto this account.

Particle Life is a swarm of colored dots. Each color attracts or repels the others by a short random rule. Out of that matrix you get cells, snakes, gliders, and little ecosystems.

## The shelf

| Folder | What it is | Stars (upstream) | License | Run it |
| --- | --- | --- | --- | --- |
| `sims/brainxyz` | Brainxyz / hunar4321. The viral one. 2D canvas, 3D canvas, and a short Python version. | ~3.4k | MIT | Open `particle_life.html` in a browser |
| `sims/particle-life-app` | Tom Mohr's desktop app behind [particle-life.com](https://particle-life.com) | ~1.0k | GPL-3.0 | Java 16–23, then `./gradlew run` |
| `sims/codeparade` | CodeParade / HackerPoet. The original C++ / SFML sim from the YouTube video. | ~370 | MIT | Build `Main.cpp` against SFML. A Windows zip is included upstream. |
| `sims/fnky-web` | Christian Petersen's JavaScript port of CodeParade, made for the browser. | ~300 | MIT | `npm install && npm start` inside the folder |

## Your copies

- https://github.com/firetiktoktube-ai/particle-life (fork of hunar4321/particle-life)
- https://github.com/firetiktoktube-ai/particle-life-app (fork of tom-mohr/particle-life-app)
- https://github.com/firetiktoktube-ai/codeparade-particle-life (mirror of HackerPoet/Particle-Life)
- https://github.com/firetiktoktube-ai/fnky-particle-life (mirror of fnky/particle-life)

CodeParade and fnky could not be plain forks: GitHub repo names are case-insensitive, and both want the name `particle-life`, which Brainxyz already took.

## Clone this shelf

```bash
git clone --recurse-submodules https://github.com/firetiktoktube-ai/life-simulators.git
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

## Where each app starts

- Brainxyz: `sims/brainxyz/particle_life.html` — a full-window canvas titled "Life", lil-gui for the knobs, attraction matrix up to 20 colors.
- Tom Mohr: `sims/particle-life-app/src/main/java/com/particle_life/app/App.java` — ImGui desktop shell over the particle-life physics.
- CodeParade: `sims/codeparade/Main.cpp` — prints "Welcome to Particle Life", opens a 1600×900 SFML window, keys B/C/D/F/G/H reshuffle the rules.
- fnky: `sims/fnky-web/src` — canvas-sketch port of the CodeParade rules.

## Licenses

These are separate projects. Do not merge their source into one binary without reading the license in that folder.

- MIT: Brainxyz, CodeParade, fnky. Keep the copyright notice.
- GPL-3.0: Tom Mohr's app. A combined work that links this code must stay GPL-3.0.

Upstream homes: [hunar4321/particle-life](https://github.com/hunar4321/particle-life), [tom-mohr/particle-life-app](https://github.com/tom-mohr/particle-life-app), [HackerPoet/Particle-Life](https://github.com/HackerPoet/Particle-Life), [fnky/particle-life](https://github.com/fnky/particle-life).

## Selling

Not legal advice. Each folder keeps its own license.

The three MIT sims (Brainxyz, CodeParade, fnky) may be sold. The MIT text itself says you can sell copies, if the copyright notice and the MIT permission notice stay in every copy. Those notices are collected in `NOTICE`.

Tom Mohr's desktop app is GPL-3.0. You can charge for it, but you cannot sell a closed version. Buyers must get the GPL and the source, and a paid app that includes that code has to stay GPL-3.0.

None of these licenses hand you the authors' names, logos, or the particle-life.com brand. Ship `NOTICE` with anything you sell.
