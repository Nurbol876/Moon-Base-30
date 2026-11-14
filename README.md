# Moon-Base-30
# 🌕 Moon Base 30: Junior Astronaut Mission Trainer

**NASA Space Apps Challenge 2026** · Challenge: *Build a Junior Astronaut Mission Trainer*
**Team:** The · **Play:** [https://nurbol876.github.io/Moon-Base-30/](https://nurbol876.github.io/Moon-Base-30/)

> A pixel-art survival game where students run a lunar outpost for 30 days and feel the engineering trade-offs that decide whether a real mission succeeds or fails.

🇷🇺 [Русская версия ниже](#-описание-на-русском)

---

## The problem

Space-themed STEM content is often either oversimplified or too complex for a young learner. Real missions are decided by **trade-offs**: more power for making oxygen means less for the greenhouse; more spacewalks for science means more radiation. Few tools let students experience those choices in a fun way.

## Our solution

**Moon Base 30** puts the player in charge of a small lunar base. You launch from Earth, land on the Moon, and keep your crew alive for 30 days by balancing:

| Resource | What it means in the game |
|---|---|
| 💨 Oxygen | Made from lunar soil, costs electricity |
| 💧 Water | Mined from ice, costs electricity |
| 🍲 Food | Grown in the greenhouse, needs water and time |
| ⚡ Power | Solar panels (dust and the lunar night reduce output) |
| ☢️ Radiation | Solar flares and spacewalks raise it; soil shielding lowers it |
| 🏠 Hull | Meteorites and dust storms damage it; repairs cost time |
| ❤️ Health | Needs exercise, food, water and air |

Every day you have a limited number of actions, so you can never do everything. That is the lesson.

## Features

- **Launch sequence:** suit up, board Orion, liftoff, trans-lunar burn, landing.
- **Three difficulty levels:** Easy, Medium, Hard (more lunar storms, less food and oxygen, more radiation).
- **Crew of 2 to 4** with roles: Doctor, Engineer, Biologist, Geologist. Each role changes how well actions work.
- **30-day simulation** with a lunar night (days 12–18), dust storms, solar flares, micrometeorites, equipment faults and supply ships.
- **Science missions with quizzes** about real space facts.
- **Astronaut passport:** achievements saved in the browser.
- **Leaderboard:** local top 10.
- **Debrief screen:** shows a resource chart and explains the real-world trade-off behind the player’s result.
- **Pixel-art scene, sound effects, English and Russian.**

## How to play

1. Pick a difficulty and 2–4 crew members.
2. Each day, spend your actions (repair, make oxygen, mine ice, tend the greenhouse, add radiation shielding, explore, clean panels, exercise, call home).
3. Press **End day**. Resources are consumed and random events happen.
4. Survive 30 days. Lose if the hull fails, radiation is too high, or the crew’s health reaches zero.

**Tip:** save power before the lunar night, and build shielding early.

## What students learn

- Systems thinking: life support, power, food and radiation are connected.
- Why astronauts exercise daily, why lunar dust is hard to handle, and why radiation shelters matter.
- That engineering is about choosing the least bad option under limits.

## NASA data and sources

The facts and ideas in the game come from NASA material about:

- International Space Station life: exercise, food, water recycling, sleep. [add links]
- The Artemis program and the Moon’s south pole (possible water ice in shadowed craters). [add links]
- Lunar surface conditions: day and night length, temperature, gravity, dust. [add links]
- Space radiation and solar flares. [add links]
- Plant growth experiments on the ISS (Veggie). [add links]

> Game numbers (consumption rates, event chances) are simplified for learning and are **not** real mission data.

## How it works

- **Simulation:** a daily tick updates oxygen, food, water, power, hull, radiation and health. Role bonuses and event odds depend on crew and difficulty.
- **Balance data:** difficulty and action values are kept in data files so they are easy to tune. [Godot version: `data/balance.json`]
- **Debrief:** the weakest resource at the end selects the matching real-world trade-off explanation.

## Tech stack

- **Web version:** HTML, CSS, JavaScript, Canvas, Web Audio API (single file, no libraries).
- **Godot version (in progress):** Godot 4, GDScript, JSON data, CSV translations.

## Run it

**Web version:** open `moon-base-30.html` in any modern browser, or visit [public link].

**Godot version:**
1. Install Godot 4.
2. Import the project folder.
3. Project Settings → Autoload: add `Events`, then `GameState`.
4. Add the `start_game` action in the Input Map.
5. Run `scenes/base.tscn` (F6) to test the simulation.

## Project structure (Godot)

```
autoload/   events.gd, game_state.gd
data/       balance.json
i18n/       translations.csv (en, ru)
scenes/     main.tscn, base.tscn
scripts/    main.gd, base.gd
assets/     art/, audio/, ui/
```

## Use of AI tools

We used AI tools during development and we list them honestly:

- **Claude (Anthropic):** game design ideas, balance prototyping, code drafts, text and presentation drafts.

All AI-generated output was reviewed and edited by the team. [adjust to match what you really did]

## Roadmap

- Mini-games: docking, panel repair, meal planning.
- More crew roles and Mars mode.
- Teacher dashboard and classroom mode.
- Online leaderboard and more languages.

## Team

| Name | Role |
|---|---|
| Nurbol Sagynbekov | Captain |
| Turusov Zhalal | Advisor |
| Turusov Zhalil | Coder |

## Credits and licenses

- Fonts: Space Grotesk (SIL Open Font License).
- Sounds, music, sprites, libraries: [list each with link and license].
- NASA content is used under NASA media usage guidelines. [verify and link]

License: [choose, e.g. MIT for code, CC BY 4.0 for content]

---

# 🇷🇺 Описание на русском

**Moon Base 30** — пиксельная игра, в которой школьник управляет лунной базой 30 дней и на практике понимает инженерные компромиссы реальных космических миссий.

**Проблема.** Космические STEM-материалы часто слишком упрощены или слишком сложны. Настоящие миссии решаются компромиссами: больше энергии на кислород означает меньше для теплицы, больше выходов на поверхность означает больше радиации.

**Решение.** Игрок стартует с Земли, летит на Луну и 30 дней балансирует кислород, воду, еду, энергию, радиацию, корпус и здоровье. Каждый день действий не хватает на всё, и в этом суть обучения.

**Возможности:** запуск и посадка, три сложности, экипаж из 2–4 человек с ролями (врач, инженер, биолог, геолог), лунная ночь, бури, вспышки, поставки, квизы о космосе, паспорт астронавта с достижениями, таблица рекордов, итоговый разбор реального компромисса, пиксельная графика, звук, русский и английский языки.

**Стек:** HTML, CSS, JavaScript, Canvas (веб-версия); Godot 4 и GDScript (версия в разработке).

**Важно:** числа в игре упрощены для обучения и не являются реальными данными миссий. Источники NASA и использованные ИИ-инструменты указаны выше.
