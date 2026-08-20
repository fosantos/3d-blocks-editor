# Floatmind (3D Blocks Editor)

Floatmind is a minimalist, single-file 3D block editor designed for organizing ideas, tasks, and goals in a spatial, connected environment. It uses a pseudo-3D perspective on a 2D canvas to visualize relationships between components.

## Project Overview

- **Architecture:** Single-file application (`docs/index.html`) with no external dependencies or build steps.
- **Technologies:** Vanilla HTML5, CSS3, and JavaScript (Canvas 2D API).
- **Core Concept:** 3D-perspective blocks with adjustable depth (Z-axis), labels, and descriptions, connected by dashed lines.
- **Persistence:** Local state is maintained via `localStorage`.
- **Primary Entry Point:** `docs/index.html` (open directly in a browser).

## Key Components (within docs/index.html)

- **Projection System:** `project()`, `corners()`, and `fInfo()` handle the conversion from 3D coordinates (X, Y, Z) to 2D screen coordinates using a fixed focal length.
- **Rendering Pipeline:** A single `draw()` function clears the canvas and re-renders all elements (grid, connections, and blocks) in Z-depth order (back-to-front).
- **Interaction Logic:** Handles mouse/touch events for dragging blocks, adjusting Z-depth (scroll wheel, contextual-panel slider), selecting blocks, and creating connections.
- **UI Overlay (Excalidraw-style floating islands):** Top-left island (main menu dropdown, realign, undo, redo); left-center vertical tool rail (add/delete/cancel modes); top-center contextual panel that appears while a block is selected (name/rename, Z-depth slider, connect-to dropdown, delete); bottom-left island (block counter, help/shortcuts popover). Plus block description panel and import/export modal.

## Development & Usage

### Running the Project
Simply open `docs/index.html` in any modern web browser. No local server is required.

### Key Commands (UI/Keyboard)
- **Add Block:** "+" button in the left tool rail.
- **Connect Blocks:** Click a selected block, then another — or the "connect to…" dropdown in the contextual panel.
- **Adjust Depth:** Mouse wheel over a block, contextual-panel slider, or `+`/`-` keys.
- **Move Block:** Drag with mouse or use Arrow keys.
- **Edit Label:** Double-click a block (or ✎ in the contextual panel).
- **Remove Block:** `Delete` or `Backspace` keys.
- **Export/Import:** Via the main menu (☰ island).

### Constraints & Conventions
- **Max Blocks:** 15 (defined by `MAX = 15` in JS).
- **Z-Axis Range:** 0 to 360 (0 is farthest/smallest, 360 is closest/largest).
- **Coding Style:** Vanilla JS, no modules, all logic in a single `<script>` tag.
- **State Management:** Global arrays `blocks[]` and `connections[]`.

## Documentation & Plans
- **README.md:** User-facing documentation and feature list.
- **CLAUDE.md:** Technical implementation details and architecture overview.
- **docs/superpowers/plans/ & specs/:** Design documents for upcoming or recently implemented features (e.g., hiding internal connection segments).
