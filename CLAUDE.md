# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio SPA for Grant Ralls (grantralls.github.io). Single-page site built with SvelteKit 2 (Svelte 5 runes syntax), TypeScript, Tailwind CSS 4 + DaisyUI, deployed as a static site to GitHub Pages.

## Commands

- **Dev server**: `pnpm dev`
- **Build**: `pnpm build` (static output via `@sveltejs/adapter-static`)
- **Preview**: `pnpm preview`
- **Type check**: `pnpm check` (runs `svelte-kit sync && svelte-check`)
- **Lint**: `pnpm lint` (ESLint flat config with TypeScript + Svelte plugins)

Package manager is **pnpm** (enforced via `engine-strict=true` in `.npmrc`).

## Architecture

Single-page application — all content lives in `src/routes/+page.svelte`.

- `src/routes/+layout.svelte` — root layout, imports global styles and favicon
- `src/routes/layout.css` — Tailwind CSS + DaisyUI imports
- `src/lib/` — shared library code
- `static/` — static assets served as-is (robots.txt, etc.)
- `index.html` at root is a legacy file from the previous site design

## Key Conventions

- Svelte 5 runes syntax (`$props()`, `$state()`, etc.) — not legacy Svelte 4 syntax
- Icons via `@lucide/svelte`
- `shaders` package available for WebGL effects
- TypeScript strict mode enabled
