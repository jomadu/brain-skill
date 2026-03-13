# Agent guidance

Quick overview for AI agents (and humans). For detailed steps, follow the linked resources.

## Repository layout

Brief description of each top-level folder:

- **areas/** — Ongoing responsibilities (no fixed "done" date). One folder per area; add whatever fits (work, learning, relationships, etc.). **Each area should have its own README.md and AGENTS.md** so both agents and people know how to operate in that area. See [areas/README.md](areas/README.md).
- **projects/** — Time-bound or outcome-bound work. One folder per project. Link to areas, resources, and zettelkasten as needed.
- **resources/** — Reference material, tooling docs. Python environment, formatting/pre-commit, etc. See [resources/README.md](resources/README.md).
- **scripts/** — Small scripts and automation. See [scripts/README.md](scripts/README.md).
- **zettelkasten/** — Slip-box for atomic, linked notes. Inbox for quick captures; permanent notes in the folder root; organize by linking, not folders. **For Zettelkasten-specific agent guidance** (how to create, link, and structure notes), see **[zettelkasten/AGENTS.md](zettelkasten/AGENTS.md)**.

## Conventions

- **File names:** Use **kebab-case** for new and renamed files (e.g. `my-note.md`, `my-script.py`). Apply when creating files or suggesting renames.

## Python environment

**Requirements:** UV and Python must be installed and on PATH (Python 3.10+). The repo uses UV and a virtual environment; dependencies are in `pyproject.toml`. When running or modifying Python (e.g. scripts), ensure the venv is set up and used. Full setup and commands: **[resources/python-environment.md](resources/python-environment.md)**.

## Formatting and pre-commit

Markdown (mdformat) and Python (Ruff) are formatted and linted automatically; pre-commit runs these checks before each commit. Setup and config: **[resources/tooling.md](resources/tooling.md)**.

**Standard operations (Makefile):** From the repo root, run `make help` to list targets. Common tasks:

- **`make install`** — Install dev dependencies and pre-commit hooks (`uv sync` + `pre-commit install`).
- **`make lint`** — Run all lint checks only (Ruff check + format check, mdformat check); no file edits.
- **`make format`** — Run all formatters and fix lint (Ruff fix + format, mdformat); edits files.
- **`make lint-python`** / **`make format-python`** — Python only (Ruff).
- **`make lint-markdown`** / **`make format-markdown`** — Markdown only (mdformat).
- **`make pre-commit`** — Run pre-commit on all files (`pre-commit run --all-files`).
