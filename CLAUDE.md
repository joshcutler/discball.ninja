# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Official website of the Intergalactic Discball Governing Body (discball.ninja), built with Jekyll (via github-pages gem) and hosted on GitHub Pages.

## Design Reference

Figma Make file: https://www.figma.com/make/huGWBLMFoeuug2jqqoYcGm/Static-website-for-Discball

The design is a React/Tailwind app with these pages:
- **Home** (`Home.tsx`): Hero with orange-red-purple gradient, "What is Discball?" section with 4 feature cards, "Ready to Play?" with 3 link cards, CTA section
- **Rules** (`Rules.tsx`): Game rules documentation
- **Ethos** (`Ethos.tsx`): Warrior spirit / community values
- **FAQ** (`FAQ.tsx`): Frequently asked questions

Shared layout (`Root.tsx`): Sticky nav with DISCBALL logo + mobile hamburger menu, footer with dark background. Color scheme: orange-500/600 primary, red-600 secondary, purple-700 accent, yellow-400 highlights. Bold typography with font-black headings.

## Commands

- **Install dependencies**: `bundle install`
- **Local dev server**: `bundle exec jekyll serve` (serves at localhost:4000)
- **Build site**: `bundle exec jekyll build` (outputs to `_site/`)

## Architecture

- Content pages are Markdown/HTML files with YAML front matter at the root level
- Custom layouts in `_layouts/` override Minima theme defaults
- Custom CSS in `assets/css/`
- Site configuration lives in `_config.yml`
- Custom domain (`discball.ninja`) configured via CNAME file
- Deployment is automatic via GitHub Pages on push to main

## Writing Style
- **No em-dashes.** Use periods, commas, or rewrite the sentence instead.
- **Lean into the pain humor.** Bruises are badges of honor. Reference getting hurt, welts, bruises, and physical consequences in a fun way. Examples: "The heavier the disc, the better the bruises." / "It hurts more than you'd think." / "The uglier the throw, the uglier the welt."
- **Tone is bold, direct, and irreverent.** Short punchy sentences. No corporate-speak. The game is violent fun and the copy should reflect that.
- **Warrior Spirit** is the core philosophy and should be referenced naturally throughout content, not just in its own section.

## Discball Rules (Canonical Source of Truth)

The rules page on the site has been updated to match these. Use the rules below as the authoritative source.

### What Is Discball?
Dodgeball with a frisbee. Free-for-all (no teams), individual elimination. 3-4 players is ideal; larger groups should subdivide into multiple games.

### Equipment
- One disc per game. Heavier is better — Big Kahuna (200g) recommended. Regulation ultimate discs work but are lighter.
- Cones to mark circles.
- A flat field (inspect for holes to avoid injury).

### Field Setup
- Players stand in equally spaced positions: 3 players = triangle, 4 players = square.
- Each player has a **circle** with a radius of **7 paces**.
- Distance between circle centers is **21 paces** (circles separated by roughly one radius from each other).
- A "pace" is a normal walking stride.
- Beginners can increase separation so the disc doesn't come in as hot.

### Objective
Be the last player standing (fewer than 3 outs) after all other players have been eliminated. **3 outs = eliminated.**

### Game Start
- Winner of the previous game throws first and picks direction. If no previous winner, pick at random.
- Thrower must verbally declare and get acknowledgement from all players before the first throw.

### Throwing
- You must stand **within your circle** when throwing.
- **The recipient must start in the center of their circle** until the disc is released.
- Any throw style is allowed — backhand, forehand, hammer, whatever works. Goofy/hard-to-catch throws are encouraged.
- **Named throw: Buzzsaw** — a straight overhead vertical throw that drops fast (like a sinker) and can be thrown very hard.
- A player may **never decline to throw** when it is their turn.

### Direction of Play
- Once a direction is chosen (clockwise or counterclockwise), **every player must continue throwing in that direction** until an event allows a change:
  - **Recording an out** on your target → you may change direction (commonly used for revenge).
  - **Throwing an uncatchable disc** (outside the circle or truly uncatchable) → the recipient now gets to select a new direction.
  - **Winning a race** → the winner picks a new direction.

