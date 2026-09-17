# Stage 5 — Overlay Mode (Killer Feature)

> Goal: Reference notes without opening a full app.
> End Result: Feels like a study companion rather than a note app.

## 1. Objective

Mini always-on-top overlay: just content, no sidebar, no clutter. Quick switch notes while coding/studying.

UI:
```text
+------------------+
| ML Roadmap       |
|                  |
| Linear Algebra   |
| Calculus         |
+------------------+
```

## 2. Scope

```text
✓ Mini overlay window (separate Tauri window: 360x480 default, resizable)
✓ Always-on-top mode (toggle, persists)
✓ Quick note switcher (Ctrl+P / Ctrl+K fuzzy list)
✓ Transparent background option (opacity slider 40-100%)
✓ Compact reading mode (preview-only, no editing in overlay v1)
```

Out of Scope: editing in overlay (allow later), full settings (Stage 6).

## 3. Tasks

```text
[ ] Second Tauri window `overlay`: frameless, compact, alwaysOnTop toggle
[ ] Shared state: activePath sync between main + overlay
[ ] Quick switcher: fuzzy search filenames, ↑↓ + Enter, Esc close
[ ] Pin/unpin button, opacity control, click-through? NO (keep interactive)
[ ] Hotkeys: separate overlay toggle (e.g. Ctrl+Shift+O) + main toggle unchanged
[ ] Position memory: save overlay x/y/w/h
[ ] Perf: overlay render <200ms, no full explorer load
```

## 4. UX Rules

- No sidebar, no toolbar — only title bar (drag) + content + pin/close
- Follows main window theme (dark crimson)
- Hide main window does not kill overlay (independent toggles)
- Opacity <100% still keeps text readable (blur backdrop)

## 5. Definition of Done

```text
✓ Study + code side-by-side: overlay stays on top of VS Code/browser
✓ Ctrl+P switches note in overlay in <300ms
✓ Restart restores overlay pos/size/pin/opacity
✓ No focus steal: overlay toggle doesn't break typing in other app until clicked
```

## 6. Test Checklist
- [ ] Overlay over YouTube fullscreen — behaves (no crash)
- [ ] Toggle pin 20x, no z-order bug
- [ ] Switch 50 notes rapidly, no stale render
- [ ] 2 windows + tray quit closes both cleanly

## 7. Next Stage
Stage 6 — Polish & Distribution.
