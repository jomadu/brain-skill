# Linting and formatting. Use `uv sync` first if needed.
# See AGENTS.md and resources/tooling.md for details.

.PHONY: help install lint format lint-python format-python lint-markdown format-markdown pre-commit

MARKDOWN_FILES := $(shell find . -name '*.md' -not -path './.git/*')

help:
	@echo "Lint and format targets (run from repo root):"
	@echo "  make install      - Install dev deps and pre-commit hooks"
	@echo "  make lint         - Run all lint checks (no edits)"
	@echo "  make format       - Run all formatters and fix lint (edits files)"
	@echo "  make lint-python  - Ruff check + format check (Python only)"
	@echo "  make format-python - Ruff fix + format (Python only)"
	@echo "  make lint-markdown - mdformat --check (Markdown only)"
	@echo "  make format-markdown - mdformat (Markdown only)"
	@echo "  make pre-commit   - Run pre-commit on all files"

install:
	uv sync
	uv run pre-commit install

lint: lint-python lint-markdown

lint-python:
	uv run ruff check .
	uv run ruff format --check .

lint-markdown:
	uv run mdformat --check $(MARKDOWN_FILES)

format: format-python format-markdown

format-python:
	uv run ruff check --fix .
	uv run ruff format .

format-markdown:
	uv run mdformat $(MARKDOWN_FILES)

pre-commit:
	uv run pre-commit run --all-files