### Outs
- **Any contact with the player (body, hair, clothes, anything) that does not result in a catch is an out.**
- A disc that lands in the circle but is NOT catchable is NOT an out.
- If you don't attempt to catch a catchable disc that lands in your circle, that IS an out.
- "Catchable" is self-policed with Warrior Spirit — don't be lazy.
- Disputes: the non-involved player(s) decide. Neither the thrower nor the catcher judges their own dispute.
- **Warrior Spirit self-outs:** If you didn't technically get hit but know you should have if you'd tried harder, you may self-assign an out. This is honored.
- **0 outs is the floor.** You cannot go negative.
- **3 outs = eliminated** (but see below — you keep playing).

### Catches
- A catch is **anything that prevents the disc from hitting the ground**.
- If the disc hits your body (leg, arm, etc.) and you grab it before it hits the ground, that's a **catch** (safe, no out).
- Once the disc hits the ground it is dead — cannot be caught. Ground bounces/rolls into a player don't count.
- **You must have initiated your last contact with the ground before catching outside the circle** (i.e., you can jump/dive out but must have launched from inside or at the circle edge).
- Catches must be attempted on catchable throws that enter your circle — Warrior Spirit demands it.

### Reducing Outs
- **Catching an errant throw outside your circle:** reduces your out count by 1.
- **Trick catch (behind the back, through the legs):** reduces your out count by 1.
- **Both combined** (trick catch on an errant throw outside circle): reduces by 2.
- Dives/layouts do NOT count as trick catches.
- If you're at 0 outs and make a reducing catch, nothing happens numerically — but you're a badass.
- Intentionally throwing outside the circle to let someone reduce outs is bad form and poor Warrior Spirit.

### Elimination & Continued Play
- **Eliminated players (3 outs) are NOT removed from the game.** They stay in their position and keep playing.
- Eliminated players cannot win, but they CAN still throw and deliver outs to others — including the decisive eliminating blow.
- Eliminated players can reduce their own outs through trick catches and errant-throw catches, potentially getting back below 3 outs and re-entering contention.
- Warrior Spirit: don't deliberately pile outs on eliminated players, but don't make it easy for them to come back either.
- **Reversals are critical in endgame** — an eliminated player can decide the winner.

### The Race
- A player may NOT leave their circle until the disc has been released.
- Once released, **any player** (including the thrower) may sprint to retrieve the disc.
- A race is only legal when the recipient did NOT receive an out on that throw.
- If a non-recipient beats the recipient to the disc (no contact allowed), they claim it and may pick a new direction.
- If the recipient gets it first, they throw in the established direction.
- **No contact during a race.** If contact occurs, it's a foul — disc goes to the fouled player.
- A race typically happens when a throw is missed/uncatchable and the disc is loose.
- If you lose a race, you get skipped in the throwing order.

### Winning
- Last player with fewer than 3 outs wins the round.
- Winner throws first and picks direction in the next game.
- There is no set number of games per session — play until you puke or have too many bruises.

### Warrior Spirit (Core Philosophy)
**The most important aspect of Discball.** Honor over outcomes.
- Be a badass. Getting hurt (not seriously injured) is good — lean into it.
- Try hard, even when it's strategically bad to do so.
- Self-call your outs honestly.
- Show off your bruises. Warrior Spirit credit for delivering bruises.
- Post pictures of bruises on the group thread afterward.
- **Trash talk is extremely encouraged.** Getting opponents on tilt is a valid strategy. Players are separated and there's no contact, so it shouldn't spiral. Don't play with people who can't handle it.
- Gloves are for weenies, even in winter.
- This is a year-round sport — play in snow, rain, whatever. Just check for field hazards.
- Spectators should cheer and jeer.

### Safety
- Inspect the field for holes and hazards before playing.
- Getting hurt is part of the game; getting seriously injured is not.
- Heavier discs hit harder — know your group's tolerance.
