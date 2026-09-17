# Stage 7 — Future (Do NOT Build Yet)

> Only if people actually use it.

## 1. Rule

Do not start Stage 7 until Stage 6 `CrimsonSetup.exe` is shipped and real usage feedback exists. No premature scope.

## 2. Possible Features

```text
○ Tags (#tag index + filter)
○ Note links ([[wiki-link]] + backlinks)
○ AI summaries (local-first, opt-in, no cloud by default)
○ Cloud sync (bring-your-own folder first, then optional sync)
○ Mobile app (read-only companion first)
○ Plugin system (sandboxed JS, minimal API)
○ Collaboration (CRDT — last, highest cost)
```

## 3. Evaluation Criteria (for each idea)

- [ ] Does it preserve "one shortcut away" speed? If no, reject.
- [ ] Does it keep local-first + lightweight? If no, needs strong justification.
- [ ] Can it ship in <2 weeks as MVP? If no, split or defer.
- [ ] Do ≥5 real users request it? If no, defer.

## 4. Suggested Order (if validated)

1. Tags (cheapest, high study value)
2. Note links + backlinks
3. Plugin system (lets others build sync/AI)
4. AI summaries (opt-in)
5. Cloud sync
6. Mobile
7. Collaboration (last)

## 5. Non-Goals

- Second-brain / Obsidian clone — Crimson is fast access, not complex organization.
- Account system / mandatory cloud — violates local-first philosophy.

## 6. Exit Condition

Pick at most 1-2 items from above per cycle, write a new `7.x-feature.md` spec before coding.
