# Notes for coders (environment + execution)

This repo is primarily reader-facing (Colab-first), but this page documents the environment and execution choices for developers/coders.

## What is Colab?

**Google Colab** is a hosted Jupyter environment that runs notebooks in a browser. It provides a temporary Linux runtime (CPU/GPU options depending on plan). Because the runtime is ephemeral, the notebook setup typically:

- clones the GitHub repo into `/content/<repo>`
- installs Python dependencies into the current Colab session

The repo’s reader notebook includes a setup cell that automates this:

- `notebooks/MLforBoneImaging.ipynb`

## What is pip?

**pip** is the standard Python package installer. In this repo:

- `requirements.txt` lists the dependencies needed to run the notebook(s)
- a typical local install is `python -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt`

## What is uv?

**uv** is a fast Python package manager that can replace many common `pip` tasks. In this repo, uv is used in two ways:

1) **Create a virtual environment**
   - `uv venv`

2) **Install dependencies**
   - `uv pip install -r requirements.lock` (fallback: `requirements.txt`)

In Colab, install uv using pip, then use uv for the rest:

- `pip install uv`
- `uv pip install -r requirements.lock` (fallback: `requirements.txt`)

## Why both `requirements.txt` and `pyproject.toml`?

- `requirements.txt` is the most universal, and works in Colab and most local setups.
- `pyproject.toml` declares the same dependencies in a standard metadata format (useful for uv tooling and IDEs).

This repository is not intended to be installed as a library/package; the goal is to run the notebooks.

## Reproducibility and locking

This repo includes a pinned lockfile for reproducibility:

- `uv pip install -r requirements.lock`

To refresh the lockfile from `requirements.txt`:

- `uv pip compile requirements.txt -o requirements.lock`

Exact bitwise figure reproduction may still depend on platform, Python version, and random seeds.

## Notebook variants

- `notebooks/MLforBoneImaging.ipynb` is the Colab-first notebook used for this repository.

## Outputs and artifacts

- Derived tables are written into `data/` (e.g., `data/df_pubmed_searches_deduplicated.csv`).
- Interactive network HTML outputs are in `networks/` (entry point: `networks/index.html`).

Some network HTML files reference external CDNs; fully-offline archival would require bundling those assets or regenerating self-contained HTML.

## Consistency checks

After renaming files (especially the notebook), a quick way to verify links is:

- `rg -n "MLforBoneImaging\\.ipynb" README.md docs notebooks`
- `rg -n "MLforBoneImaging\\.ipynb" -S .`
