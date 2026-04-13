# Start here (non-coders)

Google Colab runs the notebook in a browser (no local Python install needed).

## 1) Open the notebook

- `https://colab.research.google.com/github/madavid128/2026-BoneRep-MLforBoneImaging/blob/main/notebooks/MLforBoneImaging.ipynb`

## 2) Choose your path

- **Read-only**: scroll and read. No setup needed.
- **Rerun figures**: run the setup cell once, then jump to the figure section(s) you care about and run only those cells.
- **Rerun PubMed merge**: run the setup cell, then run the “Merge PubMed searches” section to regenerate the merged table.

If you want to run everything in Colab:

1) Run the first setup code cell.
2) Click **Runtime → Run all**.

## 3) Outputs

- Tables: `data/`
- Interactive networks: `networks/` (open `networks/index.html`)

For review, start with the curated “final” table:

- `data/References.csv`

## 4) Download outputs (optional)

Colab sessions are temporary. To download outputs, run:

```bash
!zip -r outputs.zip data networks
```

```python
from google.colab import files
files.download("outputs.zip")
```

## Help

- `docs/FAQ.md`
- `docs/TROUBLESHOOTING.md`
- `docs/VIEW_NETWORKS.md`

## How to cite

- David, M. A., Williams, K. G., Constantine, E. P., Matthias, J., Ferguson, V. L., & Adams, D. J. (2026). Demystifying Machine Learning Approaches in Digital Bone Imaging using MicroCT and HRpQCT. Bone Reports. DOI: https://doi.org/10.1016/j.bonr.2026.101911. RRID: SCR_028186.
