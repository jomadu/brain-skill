# Scripts: Agent guidance

Guidance for agents working under **scripts/**. Repo-wide rules apply: see [AGENTS.md](../AGENTS.md) for conventions, tooling, and layout.

## Scope

- **This scope covers:** Small scripts and automation run from the command line or called by other tools. Scripts use the project venv and dependencies in `pyproject.toml`.
- **Out of scope:** Reference documentation lives in [resources/](../resources/); time-bound work in [projects/](../projects/); atomic notes in [zettelkasten/](../zettelkasten/).

## Conventions

- Use kebab-case for script file names (e.g. `my-script.py`). Run via the project venv: `uv run python scripts/your_script.py` (or as documented in [resources/python-environment.md](../resources/python-environment.md)).
- Follow repo Python and formatting rules (Ruff, pre-commit); see root [AGENTS.md](../AGENTS.md) and [resources/tooling.md](../resources/tooling.md).

## Do / don’t

- **Do:** Add or edit scripts that fit the repo’s automation needs; use `uv run` so dependencies are consistent; document usage in script docstrings or [scripts/README.md](README.md) when helpful.
- **Don’t:** Install or rely on system Python or global packages for these scripts; don’t put reference docs or project notes here (use resources/ and projects/).
