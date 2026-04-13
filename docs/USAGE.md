# How to use this repository

This repository is intended to be used by opening and running the notebook:

- `notebooks/MLforBoneImaging.ipynb`

## Option A: Run in Google Colab

One-click link:

- `https://colab.research.google.com/github/madavid-research/2026-BoneRep-MLforBoneImaging/blob/main/notebooks/MLforBoneImaging.ipynb`

In Colab:

1) Run the first setup code cell.
2) Click **Runtime → Run all** (or scroll to a specific figure section and run only that section).

If the setup cell fails, see `docs/TROUBLESHOOTING.md` or `docs/FOR_CODERS.md`.

### Optional: keep outputs after Colab resets

Colab runtimes are temporary. To keep generated outputs:

```python
from google.colab import drive
drive.mount("/content/drive")
```

Then copy results you care about into Drive, for example:

```bash
!cp -r data networks "/content/drive/MyDrive/"
```

## Option B: Run locally

1) Install Python 3.10+ and Git.
2) Clone the repo (GitHub → Code → HTTPS URL):
   - `git clone https://github.com/madavid-research/2026-BoneRep-MLforBoneImaging.git`
   - `cd 2026-BoneRep-MLforBoneImaging`
   - (Alternative) Download the repository ZIP from GitHub and unzip it, then `cd` into the folder.
3) Create an environment and install dependencies (recommended: `uv`):
   - `python -m pip install uv`
   - `uv venv`
   - `source .venv/bin/activate`
   - `uv pip install -r requirements.lock` (fallback: `requirements.txt`)
4) Start Jupyter:
   - `jupyter lab`
5) Open `notebooks/MLforBoneImaging.ipynb` and run cells.

## Exact-reproduction note

The notebook was used to generate figures for the paper. If you need the closest possible match:

- use the same OS/Python/package versions used by the authors
- prefer installing from the pinned `requirements.lock`
