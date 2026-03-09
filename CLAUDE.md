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
- Custom domain (`diskball.ninja`) configured via CNAME file
- Deployment is automatic via GitHub Pages on push to main
