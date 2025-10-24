# 🏜️ Geo Cactus — Style Guide

A visual and structural reference for the **Geo Cactus** website.  
Focus: *clarity, nature-inspired minimalism, and technical precision.*

---

## 🌈 Color Palette

| Purpose | Name | Hex | Notes |
|----------|------|-----|-------|
| **Primary** | Cactus Green | `#3A7257` | Brand accent, buttons, headers |
| **Secondary** | Desert Sand | `#E4CFA3` | Background highlights, neutral blocks |
| **Accent** | Tech Cyan | `#00C6B0` | Links, highlights, interactive elements |
| **Text (Light Mode)** | Charcoal | `#1F1F1F` | Main body text |
| **Text (Dark Mode)** | Mist White | `#E6F6F5` | For dark theme readability |
| **Background (Light)** | Soft Beige | `#F8F7F3` | Default body background |
| **Background (Dark)** | Deep Green Black | `#0A1511` | Used when dark theme is active |
| **Shadow** | — | `rgba(0,0,0,0.1)` | Subtle elevation for cards & nav |

> **Tip:** Use green and cyan sparingly to keep the interface calm and natural. Avoid large, bright blocks of cyan.

---

## ✍️ Typography

| Type | Font | Fallback | Weight | Usage |
|------|------|-----------|--------|--------|
| **Headings** | `"Poppins"`, `"Montserrat"` | `sans-serif` | 600–700 | Logos, section headers |
| **Body Text** | `"Inter"` | `system-ui, sans-serif` | 400–500 | Paragraphs, navigation, UI text |
| **Code / Data** | `"Courier New"` | `monospace` | 400 | Inline code, coordinates |

**Base Font Size:** `16px`  
**Line Height:** `1.6`  
**Letter Spacing:** `0.5px` for headings  

---

## 📐 Layout

### Grid & Spacing

- **Container Width:** `90–100%` (max-width: `1200px`)
- **Section Padding:** `60px 10%`
- **Card Radius:** `12px`
- **Shadow:** `0 4px 16px rgba(0,0,0,0.1)`
- **Gutters:** `20px`

### Responsive Rules

- Stack columns below **800px** viewport width.  
- Prioritize readability and spacing on small screens.

---

## 🧭 Navigation

```
Home | Software | Data | Articles | About
```

- Fixed or sticky top navigation bar.  
- Links change color on hover (`color: var(--cyan)`).  
- **Logo:** Text + circular emblem (`GC`) resembling a stylized cactus sphere.

---

## 🎯 Buttons

| Type | Background | Text | Border | Hover |
|------|-------------|-------|---------|--------|
| **Primary (CTA)** | Cactus Green | White | None | Switch to cyan |
| **Secondary** | Transparent | Cyan | `1px solid cyan` | Fill cyan, dark text |

**Shape:** Rounded (`8px`)  
**Padding:** `10px 18px`  
**Font Weight:** `bold`

---

## 🧱 Components

### Cards

```css
.card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.1);
  padding: 16px;
  transition: transform 0.2s;
}
.card:hover {
  transform: translateY(-4px);
}
```
* Used for Software, Data, and Articles sections.
* In dark mode, background becomes #13241C.

### Hero Section

* Two-column layout (text + visual map block).
* Subtle animated background grid or contour lines.
* Keep text concise and engaging.

**Tagline Examples:**

> “Mapping the world, one dataset at a time.”
> “Where geography meets code.”

### Footer

* Center-aligned text.
* Include coordinates or timestamp, e.g.:
  `Geo Cactus © 2025 · 🌍 0° N 0° E`
* Use a soft green or gray tone.

## 🌙 Dark Mode

Activated by adding:
```html
<html data-theme="dark">
```
**Color swaps:**
* Background → #0A1511
* Text → #E6F6F5
* Card → #13241C
* Links and accents remain cyan for consistency.

## 💫 Animation & Interaction

* Use only **microinteractions** (hover effects, soft transitions).
* No heavy parallax or complex animations.
* Example background animation:
```css
@keyframes pan {
  from { background-position: 0 0; }
  to { background-position: 1000px 1000px; }
}
```

## 🔍Iconography

* **Style:** Geometric outline icons (SVG preferred).
* **Stroke Width:** ~2px.
* **Common motifs:**
  * 🗺️ Maps & grids
  * 🌵 Cactus imagery
  * 📡 Signals / coordinates
  * 🧭 Compass and exploration
 
## 🧩 File Structure
```
/geocactus
│
├── index.html
├── /css
│   └── style.css
├── /js
│   └── main.js
├── /images
│   └── logo.svg
└── STYLEGUIDE.md
```

## 📜 Voice & Tone

* **Voice:** Confident, approachable, precise.
* **Tone:** Informative, grounded, and transparent.
* **Style:** Short sentences. Minimal jargon.
  Emphasize discovery, clarity, and openness.

**Example:**

> “Geo Cactus provides open geospatial tools for researchers, developers, and explorers.
> Our mission is to make mapping simple, accessible, and efficient.”
