# Stage 1 — Core Markdown Editor

## Objective

Build the first usable version of Crimson Notepad.

At the end of Stage 1, users should be able to create, edit, and save Markdown notes locally.

This stage focuses on writing notes, not managing them.

---

## Success Criteria

The following workflow must work:

```text
Launch Crimson
↓
Create Note
↓
Write Markdown
↓
Auto Save
↓
Close App
↓
Reopen App
↓
Note Restored
```

---

## Deliverables

### Markdown Editor

Support:

```markdown
# Heading

## Subheading

**Bold**

*Italic*

- List Item

1. Numbered Item

`Inline Code`
```

---

### Note Creation

Users can:

- Create a new note
- Open existing note
- Edit note
- Save note

---

### Auto Save

Requirements:

- Save automatically
- No save button required
- Prevent accidental data loss

Behavior:

```text
User types
↓
Pause for 2 seconds
↓
Note saved automatically
```

---

### Single Note Mode

Stage 1 supports:

```text
1 active note
```

No folders.

No note explorer.

No search.

No note switching.

Those belong to Stage 2.

---

## UI Requirements

### Layout

```text
+--------------------------------------+
| Crimson Notepad                      |
+--------------------------------------+
|                                      |
|                                      |
|       Markdown Editor                |
|                                      |
|                                      |
+--------------------------------------+
| Saved                               |
+--------------------------------------+
```

---

### Theme

Theme:

```text
Dark
```

Primary Color:

```text
Crimson Red
```

Background:

```text
Near Black
```

Accent:

```text
Deep Crimson
```

---

## Technical Requirements

### File Format

Supported:

```text
.md
```

Only Markdown files.

---

### Local Storage

Default directory:

```text
Documents/
└── CrimsonNotes/
```

Example:

```text
Documents/
└── CrimsonNotes/
    └── note.md
```

---

### Persistence

On startup:

```text
Load last opened note
```

On shutdown:

```text
Remember current note
```

---

## Features Included

### Included

- Markdown editing
- Auto save
- Create note
- Open note
- Save note
- Restore last note
- Dark theme

---

### Not Included

- Search
- Multiple notes
- Folders
- Mermaid
- Global shortcuts
- System tray
- Tags
- Templates
- Sync
- Plugins

---

## Tasks

### Task 1

Create editor component.

Status:

```text
Pending
```

---

### Task 2

Implement local file saving.

Status:

```text
Pending
```

---

### Task 3

Implement auto save.

Status:

```text
Pending
```

---

### Task 4

Load existing Markdown files.

Status:

```text
Pending
```

---

### Task 5

Restore last opened note.

Status:

```text
Pending
```

---

### Task 6

Apply Crimson theme.

Status:

```text
Pending
```

---

### Task 7

Perform Windows build test.

Status:

```text
Pending
```

---

## Exit Conditions

Stage 1 is complete when:

- User can create a note
- User can write Markdown
- Notes save automatically
- Notes persist after restart
- Application remains stable
- Windows executable builds successfully

---

## User Story

As a student,

I want to quickly write and save Markdown notes,

so I can keep important information available without relying on large note-taking applications.

---

## Next Stage

Stage 2 — Note Management

Features:

- Multiple notes
- Note explorer
- Search
- Rename note
- Delete note
- Recent notes
