For **Crimson Notepad**, I would structure development into **6 stages**, where every stage ends with a usable product.

---

# Stage 0 — Project Foundation

### Goal

Get the project running and establish architecture.

### Build

```text
✓ GitHub Organization
✓ crimson-notepad repository
✓ Tauri setup
✓ React frontend
✓ Rust backend
✓ Build Windows executable
✓ Dark theme foundation
✓ App icon
```

### End Result

```text
Crimson.exe launches
```

Nothing more.

---

# Stage 1 — Core Editor

### Goal

Create the simplest usable note app.

### Build

```text
✓ Single note editor
✓ Markdown text area
✓ Auto save
✓ Open .md file
✓ Save .md file
✓ Create new note
✓ Unsaved change protection
```

### UI

```text
+--------------------+
| Crimson            |
+--------------------+
|                    |
| Markdown Editor    |
|                    |
+--------------------+
```

### End Result

User can write notes.

---

# Stage 2 — File System

### Goal

Support multiple notes.

### Build

```text
✓ Notes folder
✓ File explorer
✓ Create note
✓ Rename note
✓ Delete note
✓ Search note
✓ Recent notes
```

### UI

```text
+---------+----------------+
| Notes   | Current Note   |
|---------|                |
| ML.md   |                |
| OS.md   |                |
| AI.md   |                |
+---------+----------------+
```

### End Result

Usable as a daily note-taking app.

---

# Stage 3 — Crimson's Core Feature

This is where Crimson becomes Crimson.

### Goal

Instant access.

### Build

```text
✓ Global shortcut
✓ System tray
✓ Hide to tray
✓ Reopen from shortcut
✓ Fast startup
✓ Last note restore
```

### Workflow

```text
Studying
↓
Ctrl+C+M
↓
Crimson opens
↓
Read roadmap
↓
Ctrl+C+M
↓
Hide
```

### End Result

The original problem is solved.

---

# Stage 4 — Study Mode

### Goal

Make it ideal for students.

### Build

```text
✓ Markdown preview
✓ Mermaid support
✓ Checklists
✓ Code blocks
✓ Tables
✓ Reading mode
```

### Example

````markdown
# ML Roadmap

- Linear Algebra
- Calculus

```mermaid
graph TD
A-->B
````

````

### End Result

Roadmaps and study plans become much easier to read.

---

# Stage 5 — Overlay Mode

This is the killer feature.

### Goal

Reference notes without opening a full app.

### Build

```text
✓ Mini overlay window
✓ Always-on-top mode
✓ Quick note switcher
✓ Transparent background option
✓ Compact reading mode
````

### UI

```text
+------------------+
| ML Roadmap       |
|                  |
| Linear Algebra   |
| Calculus         |
+------------------+
```

No sidebar.

No clutter.

Just content.

### End Result

Feels like a study companion rather than a note app.

---

# Stage 6 — Polish & Distribution

### Goal

Make it professional.

### Build

```text
✓ Settings window
✓ Theme settings
✓ Startup on boot
✓ File associations
✓ Installer
✓ Auto updates
✓ Error logging
✓ About page
```

### Deliverables

```text
CrimsonSetup.exe
```

Double click.

Install.

Use.

---

# Stage 7 — Future (Do NOT Build Yet)

Only if people actually use it.

### Possible Features

```text
○ Tags
○ Note links
○ AI summaries
○ Cloud sync
○ Mobile app
○ Plugin system
○ Collaboration
```

---

# Development Priority

If you started tomorrow:

### Month 1

```text
Stage 0
Stage 1
Stage 2
```

You now have:

```text
A lightweight markdown app
```

### Month 2

```text
Stage 3
Stage 4
```

You now have:

```text
A useful study tool
```

### Month 3

```text
Stage 5
Stage 6
```

You now have:

```text
A product people can install
```

The most important stage is **Stage 3**. That's where Crimson stops being "another markdown editor" and starts solving the specific problem that led you to create it.
