# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file 3D block editor (`index.html`) — an interactive canvas for creating, connecting, and arranging 3D-perspective blocks that represent architecture components. No build system, no dependencies — pure HTML + CSS + vanilla JS with Canvas 2D rendering.

## Quick Start

Open `index.html` directly in any browser. No server needed.

## Architecture

Everything lives in one `~500-line` HTML file:

| Section | Lines | Purpose |
|---------|-------|---------|
| CSS | 1-48 | Dark theme, canvas overlay UI, toolbar, modal, description panel |
| HTML template | 50-83 | Canvas, inline editor, description panel, modal for new block creation, toolbar |
| Projection system | 117-138 | `project()` for pseudo-3D perspective (fixed focal length 600), `corners()`, `fInfo()`, `iconPos()` |
| Drawing | 148-271 | `draw()` renders grid, connections (dashed lines), blocks sorted by Z depth, Z ruler, ⓘ info badge per block |
| Hit testing | 282-292 | Rectangle/polygon hit tests via point-in-polygon (`pip`), icon hit test for ⓘ badge |
| Mouse interaction | 297-393 | Drag blocks, single-click to select/pending-connection, double-click to edit label, wheel for Z-axis |
| Keyboard | 384-393 | Arrow keys move selected, +/− adjust Z, Esc clears pending, Delete/Backspace removes block |
| Description panel | 414-444 | Per-block rich text notes, open/close via ⓘ badge, editable inline textarea |
| Modal create dialog | 454-482 | Creates blocks with optional connection to existing block |

### Key Data Structures

- `blocks[]` — `{ id, label, desc, x, y, z, w, h }`
- `connections[]` — `{ from, to }` (bidirectional, stored once)
- `selected` — currently selected block
- `pendingConn` — first block in a two-click connection flow
- `mode` — `'none' | 'add' | 'delete'`

### Rendering Pipeline

Every interaction calls `draw()` which: clears canvas → draws grid → draws connection lines (with ghost line for pending) → sorts blocks far→near → draws each as a 3D box with front/side/back faces → draws Z ruler on right edge.

### Perspective Math

`PERSP=600`, `ZOOM=1.45`. Z ranges 0–360 (closer=more foreground, farther=deeper background). The projection scales objects based on Z depth simulating depth.

## Constraints

- Max 10 blocks enforced (`MAX = 10`)
- Label max length: 20 chars
- Description max length: 300 chars
- Block labels default to `B{idCounter}` if not provided
