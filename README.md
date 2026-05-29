# superpowersexy

A Claude Code plugin-mode skills library for coding-agent workflows.

This project follows the Claude-only structure used by [`obra/superpowers`](https://github.com/obra/superpowers): plugin metadata lives in `.claude-plugin/`, and skills live in `skills/`.

## Included skills

- `clarifying-requirements` — turn vague requests into precise, actionable requirements before design or implementation.
- `writing-architecture` — create architecture design documents from requirements, plans, or codebase analysis.

## Structure

```text
superpowersexy/
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
├── skills/
│   ├── clarifying-requirements/
│   │   ├── SKILL.md
│   │   └── requirements-document-reviewer-prompt.md
│   └── writing-architecture/
│       └── SKILL.md
└── README.md
```

## Local development install

From Claude Code, add this repository as a plugin marketplace and install the plugin:

```text
/plugin marketplace add git@github.com:BestNathan/superpowersexy.git
/plugin install superpowersexy@superpowersexy-dev
```

## Adding skills

Add each Claude Code skill as a directory under `skills/` with a `SKILL.md` file that contains YAML frontmatter:

```markdown
---
name: skill-name
description: When Claude should use this skill.
---

# Skill Name

Skill instructions go here.
```
