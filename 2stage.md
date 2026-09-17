# Stage 2 — File System

> Goal: Support multiple notes.
> End Result: Usable as a daily note-taking app.

## 1. Objective

Notes folder + explorer + CRUD + search + recent. Turn Stage 1 single editor into multi-note app.

## 2. Scope

```text
✓ Notes folder (default: Documents/Crimson, configurable later)
✓ File explorer (list .md only)
✓ Create note
✓ Rename note
✓ Delete note (confirm + trash/recycle where possible)
✓ Search note (by filename + content substring)
✓ Recent notes (last 10 opened)
```

Out of Scope: global shortcut/tray (Stage 3), preview (Stage 4).

## 3. UI

```text
+---------+----------------+
| Notes   | Current Note   |
|---------|                |
| ML.md   |                |
| OS.md   |                |
| AI.md   |                |
+---------+----------------+
```

- Left sidebar 240px, collapsible
- Sidebar: Search input top, file list middle, New button bottom
- Right: Stage 1 editor reused
- Context menu on file: Rename / Delete / Reveal in Explorer
- Recent section on top when search empty

## 4. Tasks

```text
[ ] Rust FS layer: list_notes, create_note, rename_note, delete_note, search_notes
[ ] Sanitize filenames (no \ / : * ? " < > |, auto .md ext, dedupe "name (1).md")
[ ] Frontend store: activePath, fileList, recentPaths (localStorage)
[ ] File watcher: refresh on external change (Tauri notify / poll 2s fallback)
[ ] Search: debounced, filename-first ranking
[ ] Empty / error / loading states for explorer
[ ] Keyboard: Ctrl+N new, Ctrl+P quick open (basic), Delete handling
```

## 5. Data Model

```text
notes_dir/
  ML.md
  OS.md
```

```ts
type NoteMeta = { name: string; path: string; mtime: number }
```

## 6. Definition of Done

```text
✓ Create/rename/delete reflects instantly on disk + UI
✓ Search finds by name in <100ms for 500 notes
✓ Recent persists across restart
✓ No data loss on rename while dirty (flush first)
```

## 7. Test Checklist
- [ ] 500 dummy .md files still render list smoothly (virtualize if needed)
- [ ] Rename to existing name blocked with message
- [ ] Delete dirty open note asks confirm
- [ ] External edit in VS Code appears after refocus

## 8. Next Stage
Stage 3 — Instant access (global shortcut + tray).
