# 🔥 Emberfall

> A fast, escalating arena-survival game built for solo runs and local 2-player co-op.

[![Emberfall CI](https://github.com/dvilrgamerz/game/actions/workflows/ci.yml/badge.svg)](https://github.com/dvilrgamerz/game/actions/workflows/ci.yml)
![React](https://img.shields.io/badge/React-19-149eca?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178c6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-8-646cff?logo=vite&logoColor=white)

**Survive. Upgrade. Become completely unreasonable.**

Emberfall is a browser arena-survival game focused on responsive combat, fast progression, readable effects, and replayable local co-op. The game runs fully in the browser with no backend required.

## ✨ Highlights

- 🔥 **40-wave campaign** with a boss wave every 5 waves
- 👤 **Solo mode** and 👥 **local 2-player co-op**
- ⚡ **16 upgrade choices** covering damage, survivability, fire rate, abilities, rewards, crits, and more
- 🎯 Auto-targeting combat with manual movement, dash, and active abilities
- 💀 Multiple enemy classes including shooters, chargers, splitters, elites, and bosses
- 🎮 Fully **remappable keyboard controls**
- ⚙️ Low / Medium / High graphics presets
- 📈 Optional FPS counter, particles, screen shake, UI zoom, and difficulty settings
- 🧯 Recovery UI that can reset broken settings without deleting the whole game
- 🌐 Ready for **Netlify** and **GitHub Pages**

## 🎮 Default Controls

| Action | Player 1 | Player 2 |
| --- | --- | --- |
| Move | W A S D | Arrow Keys |
| Dash | Space | Right Shift |
| Ability | E | Numpad 0 |
| Pause | Esc | Esc |

Controls can be changed from **Settings → Controls**.

## 🕹️ Gameplay Loop

1. Enter the arena.
2. Survive the timed enemy wave.
3. Defeat elites and bosses for better rewards.
4. Level up and choose from four upgrades.
5. Stack upgrades into stronger builds.
6. Reach wave 40 and clear the run.

Every fifth wave introduces a boss encounter. Wave pacing now has a defined combat duration, so waves cannot accidentally complete immediately after a lucky screen clear.

## 🆕 v2.1 Improvements

The current version focuses heavily on correctness and game feel:

- Fixed fire-rate upgrades so they permanently change weapon timing
- Fixed dash-cooldown upgrades
- Fixed ability-cooldown upgrades
- Added working credit / bounty upgrades
- Added real critical-damage scaling
- Added real boss-damage scaling
- Added real ability-power scaling
- Fixed Player 2 ability-direction input handling
- Prevented multiple bosses from spawning during the same boss wave
- Made level-up choices stable instead of reshuffling during re-renders
- Added timed wave pacing and remaining-time HUD
- Added credits to the in-game HUD
- Improved TypeScript tooling and CI checks

## 🚀 Run Locally

### Requirements

- Node.js 22+
- npm

### Setup

```bash
git clone https://github.com/dvilrgamerz/game.git
cd game
npm install
npm run dev
```

Vite will print the local development URL in your terminal.

## 🧪 Project Commands

```bash
npm run dev        # Start the development server
npm run typecheck  # Run TypeScript validation
npm run build      # Create the production build
npm run check      # Typecheck + production build
npm run preview    # Preview the production build locally
```

## 🧱 Project Structure

```text
game/
├── .github/
│   └── workflows/         # CI + GitHub Pages deployment
├── src/
│   ├── components/
│   │   └── Game.tsx       # Main Emberfall game loop + UI
│   ├── game/              # Experimental / extended game modules
│   ├── main.tsx           # React entry point + crash recovery
│   └── styles.css         # Global visual system
├── index.html             # App shell + metadata
├── netlify.toml           # Netlify build configuration
├── package.json
├── tsconfig.json
└── vite.config.ts
```

## 🧠 How the Main Game Works

The active game is implemented with a lightweight React + Canvas architecture:

- **React** controls menus, settings, upgrades, pause state, and game screens.
- **Canvas 2D** renders players, enemies, bullets, particles, health bars, and arena effects.
- **requestAnimationFrame** drives simulation and rendering.
- **localStorage** stores player settings and control bindings.
- Game difficulty scales with the current wave.

The main gameplay code intentionally avoids requiring a server, database, or paid API.

## 🌍 Deployment

### Netlify

This repository already includes `netlify.toml`.

Build command:

```text
npm run build
```

Publish directory:

```text
dist
```

### GitHub Pages

A GitHub Actions workflow is included at:

```text
.github/workflows/deploy-pages.yml
```

The Vite configuration uses relative asset paths so builds can work from a repository subpath such as `/game/`.

## 🛣️ Roadmap

Ideas for future versions:

- 🎮 Gamepad support
- 📱 Touch / mobile controls
- 🔊 Music and layered combat SFX
- ✨ More active abilities for each player
- 🧟 More enemy behaviors and boss patterns
- 🏆 Persistent achievements and run records
- 🔥 Deeper meta progression
- 🌈 Additional accessibility and visual options
- 💾 Saveable build / run summaries

## 🤝 Contributing

Bug reports, balance ideas, UI improvements, and gameplay contributions are welcome.

Before opening a pull request:

```bash
npm install
npm run check
```

See [CONTRIBUTING.md](CONTRIBUTING.md) for the project workflow.

## 🛠️ Tech Stack

**React 19 • TypeScript • Vite 8 • Tailwind CSS 4 • HTML Canvas • GitHub Actions • Netlify**

---

Made as an evolving browser-game project with a focus on fast gameplay, readable code, and replayability.
