---
type: Changed
pr: 5079
---
**GSD's agents now read only the project skills that fit their task** — the 21 discovery agents, and the execute, plan and quick workflows that spawn them, used to read every project `SKILL.md` in full on every spawn, following steps written for one skill pack (gsd-build/get-shit-done#672). The steps now live only in `references/project-skills-discovery.md` and follow the Agent Skills progressive-disclosure model: each skill's frontmatter first, the full `SKILL.md` only when its `description` fits the task, and referenced files only when the task needs them. GSD's own `gsd-*` skills are skipped, and agents that self-load `agent_skills` skip the project skills configured for their type. (#4649)
