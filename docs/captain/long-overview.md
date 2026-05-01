## What this repo contains

- **Runnable examples**: Jupyter notebooks and Python scripts grouped by topic under `examples/<topic>/` (e.g., `examples/agents_sdk/`). Each example/topic can carry its own minimal `requirements.txt`.
- **Narrative documentation**: Longer-form guides and reference material under `articles/`.
- **Shared media assets**: Diagrams and screenshots in `images/`.

## Publication and metadata workflow

- New or moved content should be registered in **`registry.yaml`** so it appears on **cookbook.openai.com**.
- Contributor attribution is managed through **`authors.yaml`**.

## Development and validation workflow

- Recommended workflow uses a local virtual environment (e.g., `python -m venv .venv`).
- Notebooks are developed with `jupyter lab` / `jupyter notebook`.
- A repository script, **`.github/scripts/check_notebooks.py`**, is used to validate notebook structure before pushing changes.

## Contribution and quality guidelines

- Python style guidance: PEP 8, descriptive names, concise docstrings focused on API usage choices.
- Notebook hygiene: execute top-to-bottom, clear execution counts before committing.
- Secrets handling: API keys must be provided via environment variables (not hard-coded), typically `OPENAI_API_KEY`.
- PR expectations: include summary/motivation/self-review; ensure registry/author metadata stays in sync with content.

## Notable engineering notes captured in repo docs

The guidelines also document several repo-specific pitfalls and mitigations (e.g., virtualenv inheritance issues, import resolution under pytest, and evaluation harness/schema considerations), indicating the repo includes or supports notebook- and test-driven example validation as it evolves.