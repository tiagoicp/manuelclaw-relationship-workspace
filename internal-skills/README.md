# Internal Skills

This folder contains agent-specific procedural knowledge — skills you've developed, refined, or adapted for your own workflows.

## What goes here

- Skills you've written from scratch for your domain
- Adaptations of external skills that didn't quite fit your needs
- Distilled how-tos from repeated tasks (e.g. "how to structure a weekly review")

Each skill is a single `SKILL.md` file inside a named folder:

```
internal-skills/
  {skill-slug}/
    SKILL.md
```

## How to use

Discover skills by browsing this folder or grepping for keywords. Read the relevant `SKILL.md` and follow it. No state tracking, no usage logs — just the knowledge.

## Versioning

All changes are git-tracked. To see the history of a skill:
```
git log --oneline -- internal-skills/{skill-slug}/SKILL.md
git diff HEAD~1 -- internal-skills/{skill-slug}/SKILL.md
```

## Lifecycle

- **Create** a skill when you find yourself doing the same thing more than twice and want to codify it
- **Improve** a skill when you discover a better approach — edit in place, git captures the history
- **Delete** a skill when it becomes redundant (e.g. Manuel Claw promoted it to the main `skills/` folder and the external version covers it fully)

## Relationship to external skills

External skills (from OpenClaw's main `skills/` folder) take precedence. If an internal skill duplicates an external one, prefer the external. Internal skills are for gaps and domain-specific adaptations.

Manuel Claw reviews internal skills across all agent workspaces and decides if any should be promoted to the shared `skills/` folder. That promotion is his call only — internal agents don't write to the main skills folder.

## Weekly review

Once a week, review this folder as part of your weekly self-improvement cron:
- Are all skills still accurate and useful?
- Is any skill now covered by an external skill? (delete if so)
- Are there repeated workflows you haven't codified yet? (create a new one)
- Could any skill benefit from web research to stay current?
