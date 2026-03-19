# Project knowledge

This file gives Codebuff context about your project: goals, commands, conventions, and gotchas.

## Overview
Personal portfolio website for **Aditya Mittha** — Embedded Systems Engineer. Single-page static site with a newspaper/editorial design theme. No build tools, no frameworks — pure HTML/CSS/JS in one file.

## Quickstart
- Setup: No install needed — just open `index.html` in a browser.
- Dev: Edit `index.html` directly; refresh browser to see changes.
- Test: Open in browser and visually verify.

## Architecture
- **`index.html`** — The entire site: markup, `<style>` block, and `<script>` block all in one file.
- No package manager, no bundler, no framework.
- Fonts loaded from Google Fonts: **Big Shoulders Display** (headings) and **Azeret Mono** (body/mono).
- Sections: Ticker → Nav → Hero → About (bio + skills) → Experience → Projects → Comments → Contact → Footer.

## Conventions
- **Design tokens** via CSS custom properties on `[data-t="light"]` / `[data-t="dark"]` for theming.
- **Color palette**: `--hot` (orange/red accent), `--ink` (text), `--paper` (background), `--muted`, `--gold`, `--blue`, `--green`.
- **Class naming**: Short, BEM-ish prefixes per section (`h-` hero, `pj-` project, `sk-` skill, `exp-` experience, `ct-` contact, `c-` comments).
- **Scroll reveal**: Elements with class `sr` are animated in via IntersectionObserver; delay variants `sr-d1` through `sr-d4`.
- **Animations**: CSS keyframes for entrance (`riseUp`), ticker scroll, cursor blink, dot pulse.
- Inline `<style>` and `<script>` — no external CSS/JS files.
- Comments section is client-side only (no backend persistence).

## Gotchas
- Everything is in a single `index.html` — edits to CSS, HTML, and JS all happen in that one file.
- The ticker track content is duplicated for seamless infinite scroll.
- Counter animation (`data-to`, `data-dec`) fires once via IntersectionObserver.
- No responsive hamburger menu — nav links are simply hidden on mobile (`display: none`).
