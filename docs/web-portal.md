# Web Portal Specification & Design System

The Awesome Tech Talks web portal is a modern, high-performance application built with Next.js 15 (App Router), Tailwind CSS, and shadcn/ui. It delivers a familiar YouTube-style developer learning interface.

---

## 1. Page Routes and Layouts

### 1.1 Home / Marketing (`/`)
- **Hero Section**: High-impact value proposition, key metrics (66 talks, 40K+ words, 4 channels), and primary CTA to `/browse`.
- **Feature Grid**: Dual-layer architecture explanation (Machine JSON vs. Human Markdown), AI-ready prompt payloads, and Mermaid diagram support.
- **Sponsors Strip**: Active sponsor logos dynamically loaded from `data/ads.json`.
- **Footer**: MIT license, GitHub link, governance documents.

### 1.2 Browse Grid (`/browse`)
- **Top Bar**: Search input with keyboard shortcut (`Cmd+K`) and horizontally scrollable topic filter chips.
- **Sidebar**: Collapsible drawer with navigation links and channel list.
- **Card Feed**: 4-column responsive grid (1 on mobile, 2 on tablet, 3-4 on desktop) displaying:
  - 16:9 YouTube thumbnail (`https://img.youtube.com/vi/{ID}/maxresdefault.jpg`).
  - Overlay badge showing read time.
  - Video title, speakers, channel badge, publication date, and topic tag pills.

### 1.3 Watch Studio (`/watch/[slug]`)
- **Left Pane (Media & Metadata)**:
  - Embedded YouTube iframe player with responsive 16:9 container.
  - Video title, speakers, channel attribution, and external YouTube redirect button.
  - Interactive chapter segment list.
- **Right Pane (Knowledge Studio)**:
  - **Study Notes Tab**: Full rendered markdown note with interactive Mermaid diagrams, TL;DR, and concept definitions.
  - **Raw DATA Tab**: Syntax-highlighted JSON record.
  - **Action Bar**: Fixed bottom buttons: "Copy Markdown" and "Copy JSON" for instant paste into Claude, Gemini, or ChatGPT.
- **Bottom Rail**: Featured advertiser videos and related session recommendations.

---

## 2. Typography & Fonts

The portal uses **Geist** from Vercel as its primary typeface.

```css
--font-sans: 'Geist', system-ui, -apple-system, sans-serif;
--font-mono: 'Geist Mono', monospace;
```

---

## 3. Dual-Mode Color Tokens

### Light Mode

| Token | Hex Value | Purpose |
|---|---|---|
| `--bg-primary` | `#f8f8f8` | Main background across all pages |
| `--bg-secondary` | `#ededed` | Search bar, input fields, cards, sidebar |
| `--text-heading` | `#121317` | Headings (h1, h2, h3) and subheadings only |
| `--text-body` | `#222222` | Body text, descriptions, captions, metadata |
| `--accent` | `#e78a53` | Primary buttons, active states, tags, highlights |

### Dark Mode (Default)

| Token | Hex Value | Purpose |
|---|---|---|
| `--bg-primary` | `#121113` | Main background across all pages |
| `--bg-secondary` | `#312f2f` | Search bar, input fields, cards, sidebar |
| `--text-heading` | `#e78a53` | Headings (h1, h2, h3) and subheadings only |
| `--text-body` | `#f8f8f8` | Body text, descriptions, captions, metadata |
| `--accent` | `#e78a53` | Primary buttons, active states, tags, highlights |

---

## 4. Client-Side Search Architecture

Search operates entirely in-memory using **Fuse.js**:

```typescript
import Fuse from "fuse.js";

const fuse = new Fuse(talks, {
  keys: [
    { name: "title", weight: 0.4 },
    { name: "speakers", weight: 0.3 },
    { name: "entities", weight: 0.2 },
    { name: "description", weight: 0.1 },
  ],
  threshold: 0.3,
  ignoreLocation: true,
});
```
