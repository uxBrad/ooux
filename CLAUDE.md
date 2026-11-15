# CLAUDE.md

<!-- second-brain-link -->
## Second Brain link (read first, keep in sync)

This code project's Brain folder is `C:\Users\18563\Desktop\All\Brain\Projects\uxBrad\OOUX\` (OOUX).

**At the start of every session, read:** `README.md`, `SESSION_NOTES.md`, `Backlog.md`, `Memory.md` in that folder (and `DECISIONS.md` before changing direction). Then this file.

**While working:**
- `Backlog.md` is the task list. When an item is finished, change `- [ ]` to `- [x]` in `Backlog.md` right away, and say which items you checked. Add new work we discover as `- [ ]` under Now, Next, or Later.
- Brad also checks items himself. Re-read `Backlog.md` before picking the next task; the file is the source of truth.
- After each commit and push, add a dated entry to `Changelog.md`. Log lasting choices in `DECISIONS.md`.
- `/end` writes the session out: it moves checked items from `Backlog.md` into `Changelog.md`, updates `SESSION_NOTES.md` and `Memory.md`, adds a `Logs/` entry, and updates `Brain/Projects/PULSE.md`.
- Ask before editing Brain notes Brad wrote (anything outside the files above). Never delete files, move them to `Archive/`.
<!-- second-brain-link -->

OOUX: the `ooux-architect` Claude skill. Public repo https://github.com/uxBrad/ooux.

- Skill source is `ooux-architect/`. `All/.claude/skills/ooux-architect` is a Windows junction to it. Edit here only.
- Public repo: no private Brain content, names, or client material.
- No build step. Test by running `/ooux-architect` on a real domain.
- After every change: commit, push, then add an entry to `Brain/Projects/uxBrad/OOUX/Changelog.md`.
