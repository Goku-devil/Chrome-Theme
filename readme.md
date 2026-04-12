# Chrome Home Page — Feature Documentation

> **Page Title:** Home
> **File Location:** G:/Chrome Themes/newtab.html
> **Purpose:** A personalized productivity-focused browser home page

---

## 1. Header / Branding Section

- **Brand Label:** CHROME HOME — a small uppercase label at the top center
- **Main Headline:** Start Focused — large bold text serving as the page motto
- **Subtitle:** Search with Google or jump to your shortcuts

---

## 2. Live Clock & Date Widget

- **Clock Display:** Shows current time in 12-hour format with AM/PM
- **Date Display:** Shows full date in readable format
- **Live Updates:** Both update in real time using JavaScript

---

## 3. Tech Quotes Section

- **Section Label:** TECH QUOTES in teal uppercase text
- **Quote Display:** Curated tech/motivational quote with quotation mark icon
- **Author Attribution:** Author name in all caps, right-aligned
- **Dynamic Updates:** Uses aria-live for accessibility and auto-refresh

---

## 4. Google Search Bar

- **Function:** Fully functional search input that submits to Google Search
- **Dual Purpose:** Search queries or direct URL navigation
- **Design:** Wide rounded bar centered below clock/quote section

---

## 5. Shortcuts Section

- **Pre-configured Shortcuts (5):** Google, YouTube, Gmail, GitHub, Drive
- **Click Behavior:** Each tile opens the respective website immediately

---

## 6. Add Shortcut Button

- **Appearance:** Dashed-outline button with + symbol
- **Dialog Fields:** Name and URL inputs
- **Action Buttons:** Cancel and Add

---

## 7. ADD TASK Button

- **Location:** Bottom-right corner of the page
- **Click Behavior:** Opens Add Task modal with text input
- **Purpose:** Lightweight task manager for quick to-dos

---

## 8. Customize Button & Panel

### 8.1 Theme Selector
- **Options:** Ocean, Emerald, Sunset, Mono

### 8.2 Command-Line Aesthetic Toggle
- **Effect:** Swaps page into dark monospace workspace

### 8.3 Main Page Template
- **Options:** Centered, Wide, Minimal

### 8.4 Background Template
- **Options:** Aurora, Prism, Dark Wave, Neon Grid, Sunrise, Midnight, Fluid Flow, Pulse Ring, Spiral Orbit, Bouncing BG, Custom

### 8.5 Background Image Uploader
- **Function:** Upload custom image as page background

### 8.6 Reset & Done Buttons
- **Reset:** Reverts to defaults
- **Done:** Saves changes and closes panel

---

## Summary Table

| # | Feature | Type | Description |
|---|---|---|---|
| 1 | Header | Static | Brand label + Start Focused headline |
| 2 | Clock | Dynamic | Live 12-hour time display |
| 3 | Date | Dynamic | Live full date display |
| 4 | Tech Quotes | Dynamic | Rotating tech quote with author |
| 5 | Search Bar | Interactive | Google search or URL navigation |
| 6 | Shortcuts | Interactive | 5 clickable website tiles |
| 7 | Add Shortcut | Modal | Create custom shortcuts |
| 8 | Add Task | Modal | Quick task capture |
| 9 | Customize | Panel | Themes templates backgrounds |
| 10 | Theme Selector | Dropdown | Ocean Emerald Sunset Mono |
| 11 | Command-Line Toggle | Switch | Dark monospace aesthetic |
| 12 | Page Template | Buttons | Centered Wide Minimal |
| 13 | Background Templates | Grid | 10 animated backgrounds |
| 14 | Custom Image | File Input | Upload own background |

---

## Quick Reference Guide

| Action | How To |
|---|---|
| Search the web | Click search bar, type query, press Enter |
| Open a website | Type URL in search bar, press Enter |
| Open a shortcut | Click any shortcut tile |
| Add a shortcut | Click + button, enter name and URL, click Add |
| Add a task | Click ADD TASK, type task, click Add |
| Change theme | Click Customize, select from Theme dropdown |
| Change background | Click Customize, select from Background Template grid |
| Upload custom image | Click Customize, click Choose File |
| Reset to defaults | Click Customize, click Reset |
| Save customizations | Click Customize, click Done |

---

*Documentation generated on April 12, 2026*`;

const blob = new Blob([md], {type: 'text/markdown'});
const url = URL.createObjectURL(blob);
const a = document.createElement('a');
a.href = url;
a.download = 'ChromeHome_FeatureDocs.md';
a.click();
URL.revokeObjectURL(url);