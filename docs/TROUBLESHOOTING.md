# Troubleshooting

## “Not a directory” / file not found

The notebook expects to be run from the repo root and sets paths automatically. If you moved files around and see “Not a directory” or “file not found”, update the path variables near the top of the notebook:

- `dir_pubmed_searches_path` → point to your local `pubmed_searches/` folder
- `dir_path` → point to your local repo root

## Package import errors (e.g., `ModuleNotFoundError: shap`)

Re-run the dependency install step:

- Colab:
  - `!pip -q install uv`
  - `!uv pip install -r requirements.lock` (fallback: `requirements.txt`)
- Local (with the venv activated):
  - `uv pip install -r requirements.lock` (fallback: `requirements.txt`)

## OpenCV issues (`import cv2` fails)

Try reinstalling into a fresh environment:

- `rm -rf .venv`
- `uv venv`
- `source .venv/bin/activate`
- `uv pip install -r requirements.lock` (fallback: `requirements.txt`)

On some platforms, using `conda` may be easier for native dependencies:

- `conda env create -f environment.yml`

Note: `shap` is only needed for the SHAP illustration section (Figure 9C). Figure 7C does not require SHAP.

## Colab: notebook runs but interactive HTML doesn’t display

The `networks/*.html` files are easiest to view by downloading and opening locally in a browser.
See `docs/VIEW_NETWORKS.md`.
