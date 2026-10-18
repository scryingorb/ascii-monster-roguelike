# ASCII Monster Roguelike: Reforged

Python terminal roguelike with procedural dungeons, monster capture, turn-based combat, and persistent saves.

## Overview

The original prototype was a single large `game.py`. Reforged splits the project into focused modules for game flow, battles, procedural generation, data models, persistence, content, and UI. The result is easier to test, maintain, and extend.

## Features

- Explore connected procedural floors with combat, treasure, healing, and boss rooms.
- Capture monsters and manage a team of up to six.
- Level up through turn-based battles and collect items and gold.
- Save and restore progress through versioned JSON files.
- Reveal the dungeon through a fog-of-war map.
- Keep game flow, combat, generation, persistence, and terminal UI in separate modules.

## Technologies

Python 3.10+, standard-library dataclasses and JSON; pytest for the existing tests.

## Getting Started

Requires Python 3.10+.

```bash
python main.py
```

Movement uses `W`, `A`, `S`, `D` followed by Enter. This makes the game work in Windows PowerShell, Command Prompt, VS Code terminals, macOS, and Linux without a platform-specific keyboard library.

## Usage

| Command | Action |
|---|---|
| W A S D | Move |
| M | Map |
| T | Team |
| I | Inventory |
| V | Save |
| H | Help |
| Q | Return to title |

## Project structure

```text
ascii-monster-roguelike-v2/
├── main.py
├── roguelike/
│   ├── battle.py
│   ├── content.py
│   ├── dungeon.py
│   ├── factory.py
│   ├── game.py
│   ├── models.py
│   ├── save.py
│   └── ui.py
├── tests/
│   └── test_core.py
├── README.md
└── .gitignore
```

## Technical highlights

This project demonstrates:

- Python package/module organization
- Dataclasses and serialization
- Procedural generation
- Graph connectivity
- State machines and turn-based combat
- Rule-based enemy behavior
- Collision detection
- Manhattan-distance AI decisions
- JSON persistence and save versioning
- Automated testing
- Separation of game data, logic, and presentation

## Tests

The runtime has no third-party dependencies. If `pytest` is installed:

```bash
pytest
```

## Future ideas

- A* pathfinding
- Status effects and elemental strengths/weaknesses
- Shops and equipment
- More bosses and biomes
- Seeded daily runs
- Pygame graphical client using the same game logic

## Project Status

Functional prototype. Run from source; no packaged GitHub release is available.
