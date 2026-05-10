# Kanban Board

A fully functional, single-file Kanban board for personal task management. Built with vanilla HTML, CSS, and JavaScript — no frameworks or build tools required.

## Features

### Board Management
- **4 default columns**: Backlog, To Do, In Progress, Done
- **Add custom columns** with the "＋ Add Column" button
- **Rename columns** by double-clicking the header
- **Delete columns** (only when empty) via the trash icon on hover

### Cards
- **Title** (required) and optional **Description** (collapsible)
- **Priority badges**: Low (green), Medium (amber), High (red)
- **Due dates** — overdue dates display in red with a ⚠️ icon
- **Drag & drop** cards between columns using the native HTML5 API
- Cards dropped into the **Done** column are automatically marked complete (muted style + strikethrough)

### Filtering & Search
- **Real-time search** filters cards by title (case-insensitive)
- **Priority filter** dropdown hides non-matching cards (preserves column height)

### Persistence
- Board state is **automatically saved** to `localStorage` after every change
- State is **restored** on page load
- Example cards populate the board on first visit

### Statistics Bar
A fixed bar at the bottom showing live-updating metrics:
- Total cards, overdue count, done count, completion rate

## Design

- Dark theme with deep charcoal background
- Glassmorphism columns with frosted-glass effect
- Inter font (loaded from Google Fonts)
- Smooth transitions: card hover lift, drag ghost opacity, drop-zone pulse
- Fully responsive with horizontal column scrolling on small screens

## Getting Started

Simply open `index.html` in any modern browser. No server, no installation, no dependencies.

## Technical Details

| Aspect | Detail |
|---|---|
| **Architecture** | Single `index.html` file — all HTML, CSS, and JS inline |
| **Language** | Vanilla JavaScript (ES6+) |
| **Drag & Drop** | Native HTML5 Drag and Drop API |
| **Storage** | `localStorage` for board state persistence |
| **External deps** | Google Fonts (Inter) CDN only |
| **Browser support** | Modern browsers (Chrome, Firefox, Safari, Edge) |

## Code Structure

The JavaScript is organized into clearly separated sections:

1. **State** — Central application state object
2. **Default Data** — Example cards for first-time users
3. **Persistence** — `localStorage` save/load functions
4. **Rendering** — Column and card DOM generation
5. **Column CRUD** — Add, rename, delete columns
6. **Card CRUD** — Add, delete cards; inline forms
7. **Drag & Drop** — HTML5 drag/drop event handlers
8. **Filtering** — Search and priority filter logic
9. **Statistics** — Live stats bar calculation
10. **Initialization** — App bootstrapping

## License

MIT
