# 2026-BoneRep-MLforBoneImaging

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/madavid-research/2026-BoneRep-MLforBoneImaging/blob/main/notebooks/MLforBoneImaging.ipynb)
[![RRID](https://img.shields.io/badge/RRID-SCR__028186-2ea44f)](https://scicrunch.org/resolver/SCR_028186)
[![Paper DOI](https://img.shields.io/badge/Paper%20DOI-10.1016%2Fj.bonr.2026.101911-blue)](https://doi.org/10.1016/j.bonr.2026.101911)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange)](https://github.com/madavid-research/2026-BoneRep-MLforBoneImaging/releases/tag/v1.0.0)
[![Status](https://img.shields.io/badge/Status-Published-brightgreen)](https://doi.org/10.1016/j.bonr.2026.101911)
[![Paper Repo](https://img.shields.io/badge/Paper%20Repo-GitHub-black)](https://github.com/madavid-research/2026-BoneRep-MLforBoneImaging)

Repository accompanying the paper. The analysis in `notebooks/MLforBoneImaging.ipynb` generates the results/figures and derived artifacts (CSV outputs and interactive HTML networks).

## Associated paper

- Citation: David, M. A., Williams, K. G., Constantine, E. P., Matthias, J., Ferguson, V. L., & Adams, D. J. (2026). *Demystifying Machine Learning Approaches in Digital Bone Imaging using MicroCT and HRpQCT*. *Bone Reports*.
- DOI: https://doi.org/10.1016/j.bonr.2026.101911
- RRID: SCR_028186

## Start here

- Open the notebook in Colab: `https://colab.research.google.com/github/madavid-research/2026-BoneRep-MLforBoneImaging/blob/main/notebooks/MLforBoneImaging.ipynb`
- Non-coder guide: `docs/START_HERE.md`
- FAQ: `docs/FAQ.md`
- Curated “final” reference table: `data/References.csv`
- Figure navigation: `docs/FIGURE_MAP.md`
- View interactive networks: `docs/VIEW_NETWORKS.md` (start with `networks/index.html`)
- Optional (advanced): local runs and environment details in `docs/FOR_CODERS.md`

## Stable Colab link (for papers)

The link above always points to the latest `main` branch.

For a stable link that never changes, use a GitHub **release tag** or **commit SHA** in the URL, for example:

- `https://colab.research.google.com/github/madavid-research/2026-BoneRep-MLforBoneImaging/blob/<TAG_OR_COMMIT>/notebooks/MLforBoneImaging.ipynb`

## Jump to figures (in the notebook)

- Figure 7C: Prediction — [notebooks/MLforBoneImaging.ipynb](notebooks/MLforBoneImaging.ipynb)
- Figure 7D: Classification — [notebooks/MLforBoneImaging.ipynb](notebooks/MLforBoneImaging.ipynb)
- Figure 8: Dimensionality reduction & clustering — [notebooks/MLforBoneImaging.ipynb](notebooks/MLforBoneImaging.ipynb)
- Figure 9B/9C/9D: Grad-CAM / SHAP / radar plots — [notebooks/MLforBoneImaging.ipynb](notebooks/MLforBoneImaging.ipynb)

See [docs/FIGURE_MAP.md](docs/FIGURE_MAP.md) for the exact section headings.

## Key outputs

- [data/References.csv](data/References.csv): curated “final” reference table used for downstream analysis/figures
- [data/df_pubmed_searches_deduplicated.csv](data/df_pubmed_searches_deduplicated.csv): merged PubMed exports (output of the merge section; can be imported into SciNetX)
- [data/PubMedSearchesWords.csv](data/PubMedSearchesWords.csv): lookup table listing the PubMed search terms used

## What’s in here

- `notebooks/` – Jupyter notebook (`notebooks/MLforBoneImaging.ipynb`)
- `pubmed_searches/` – exported PubMed search CSVs (inputs)
- `data/` – derived tables (outputs)
- `networks/` – interactive HTML network visualizations (outputs)
- `images/` – static images used in the notebook/paper

More docs:
- `docs/GLOSSARY.md`
- `docs/TROUBLESHOOTING.md`

## Viewing interactive networks

Interactive HTML network visualizations are in `networks/`. Start with `networks/index.html`, and for viewing tips (including Colab), see `docs/VIEW_NETWORKS.md`.

If you only want to view the networks (no coding):

1) On GitHub, click **Code → Download ZIP**
2) Unzip the download
3) Open `networks/index.html` in a browser

## Citation and license

- Cite via `CITATION.cff`.
- License terms are in `LICENSE`.

If you need a plain-text citation for the paper, use:

- David, M. A., Williams, K. G., Constantine, E. P., Matthias, J., Ferguson, V. L., & Adams, D. J. (2026). Demystifying Machine Learning Approaches in Digital Bone Imaging using MicroCT and HRpQCT. Bone Reports. DOI: https://doi.org/10.1016/j.bonr.2026.101911. RRID: SCR_028186.

If you need a plain-text repository citation, use:

- David MA, Williams KG, Constantine EP, Matthias J, Ferguson VL, Adams DJ. *2026-BoneRep-MLforBoneImaging* (software). GitHub: `https://github.com/madavid-research/2026-BoneRep-MLforBoneImaging`.

## Software used

This work utilized the SciNetX software to generate the network visualizations used in this repository and the paper. If you are interested in the SciNetX software itself, see `https://github.com/madavid-research/SciNetX` for source code and license terms.
