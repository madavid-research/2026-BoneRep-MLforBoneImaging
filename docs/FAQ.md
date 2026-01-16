# FAQ (for non-coders)

## Do I need to install Python?

No, not if you use Google Colab. Colab runs the notebook in your browser.

Start here:

- `docs/START_HERE.md`
- One-click Colab: `https://colab.research.google.com/github/madavid128/2026-BoneRep-MLforBoneImaging/blob/main/notebooks/MLforBoneImaging.ipynb`

## What should I click in Colab?

- If you are reading only: you can just scroll and read (no setup needed).
- If you want to rerun figures or regenerate outputs: run the first setup cell (it installs what’s needed), then run the section(s) you care about (or click **Runtime → Run all**).

## Where are the outputs?

- Tables: `data/`
- Interactive networks: `networks/` (open `networks/index.html`)

## Which table should I review first?

- `data/References.csv` is the curated “final” reference table.
- `data/df_pubmed_searches_deduplicated.csv` is the broader merged PubMed-export table used to build the merged literature set.

## I only want to view the interactive networks (no notebook)

1) On GitHub, click **Code → Download ZIP**
2) Unzip the download
3) Open `networks/index.html` in a browser

## A network page is blank

Some `networks/*.html` files may require an internet connection (they reference CDN assets). See `docs/VIEW_NETWORKS.md`.

## I get “file not found”

If you moved files or renamed folders, update the path variables near the top of the notebook. See `docs/TROUBLESHOOTING.md`.
