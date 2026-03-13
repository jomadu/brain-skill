# Projects: Agent guidance

Guidance for agents working under **projects/** (folder-level). Repo-wide rules apply: see [AGENTS.md](../AGENTS.md) for conventions and layout.

## Scope

- **This scope covers:** The projects directory and all project folders. Projects are time-bound or outcome-bound work with a clear end (unlike areas, which are ongoing).
- **Per-project rules:** Each project folder may have its own README.md and optionally AGENTS.md. When present, a project’s AGENTS.md overlays this file and root for work inside that project.

## Conventions

- One folder per project; name folders in kebab-case. When creating a new project, copy from [template-project/](template-project/) and adapt README.md and AGENTS.md.
- Active projects live here; completed work moves to `archive/<project-name>/` (sibling of `projects/` if the repo uses it, or as the repo defines).
- Link to [areas/](../areas/), [resources/](../resources/), and [zettelkasten/](../zettelkasten/) where relevant. Do not duplicate reference or concept content here; link instead.

## Procedures

Each procedure has a **name**, then **When** and **What to do** as section headers. **What to do** is an enumerated list (1. 2. 3. …).

### Create a new project

#### When

The user or context requires a new project (time-bound or outcome-bound work).

#### What to do

1. Copy [template-project/](template-project/) to a new folder under projects/ with a kebab-case name.
2. Adapt the new folder’s README.md (what this project is, goals, how it connects to areas/resources/zettelkasten).
3. Adapt the new folder’s AGENTS.md if present (scope, conventions, procedures with name, When and What to do as section headers, What to do as an enumerated list; how to operate).
4. Link to areas, resources, and zettelkasten as needed; do not duplicate their content here.

### Archive a completed project

#### When

A project is finished and the repo uses an archive (e.g. `archive/<project-name>/`).

#### What to do

1. Move the project folder from projects/ to archive/<project-name>/ (or the path the repo defines).
2. Update any links that pointed at the old location if necessary.
3. Do not leave completed projects in projects/ once the repo expects them in archive.

## How to operate

- **Do:** Create or edit project folders and their README/notes in line with project scope; use links to areas, resources, and zettelkasten for context.
- **Don’t:** Put ongoing responsibilities (areas) or atomic concept notes (zettelkasten) under projects; don’t leave completed projects in the active projects folder when the repo uses an archive.
