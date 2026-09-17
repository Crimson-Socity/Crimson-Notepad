# Stage 4 — Study Mode

> Goal: Make it ideal for students.
> End Result: Roadmaps and study plans become much easier to read.

## 1. Objective

Reading-quality markdown rendering for study notes: preview, Mermaid, checklists, code, tables, reading mode.

## 2. Scope

```text
✓ Markdown preview (GFM)
✓ Mermaid support (graph TD etc., lazy-load)
✓ Checklists (- [ ] / - [x] clickable in preview)
✓ Code blocks (syntax highlight + copy button)
✓ Tables (styled, horizontal scroll)
✓ Reading mode (distraction-free: hide sidebar, larger type, centered 720px)
```

Out of Scope: overlay mini window (Stage 5), WYSIWYG editing.

## 3. UI Modes

- Edit | Split | Preview toggle (Ctrl+E / Ctrl+Shift+V style)
- Reading mode button hides sidebar + toolbar, `Esc` exits
- Mermaid error block shows code fallback, never crashes page

Example must render:
````markdown
# ML Roadmap

- Linear Algebra
- Calculus

```mermaid
graph TD
  A-->B
```
````

## 4. Tasks

```text
[ ] Add markdown pipeline: remark-gfm + rehype-highlight + mermaid
[ ] Sanitize HTML (rehype-sanitize) — no raw script exec
[ ] Checklist: click toggles source and auto-saves
[ ] Code: language label + copy-to-clipboard
[ ] Tables: responsive wrapper
[ ] Reading mode layout + typography scale + print-friendly
[ ] Perf: render debounce, virtualize for >2000-line notes, cache Mermaid SVG
```

## 5. Definition of Done

```text
✓ 2000-line roadmap renders <500ms
✓ Mermaid diagram renders or shows readable fallback
✓ Checklist click persists to .md file
✓ Edit/Preview scroll sync (basic, approx ok)
✓ Reading mode readable at 125% zoom
```

## 6. Test Checklist
- [ ] Paste ML/OS/AI roadmap with tables + code + mermaid — no breakage
- [ ] XSS payload in note does not execute
- [ ] Toggle Edit/Split/Preview preserves cursor + scroll
- [ ] Offline works (bundle mermaid, no CDN)

## 7. Next Stage
Stage 5 — Overlay Mode.
