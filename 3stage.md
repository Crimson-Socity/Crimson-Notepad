# Stage 3 — Crimson's Core Feature (Instant Access)

> This is where Crimson becomes Crimson.
> Goal: Instant access. End Result: The original problem is solved.

## 1. Objective

User studying -> hotkey -> Crimson opens -> read roadmap -> hotkey -> hide. No tab switching, no loading.

Workflow:
```text
Studying
↓
Ctrl+C+M (default, remappable later)
↓
Crimson opens
↓
Read roadmap
↓
Ctrl+C+M
↓
Hide
```

## 2. Scope

```text
✓ Global shortcut (register/unregister, default Ctrl+Shift+M — avoid Ctrl+C+M conflict)
✓ System tray (show/hide, quit, icon)
✓ Hide to tray (close button = hide, not quit)
✓ Reopen from shortcut (toggle show/hide + focus)
✓ Fast startup (<800ms to visible on SSD)
✓ Last note restore (reopen activePath + cursor on launch)
```

Out of Scope: overlay always-on-top (Stage 5), settings UI full (Stage 6 — use config file for now).

## 3. Tasks

```text
[ ] Tauri global-shortcut plugin: toggle_window command
[ ] Tray menu: Show / Hide / New Note / Quit
[ ] Window behavior: close -> hide, dock icon click -> show
[ ] Single instance: second launch focuses existing window
[ ] Persist: activePath, window size/pos, notes_dir in tauri store / config.json
[ ] Startup perf: lazy-load explorer, defer search index, no blocking FS scan >200ms
[ ] Edge: shortcut conflict detection + fallback toast
```

## 4. UX Requirements

- Toggle latency <150ms
- Focus editor on show, restore cursor position
- Hide must preserve dirty state (no save prompt on hide)
- Tray tooltip: "Crimson Notepad — press Ctrl+Shift+M"

## 5. Definition of Done

```text
✓ Fresh boot -> hotkey -> note visible in <1s
✓ Close (X) keeps process in tray, no data loss
✓ Quit from tray fully exits
✓ Restart restores last note + cursor
✓ Shortcut works when VS Code / browser focused
```

## 6. Test Checklist
- [ ] Hotkey while fullscreen game/app doesn't steal badly (guard)
- [ ] Kill + relaunch restores state
- [ ] Unregister on quit (no ghost hotkey)
- [ ] Works after Windows sleep/resume

## 7. Why This Matters

> The most important stage. This is where Crimson stops being "another markdown editor" and starts solving the specific problem that led to its creation.

Do not proceed to Stage 4 until toggle feels instant.

## 8. Next Stage
Stage 4 — Study Mode (preview + Mermaid).
