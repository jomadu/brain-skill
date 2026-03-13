# Formatting and pre-commit

The repo uses automated formatting and linting, with **pre-commit** so checks run before each commit.

## What runs

- **Markdown:** [mdformat](https://github.com/executablebooks/mdformat) formats `.md` files (line endings, spacing, list style). Config: `[tool.mdformat]` in `pyproject.toml`.
- **Python:** [Ruff](https://docs.astral.sh/ruff/) runs lint (`ruff check`) and format (`ruff format`). Config: `[tool.ruff]` in `pyproject.toml`.

## One-time setup

1. Install dev dependencies and pre-commit hooks:
   ```bash
   uv sync
   pre-commit install
   ```
1. (Optional) Run on all files once: `pre-commit run --all-files`.

After that, pre-commit runs automatically on `git commit`. If a hook changes files, the commit is aborted; stage the changes and commit again.

## Manual runs

- Format/lint everything: `pre-commit run --all-files`
- Only Markdown: `pre-commit run mdformat --all-files`
- Only Python: `pre-commit run ruff --all-files` and `pre-commit run ruff-format --all-files`

## Adding or changing config

- **Markdown:** Edit `[tool.mdformat]` in `pyproject.toml` (e.g. `wrap`, `number`, `end_of_line`). See [mdformat configuration](https://mdformat.readthedocs.io/en/stable/users/configuration_file.html).
- **Python:** Edit `[tool.ruff]` and `[tool.ruff.lint]` in `pyproject.toml`. See [Ruff configuration](https://docs.astral.sh/ruff/configuration/).
- **Hooks:** Edit `.pre-commit-config.yaml` at the repo root, then run `pre-commit autoupdate` to refresh hook revisions if desired.
