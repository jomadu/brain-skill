# Scripts: Agent guidance

Guidance for agents working under **scripts/**. Repo-wide rules apply: see [AGENTS.md](../AGENTS.md) for conventions and layout.

## Scope

- **This scope covers:** Small scripts and automation run from the command line or called by other tools.
- **Out of scope:** Reference documentation lives in [resources/](../resources/); time-bound work in [projects/](../projects/); atomic notes in [zettelkasten/](../zettelkasten/).

## Conventions

- Use kebab-case for script file names (e.g. `my-script.py`, `fetch-data.sh`). Run scripts with the appropriate interpreter or runtime for the repo.
- Document usage in script docstrings or [scripts/README.md](README.md) when helpful.

## Do / don't

- **Do:** Add or edit scripts that fit the repo's automation needs; document how to run them.
- **Don't:** Put reference docs or project notes here (use resources/ and projects/).
