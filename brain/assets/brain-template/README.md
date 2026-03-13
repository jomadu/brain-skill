# Brain template

A reusable template for a personal knowledge base: **areas** (ongoing responsibilities), **projects** (time-bound work), **resources** (reference and tooling), and a **Zettelkasten** (atomic, linked notes). Includes UV/Python tooling and pre-commit formatting (Ruff + mdformat).

Use this template to stand up the same structure in a new repository. You can version and update the template independently (e.g. in a repo named `brain-template`) and re-use it whenever you want a fresh brain.

## Layout

| Folder | Purpose |
|--------|---------|
| **areas/** | Ongoing responsibilities. No fixed "done" date; add your own area folders. |
| **projects/** | Time-bound work. One folder per project; move completed work to `archive/<name>/`. |
| **resources/** | Reference docs, tooling (Python/UV, pre-commit). |
| **zettelkasten/** | Slip-box: inbox, permanent notes, template, and agent guidance. |
| **scripts/** | Scripts and automation; see [scripts/README.md](scripts/README.md). |

See [AGENTS.md](AGENTS.md) for agent and human guidance (conventions, Makefile).

## Quick start

1. **Copy this directory** into a new repo (e.g. clone or copy the contents of `brain-template` so they become the root of the new repo).
1. **Rename the project** (optional): edit `pyproject.toml` and change `name = "brain-template"` to something like `name = "brain"` or your repo name.
1. **Install and hook**:
   ```bash
   make install
   ```
   This runs `uv sync` and `pre-commit install`. Requires [UV](https://docs.astral.sh/uv/) and Python 3.10+.
1. **Customize**:
   - Add your areas under `areas/` (one folder per area). Each area should have its own **README.md** and **AGENTS.md**—see [areas/README.md](areas/README.md) and copy from `areas/example-area/`.
   - Replace `projects/example-project/` with real projects.
   - Add permanent notes in `zettelkasten/` and use `zettelkasten/inbox/` for quick captures.
   - Add reference material under `resources/` and any scripts under `scripts/` as needed.

## Versioning this template

- Keep the template in its own repo (e.g. `brain-template`). Tag or release when you want a stable snapshot.
- To update an existing brain from the template: diff or cherry-pick changes from the template repo, or re-copy only the files you want to refresh (e.g. `AGENTS.md`, `Makefile`, `resources/`, `scripts/`) and leave your content (areas, projects, zettelkasten notes) in place.
