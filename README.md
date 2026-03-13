# brain-skill

An **[Agent Skill](https://agentskills.io/home)** (following the [Agent Skills spec](https://agentskills.io/home)) plus a **template** for “brain-style” repositories: a personal knowledge base with **areas** (ongoing responsibilities), **projects** (time-bound work), **resources** (reference), and a **Zettelkasten** (atomic, linked notes).

## Structure and components

A brain-style repo splits guidance by audience and layers it by path.

**README vs AGENTS.md** — Every scope (root, areas, projects, etc.) can have a **README.md** for humans (what this is, how to use it, how it connects) and an **AGENTS.md** for agents (scope, conventions, procedures, how to operate). Content stays split: human-facing in README, agent-facing in AGENTS.md.

**Overlay** — When working at a path, agents apply **all** AGENTS.md files from the repo root down to that path. Root is the base; each level adds or refines. More specific (closer to the path) overrides the more general.

**Procedures** — In AGENTS.md, procedures are first-class: each has a **name**, a **When** (when to use it), and **What to do** (an enumerated list of steps). Agents follow these instead of inventing ad-hoc workflows. Procedures are defined at the right scope (e.g. "Create a permanent note" in zettelkasten/AGENTS.md, "Add or change a top-level scope" in root AGENTS.md).

**Top-level scopes** (what the template creates):

| Scope | Purpose |
|-------|--------|
| **areas/** | Ongoing responsibilities with no fixed "done" date. One folder per area (e.g. work, learning, health). Each area has its own README and AGENTS.md. |
| **projects/** | Time-bound or outcome-bound work. One folder per project; completed work moves to `archive/<name>/`. Link to areas, resources, and zettelkasten. |
| **resources/** | Reference material: docs, bookmarks, templates. Things you refer to but don't necessarily atomize into notes. |
| **zettelkasten/** | Slip-box for atomic, linked notes. **inbox/** for quick captures; permanent notes in the folder root with **date+slug** filenames (`YYYY-MM-DD-slug.md`). Organize by linking, not folders. Includes a note template and method doc. |
| **scripts/** | Small scripts and automation; documented for both humans and agents. |

The skill teaches agents this structure, the overlay, and the procedures; the template provides the folders, READMEs, AGENTS.md files, and templates (e.g. template-area, template-project, template-zettel) so you can copy and adapt.

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
