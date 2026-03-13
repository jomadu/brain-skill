# Brain template

A reusable template for a personal knowledge base: **areas** (ongoing responsibilities), **projects** (time-bound work), **resources** (reference), and a **Zettelkasten** (atomic, linked notes).

Use this template to stand up the same structure in a new repository. You can version and update the template independently (e.g. in a repo named `brain-template`) and re-use it whenever you want a fresh brain.

## Use your agent as the primary way to work with this brain

**Prefer working through your AI agent** (e.g. in your editor or chat) rather than editing files by hand. The agent is loaded with this repo’s guidance: it knows the procedures in each folder’s **AGENTS.md**, how to apply the README/AGENTS overlay from root down to the path you’re in, how to create and link zettels (date+slug, atomicity, link context), and how to keep areas, projects, and resources consistent. Ask the agent to add notes, create or move projects, process the inbox, refactor structure, or run checks—it will follow the right conventions and manage the data for you.

## Layout

| Folder | Purpose |
|--------|---------|
| **areas/** | Ongoing responsibilities. No fixed "done" date; add your own area folders. |
| **projects/** | Time-bound work. One folder per project; move completed work to `archive/<name>/`. |
| **resources/** | Reference docs and bookmarks. |
| **zettelkasten/** | Slip-box: inbox, permanent notes, template, and agent guidance. |
| **scripts/** | Scripts and automation; see [scripts/README.md](scripts/README.md). |

See [AGENTS.md](AGENTS.md) for agent and human guidance (conventions).

## Quick start

1. **Copy this directory** into a new repo (e.g. clone or copy the contents of `brain-template` so they become the root of the new repo).
1. **Customize** (or ask your agent to do it): Add areas from `areas/template-area/`, projects from `projects/template-project/`, permanent notes in `zettelkasten/` (date+slug), and quick captures in `zettelkasten/inbox/`. See [areas/README.md](areas/README.md), [projects/](projects/), and [zettelkasten/](zettelkasten/) for details. Your agent knows the procedures and can create or update structure for you.

## Versioning this template

- Keep the template in its own repo (e.g. `brain-template`). Tag or release when you want a stable snapshot.
- To update an existing brain from the template: diff or cherry-pick changes from the template repo, or re-copy only the files you want to refresh (e.g. `AGENTS.md`, `resources/`, `scripts/`) and leave your content (areas, projects, zettelkasten notes) in place.
