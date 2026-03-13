# Scripts: Agent guidance

Guidance for agents working under **scripts/**. Repo-wide rules apply: see [AGENTS.md](../AGENTS.md) for conventions and layout.

## Scope

- **This scope covers:** Small scripts and automation run from the command line or called by other tools.
- **Out of scope:** Reference documentation lives in [resources/](../resources/); time-bound work in [projects/](../projects/); atomic notes in [zettelkasten/](../zettelkasten/).

## Conventions

- Use kebab-case for script file names (e.g. `my-script.py`, `fetch-data.sh`). Run scripts with the appropriate interpreter or runtime for the repo.
- Document usage in script docstrings or [scripts/README.md](README.md) when helpful.

## Procedures

Each procedure has a **name**, then **When** and **What to do** as section headers. **What to do** is an enumerated list (1. 2. 3. …).

### Add or change a script

#### When

Adding or changing a script or automation that runs from the command line or is called by other tools.

#### What to do

1. Create or edit the script under scripts/ with a kebab-case file name.
2. Use the repo’s expected interpreter or runtime.
3. Document how to run it (in the script’s docstring and/or [scripts/README.md](README.md)).
4. Do not put reference docs or project notes here (use resources/ and projects/).

## How to operate

- **Do:** Add or edit scripts that fit the repo's automation needs; document how to run them.
- **Don't:** Put reference docs or project notes here (use resources/ and projects/).
