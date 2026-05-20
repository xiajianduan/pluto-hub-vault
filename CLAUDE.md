# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an Obsidian vault ("Pluto Hub Vault") with a custom plugin **Pluto Hub** (v2.0.0). It's a personal knowledge management system focused on Chinese classics, work notes, and drafts.

## Vault Structure

- `01草稿/` — Drafts and in-progress notes
- `02国学/` — Chinese classics (道德经, 孙子兵法, 词谱详解)
- `03工作/` — Work-related notes
- `04智搜/` — Smart search content (reserved)
- `98图片/` — Image assets
- `99系统/` — System configuration: skins (`assets/skin/`), samples (`assets/sample/`), plugin documentation screenshots/GIFs (`assets/doc/`)
- `.obsidian/plugins/pluto-hub/` — Custom plugin source (bundled)

## Pluto Hub Plugin

- **Manifest**: `.obsidian/plugins/pluto-hub/manifest.json` — id `pluto-hub`, minAppVersion 1.7.2, desktop + mobile
- **Config**: `.obsidian/plugins/pluto-hub/data.json` — module storage at `.obsidian/cache/modules`, backups at `.obsidian/cache/backups`, system config path `99系统`
- **Build**: Bundled via esbuild into `main.js` (single minified file, includes React)

The plugin allows users to manage, edit, and run local code modules within Obsidian. Module files are stored in `.obsidian/cache/modules/`. The plugin provides a card-based UI for modules with drag-and-drop reordering, a code editor with syntax highlighting, and file management sidebar.

## General Guidelines

- **No build step needed** — the plugin is checked in as a pre-built `main.js`. Source/build config is elsewhere.
- **Vault content** edits are Markdown files — standard Obsidian formatting applies.
- **Git**: Keep vault content and plugin changes in the same repo. Current branch is `master`.
