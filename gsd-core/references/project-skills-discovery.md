# Project Skills Discovery

Before execution, find the project-defined skills that fit your task and apply them.

**Discovery steps (shared across all GSD agents):**
1. Check `.claude/skills/` or `.agents/skills/` directory — if neither exists, skip.
2. List available skills (subdirectories that contain a `SKILL.md`).
3. For each skill, read only the YAML frontmatter at the top of its `SKILL.md` (`name`, `description`). If a `SKILL.md` has no `description`, read it in full.
4. Read the full `SKILL.md` only for skills whose `description` fits the current task. A skill you did not read stays available: read its `SKILL.md` later if the task turns out to need it.
5. Load files a `SKILL.md` references (for example under `references/`, `scripts/`, or `rules/`) only when the task needs them.

**Application** — the calling agent's file states how its role applies the skills it loads.
