# Stage 6 — Polish & Distribution

> Goal: Make it professional.
> Deliverable: `CrimsonSetup.exe` — Double click. Install. Use.

## 1. Objective

Settings, startup, file association, installer, auto-update, logging, about. Ship-ready.

## 2. Scope

```text
✓ Settings window (notes folder, hotkeys, theme, startup, overlay defaults)
✓ Theme settings (dark crimson default + contrast options, font size)
✓ Startup on boot (Windows autostart toggle)
✓ File associations (.md open with Crimson)
✓ Installer (NSIS/WiX via Tauri bundler -> CrimsonSetup.exe)
✓ Auto updates (Tauri updater: signature + release feed)
✓ Error logging (local log file + view in About)
✓ About page (version, links, check update)
```

## 3. Tasks

```text
[ ] Settings persistence: config.json schema + migration (v1)
[ ] Hotkey remap UI with conflict validation
[ ] Autostart: tauri autostart plugin
[ ] Assoc .md: registry via installer + "Open with Crimson" context
[ ] Bundler: icon set, version from package.json/Cargo.toml sync
[ ] Updater: public key, GitHub releases feed, staged rollout flag
[ ] Logger: Rust tracing -> %APPDATA%/Crimson/logs/crimson.log (rotate)
[ ] About: version, changelog link, Copy diagnostics button
[ ] Final QA: clean Win10 + Win11 VM install/uninstall test
```

## 4. Definition of Done

```text
✓ Fresh user installs CrimsonSetup.exe with no manual steps
✓ .md double-click opens in Crimson
✓ Reboot -> autostart (if enabled) restores tray + last note
✓ Update prompt appears on new release, installs on restart
✓ All errors write to log, no silent failures, no panic dialog
```

## 5. Test Checklist
- [ ] Install / uninstall leaves no orphan hotkey/tray
- [ ] Upgrade from previous version migrates config
- [ ] Offline launch works (updater fails soft)
- [ ] Log file caps at ~5MB with rotation
- [ ] About shows correct version/hash

## 6. Release Gate

Do not mark Stage 6 done until:
1. `CrimsonSetup.exe` tested on clean VM
2. Stage 0-5 regression pass (editor, explorer, hotkey, preview, overlay)
3. README install section updated

## 7. Next Stage
Stage 7 — Future (do NOT build yet).
