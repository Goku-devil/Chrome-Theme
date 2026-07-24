# Custom Chrome Home Documentation

**Custom Chrome Home** is a Chromium extension that replaces the default New Tab page
with a highly customizable productivity dashboard.

---

## 1. Overview

The extension provides a centralized, distraction-free hub featuring:

- Live clock and date display
- Google search with autocomplete suggestions
- Editable quick shortcuts with automatic favicons
- Built-in task manager with persistent state
- Extensive customization (themes, layouts, and animated backgrounds)
- Optional terminal-style visual mode for a developer aesthetic

---

## 2. Project Structure

| Path | Purpose |
|---|---|
| `manifest.json` | Chrome extension manifest (MV3) and New Tab override configurations. |
| `newtab.html` | Main page markup and UI structure. |

| `style.css` | Styling, layouts, themes, and animation templates. |
| `script.js` | Core application logic (search, shortcuts, tasks, settings, and persistence). |
| `assets/image.png` | Default background image. |
| `assets/icons8-home-48.png` | Extension and New Tab icon. |
| `INSTALL.md` | Quick installation guide. |

---

## 3. Installation

For detailed manual installation instructions, please refer to the `INSTALL.md` file.

To install the extension directly on Microsoft Edge, download it from the official store:
**[Install from the Edge Add-on
Store](https://microsoftedge.microsoft.com/addons/detail/pfhncogmoeopdpfokomlldgigafbbgdk)**

---

## 4. Runtime Features

### 4.1 Search
- Submits standard queries directly to Google.
- Detects URL-like input and navigates to the site directly.
- Fetches real-time suggestions using the Google suggestions endpoint.
- Supports full keyboard navigation (`ArrowUp`, `ArrowDown`, `Enter`, `Escape`).

### 4.2 Shortcuts
- Populates with default shortcuts on the first load.
- Allows users to add, edit, and delete custom shortcuts.
- Automatically fetches and displays site favicons using the Google favicon service.
- Saves all shortcut data to local storage.

### 4.3 Task Manager
- Add tasks via the main form or a quick-add modal.
- Toggle tasks between complete and incomplete states.
- Delete individual tasks, clear all completed tasks, or wipe the entire list.
- **Smart Alert:** Displays a warning modal when opening a new tab if there are pending
tasks.

### 4.4 Customization
- **Themes:** `ocean`, `emerald`, `sunset`, `mono`
- **Visual Modes:** Standard or `terminal-mode` (command-line aesthetic)
- **Layouts:** `centered`, `wide`, `minimal`
- **Background Templates:**
`aurora`, `prism`, `dark-wave`, `neon-grid`, `sunrise`, `midnight`, `fluid-flow`, `pulse-ring`,
`spiral-orbit`, `bouncing-bg`, `custom`
- **Custom Template Controls:** Fine-tune the primary color, secondary color, glow color,
and motion speed.
- **Custom Image:** Support for uploading a personal background image.

---

## 5. Data Persistence

All user data and preferences are saved locally in the browser profile using local storage. No
external databases are used.

| Key | Description |
|---|---|
| `customHomeShortcuts` | Array of shortcut objects: `{ name, url }` |
| `customHomeTasks` | Array of task objects: `{ id, text, done, createdAt }` |
| `customHomeSettings` | Object storing theme, layout, template, and background
preferences. |

---

## 6. Permissions and External Calls

Declared in `manifest.json`:
- `https://suggestqueries.google.com/*` — Used for fetching search autocomplete
suggestions.
- `https://www.google.com/*` — Used for executing searches and retrieving favicons.

*Privacy Note: No backend tracking service is used. All state and data remain completely
local to the user&#39;s browser profile.*

---

## 7. Development Notes

- **Manifest Version:** MV3
- **New Tab Override Entry:** `&quot;chrome_url_overrides&quot;: { &quot;newtab&quot;: &quot;newtab.html&quot; }`
- **Initialization Sequence:**
1. Load shortcuts
2. Load tasks
3. Load settings
4. Apply user settings to the DOM
5. Render the final UI

---

## 8. Troubleshooting

### Extension does not update after editing code
1. Navigate to `chrome://extensions`.
2. Click the **Reload** icon on the extension&#39;s card.
3. Open a fresh new tab to see the changes.

### Search suggestions are not appearing
- Check your active internet connection.
- Verify that the host permissions in `manifest.json` have not been accidentally removed or
modified.

### Background or settings reset unexpectedly
- Ensure browser settings aren&#39;t configured to clear local storage on exit.
- Reapply your settings and verify if your specific browser profile allows persistent storage
for unpacked extensions.

---

## 9. Version History

- **Extension version:** `1.1.2`
- **Last documentation update:** July 24, 2026
