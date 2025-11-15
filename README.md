# 🦄 0days Uncover — Advanced On-Page Recon & Visibility Toolkit  
### *Modernized & Expanded from the original bookmarklet by **lostsec aka coffin XP***

0days **Uncover** is a powerful, single-click **bookmarklet** for bug bounty hunters, pentesters, and web security researchers who need **instant on-page recon, DOM extraction, script scraping, and anti-overlay / anti-obfuscation tools** — without installing anything.

This version is a **heavily upgraded, fully rewritten** evolution of the original tool by **lostsec aka coffin XP**, preserving the spirit of the original bookmarklet while introducing **major enhancements** across UI, functionality, extraction accuracy, and usability.

---

## 🚀 Features

### 🔎 **Full URL Extraction Engine**
Uncover automatically collects:
- All DOM-referenced URLs (`href`, `src`, `action`)
- All `<script>` content via **real script fetching + regex parsing**
- All browser-known resource entries via `performance.getEntriesByType('resource')`
- Hidden inline references (`"/path"` / `'../file.js'` / `` `/api/...` ``)

This gives you the **maximum possible surface** without scanning the host externally.

---

### 🎛️ **Interactive, Resizable Recon Panel**
- Drag-to-resize panel  
- Dark/purple neon UI  
- Collapsible UI mode  
- Real-time filtering by:
  - URL substring
  - File type (`.php`, `.js`, `.json`, `.api`, `.asp`, etc.)
  - Domain-only toggle

---

### 📤 **Export & Copy Options**
One-click:
- Copy results as **.txt**  
- Copy results as **.json**  
- Export to `0days_urls.txt`

Useful for automated workflows and recon pipelines.

---

### 🫥 **Unhide / De-obfuscate Tooling (Major Upgrade)**
This version includes a highly enhanced **anti-obfuscation engine**, allowing you to instantly unhide:
- Disabled elements
- Readonly fields
- Hidden, inert, aria-hidden nodes
- Blurred or obscured content
- CSS-hidden components
- Overlaying classes (`veil`, `overlay`, `blur`, `modal-backdrop`, etc.)

This is extremely useful for:
- Hidden admin panels
- Shadow UI components
- Form discovery
- Bypassing UI gating mechanisms

---

### 🧼 **Anti-Overlay Nuker**
Removes **aggressive fixed-position overlays** (e.g., paywalls, popups, darkeners) without touching the panel.

Works by checking extremely high z-index elements & safely removing them.

---

### 📡 **Real-Time Script Scanner**
Every external `<script src="">` is fetched in real-time and scanned for paths using a robust regex.
This scrapes:
- Hidden API endpoints
- JS-only URLs
- Internal routes
- Static asset maps  
- Lazy-loaded endpoints

---

## 📦 Installation (Bookmarklet)

1. Copy the entire JavaScript code (minified or full).
2. Create a new bookmark.
3. Paste the code into the **URL** field.
4. Visit *any* website → Click the bookmarklet → Panel launches instantly.

---

## 🛠️ Usage Guide

### ▶️ **Launching**
Click the bookmarklet on any page.  
A neon purple panel will slide up from the bottom of the screen.

---

### 🔍 **Filtering URLs**
Use:
- **Search bar** → text match  
- **File type selector**  
- **Domain-only checkbox**  

Results update instantly.

---

### 🧩 **Unhide Elements**
Click **Unhide Elements** to unlock:
- Hidden forms  
- Disabled UI  
- Greyed-out admin buttons  
- Obscured content  
- Blurred layers  

Useful for analysing real UI structure without JS interference.

---

### 🛡️ **Remove Overlays**
Click **Remove Overlays** to remove:
- Paywalls  
- Dark screens  
- Modal blockers  
- “Sign up to continue” shields  

Only extreme high-z-index elements are removed.

---

### 📥 **Exporting**
Use:
- **Copy .txt**
- **Copy .json**
- **Export .txt**

This is useful for piping into:
- gf
- xargs
- httpx
- nuclei
- dirsearch
- custom recon scripts

---

## 🧬 Technical Notes

### ✔️ Internal Script Scanner  
Fetches every `<script src="">` via `fetch()` + `AbortController`.

### ✔️ DOM Collector  
Grabs everything from:
- `<a>`
- `<script>`
- `<img>`
- `<link>`
- `<form>`
- Performance API entries

### ✔️ Smart Rendering System  
Ensures constant performance even on heavy pages.

---

## 🙏 Credits

### 💀 Original Creator  
**lostsec aka coffin XP**

The original bookmarklet concept and early implementation belong to him.

### 🦄 Major Rewrite & Upgrades  
This version — **0days Uncover** — includes substantial new functionality, improved UI/UX, stability upgrades, new modules (overlay removal, advanced filetype search, etc etc), as well as refined regex extraction, and full script scanning, implemented by:

**0days**  
https://github.com/TheEmperorsPath  
https://youtube.com/@0dayscyber

---

## 📜 Disclaimer

This tool is intended **only** for:
- Educational use  
- Authorized penetration testing  
- Legitimate bug bounty research  

Do **not** use this tool on systems you do not own or have permission to test.

---

## ⭐ If You Use This Tool  
Please credit **0days** and **lostsec / coffin XP** where appropriate.

---
