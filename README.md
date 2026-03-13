# brain-skill

An **[Agent Skill](https://agentskills.io/home)** (following the [Agent Skills spec](https://agentskills.io/home)) plus a **template** for “brain-style” repositories: a personal knowledge base with **areas** (ongoing responsibilities), **projects** (time-bound work), **resources** (reference), and a **Zettelkasten** (atomic, linked notes).

## What you get

- **Skill** (`brain/SKILL.md`) — Tells skills-compatible agents how to work in brain-style repos: README for humans, AGENTS.md for agents, and an overlay of AGENTS.md from root down to the current path. Use it when managing structure, creating/linking zettels, or initializing from the template.
- **Template** (`brain/assets/brain-template/`) — Copy into any repo to stand up the full layout (root README + AGENTS, areas/, projects/, resources/, scripts/, zettelkasten/ with inbox and template zettel). Your agent can “pull the template” or initialize an uninitialized directory.

## Quick start

1. **Use the skill** — Add the brain skill to your agent's skills path (e.g. Cursor's `.cursor/skills/`) so agents load it when working in brain-style repos.
2. **Use the template** — Copy the contents of `brain/assets/brain-template/` into a repo root (or ask your agent to initialize from the template). Customize areas, projects, and zettelkasten from the new root README.

## Repo layout

| Path | Purpose |
|------|--------|
| `brain/SKILL.md` | Skill definition and contract (README vs AGENTS, overlay, procedures). |
| `brain/assets/brain-template/` | Full template to initialize a brain repo. |
| `docs/release-notes.md` | Where release notes live and how releases are produced. |

## Development

- **Commits** — Conventional commits (validated by commitlint; husky `commit-msg` hook). See [docs/release-notes.md](docs/release-notes.md).
- **Releases** — Semantic-release on push to `main`, `rc`, `alpha`, or `beta`. The `brain` folder is published as a release asset. Run `npm run semantic-release` for a dry-run.

License: GPL-3.0 (see [brain/SKILL.md](brain/SKILL.md)).
