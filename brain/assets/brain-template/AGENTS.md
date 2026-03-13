# Agent guidance

Quick overview for AI agents (and humans). For detailed steps, follow the linked resources.

## Repository layout

Brief description of each top-level folder:

- **areas/** — Ongoing responsibilities (no fixed "done" date). One folder per area; add whatever fits (work, learning, relationships, etc.). **Each area should have its own README.md and AGENTS.md** so both agents and people know how to operate in that area. See [areas/README.md](areas/README.md).
- **projects/** — Time-bound or outcome-bound work. One folder per project. Link to areas, resources, and zettelkasten as needed.
- **resources/** — Reference material, docs, bookmarks. See [resources/README.md](resources/README.md).
- **scripts/** — Small scripts and automation. See [scripts/README.md](scripts/README.md).
- **zettelkasten/** — Slip-box for atomic, linked notes. Inbox for quick captures; permanent notes in the folder root; organize by linking, not folders. **For Zettelkasten-specific agent guidance** (how to create, link, and structure notes), see **[zettelkasten/AGENTS.md](zettelkasten/AGENTS.md)**.

## Conventions

- **File names:** Use **kebab-case** for new and renamed files (e.g. `my-note.md`, `my-script.py`). Apply when creating files or suggesting renames.

## Procedures

Each procedure has a **name**, then **When** and **What to do** as section headers. **What to do** is an enumerated list (1. 2. 3. …). Follow these at repo root; scope-specific procedures live in each scope’s AGENTS.md.

### Add or change a top-level scope

#### When

You are adding or changing top-level structure (e.g. a new area, project, or resource type) and the repo expects README + AGENTS at that scope.

#### What to do

1. Create or update README.md for humans (what this scope is, how to use it, how it connects).
2. Create or update AGENTS.md for agents: scope, conventions, and procedures (each procedure with a name, When and What to do as section headers, What to do as an enumerated list).
3. If the scope has a template (e.g. template-area, template-project), copy from the template and adapt.
