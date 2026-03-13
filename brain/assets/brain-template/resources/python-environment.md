# Python environment (UV)

This repo uses [UV](https://docs.astral.sh/uv/) as the package manager, with dependencies declared in `pyproject.toml`.

## Requirements

- **UV** and **Python** must be installed and on your PATH. The project targets Python 3.10+ (see `requires-python` in `pyproject.toml`); UV will use the appropriate interpreter when creating the venv.
- Install UV: `curl -LsSf https://astral.sh/uv/install.sh | sh` (or see [install docs](https://docs.astral.sh/uv/getting-started/installation/)). After installing, ensure your shell picks it up (e.g. re-source `~/.zshrc` or open a new terminal).
- Verify: `which uv` and `which python3` (or `python`) should both succeed.

## One-time setup

From the repo root, create a virtual environment and install dependencies:

```bash
uv venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate
uv sync
```

Or without activating: `uv sync` will create `.venv` and install into it; then use `uv run python scripts/your_script.py` to run scripts.

## Adding or changing dependencies

Edit `pyproject.toml`: runtime deps under `[project].dependencies`, dev/tooling deps under `[dependency-groups].dev`. Then run `uv sync`.

## Running Python

Prefer the project venv (activate it, or use `uv run python ...`) so that dependencies in `pyproject.toml` are available.
