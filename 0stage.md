# Stage 0 — Foundation

## Objective

Establish the technical foundation of Crimson Notepad.

At the end of Stage 0, the application does not need to be useful yet.

The goal is simply:

> Launch Crimson Notepad as a native Windows application.

---

## Success Criteria

The following must work:

- Application launches successfully
- Dark theme loads correctly
- Custom Crimson icon appears
- Windows executable can be built
- Git repository is configured
- Development environment is stable

---

## Deliverables

### Repository Setup

Create repository:

```text
crimson-notepad
```

Required files:

```text
README.md
LICENSE
.gitignore
```

---

### Project Structure

```text
crimson-notepad/
│
├── assets/
│   └── logo.png
│
├── docs/
│   ├── DRD.md
│   ├── PRD.md
│   ├── EDR.md
│   ├── ERD.md
│   ├── TRD.md
│   └── STAGE-0.md
│
├── src/
├── src-tauri/
│
├── README.md
├── package.json
└── tauri.conf.json
```

---

## Technology Stack

### Frontend

- React
- TypeScript

### Backend

- Rust

### Desktop Runtime

- Tauri

### Package Manager

- npm

---

## UI Foundation

Create a basic application window.

Requirements:

- Dark background
- Crimson accent color
- Custom title
- Responsive layout

Example:

```text
+--------------------------------+
| Crimson Notepad               |
|                               |
|     Stage 0 Running...        |
|                               |
+--------------------------------+
```

---

## Branding

Organization:

```text
Crimson Society
```

Application:

```text
Crimson Notepad
```

Tagline:

```text
Write less. Switch less. Focus more.
```

---

## Build System

Application must compile successfully.

Commands:

```bash
npm install
npm run tauri dev
```

Production build:

```bash
npm run tauri build
```

Expected output:

```text
CrimsonNotepad.exe
```

---

## Tasks

### Task 1

Initialize repository.

Status:

```text
Pending
```

---

### Task 2

Install Tauri.

Status:

```text
Pending
```

---

### Task 3

Create React application.

Status:

```text
Pending
```

---

### Task 4

Configure TypeScript.

Status:

```text
Pending
```

---

### Task 5

Add Crimson branding.

Status:

```text
Pending
```

---

### Task 6

Create initial application window.

Status:

```text
Pending
```

---

### Task 7

Build Windows executable.

Status:

```text
Pending
```

---

## Exit Conditions

Stage 0 is complete when:

- Application launches
- Dark UI renders correctly
- Logo appears correctly
- Tauri build succeeds
- Windows executable is generated

---

## Next Stage

Stage 1 — Core Markdown Editor

Features:

- Markdown editing
- Auto save
- Open note
- Save note
- Single note support
