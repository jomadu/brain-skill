# Brain skill assets

## brain-template/

A full brain-structure template for initializing an uninitialized directory or repository.

**When to use:** The user asks to "initialize as a brain", "pull the brain template", or set up a repo with areas, projects, resources, zettelkasten, and agent guidance.

**What to copy:** Everything inside `brain-template/` (not the folder itself) into the target root, so that the target gets:

- **Root:** AGENTS.md, README.md, Makefile, pyproject.toml, .pre-commit-config.yaml, .gitignore
- **areas/:** README.md, AGENTS.md, example-area/ (README.md, AGENTS.md)
- **projects/:** README.md, AGENTS.md, example-project/ (README.md, AGENTS.md)
- **resources/:** README.md, AGENTS.md, python-environment.md, tooling.md
- **scripts/:** README.md, AGENTS.md
- **zettelkasten/:** README.md, AGENTS.md, Zettelkasten.md (method for humans and agents), \_template.md, inbox/ (empty, for quick captures)

**After copying:** Direct the user to the new root README.md (quick start: optionally rename in pyproject.toml, run `make install`, then customize areas, projects, and zettelkasten).

See the main [SKILL.md](../SKILL.md) section "Initializing from template" for the full procedure.
