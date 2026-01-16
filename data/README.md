# Data outputs

This folder contains derived tables used by the notebook and/or included as paper supplements.

Files currently present:

- `References.csv`: the curated “final” reference table used for downstream analysis/figure generation (includes additional annotations like task flags, modality, and model fields).
- `df_pubmed_searches_deduplicated.csv`: merged PubMed search exports (a broader, de-duplicated merge across `pubmed_searches/`) with metadata columns (e.g., `duplicate_count`, `duplicate`, `dataset`). This is the table you would import into SciNetX.
- `PubMedSearchesWords.csv`: lookup table listing the PubMed search terms used (with `Search Description`, `Time`, `GitHub_Filename`, and the `Pubmed Search` string).

## Column overview

`df_pubmed_searches_deduplicated.csv` columns:

- `PMID`, `Title`, `Authors`, `Citation`, `First Author`, `Journal/Book`, `Publication Year`, `Create Date`, `PMCID`, `NIHMS ID`, `DOI`, `dataset`, `duplicate_count`, `duplicate`

`References.csv` columns:

- `PMID`, `Title`, `Authors`, `Citation`, `First Author`, `Journal/Book`, `Publication Year`, `Create Date`, `DOI`, `Prediction`, `Segmentation`, `Radiomics Constrast/Texture`, `Classification`, `Super Resolution`, `Clustering`, `Data Reduction`, `Data Integration`, `ML_Task`, `Modality`, `Species`, `In Vivo or Ex Vivo`, `Model`, `Accuracy`

`PubMedSearchesWords.csv` columns:

- `Search Description`, `Time`, `GitHub_Filename`, `Pubmed Search`

## Provenance

The notebook reads inputs from `pubmed_searches/` and writes derived tables into this folder.
