
# Bank Liquidity Risk — DistilBERT Notebook (Reproducible Minimal Repo)

  

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17136508.svg)](https://doi.org/10.5281/zenodo.17136508)

![Python](https://img.shields.io/badge/python-3.10%2B-blue.svg)

![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red.svg)

  

This repository contains a **single notebook** to reproduce our main experiment on bank liquidity risk using **DistilBERT**.

All data are fetched from public sources (see links below). For full archival reproducibility, the dataset and notebook are preserved on **Zenodo** with a DOI.

  

---

  

## Contents

  

- `liquidity-distilbert.ipynb` — end-to-end training, validation calibration, threshold tuning, and test evaluation.

  

---

  

## Data

  

- **Primary replication deposit (with DOI)**

Zenodo: **https://doi.org/10.5281/zenodo.17136508**

  

- **Convenience mirror**

Kaggle: **https://www.kaggle.com/datasets/mjshahchera/bank-marketing-dataset-portuguese-bank-institution/data**

  

> The Zenodo record is recommended for long-term preservation and citation.

> The Kaggle page is convenient for quick access.

  

---

  

## Quick Start

  

### Option A — Google Colab

1. Upload `liquidity-distilbert.ipynb` to Colab.

2. In the first setup cell, install dependencies:

3. Set the DATA_CSV path in the notebook to the downloaded CSV (from Zenodo or Kaggle).

4. Run all cells.
  

> What the Notebook Does

 - Loads & preprocesses the World Bank–derived dataset (binary label: liquidity risk).
- Trains DistilBERT for 50 epochs (default).

> Validates with:

 - Temperature calibration (on validation only)
 - Threshold tuning for macro-F1 (on validation only)
 - Evaluates on test using the calibrated temperature + tuned threshold.
 - Saves a small set of artifacts (metrics table & figures) to a local folder.

> The notebook follows a leak-free protocol: calibration and threshold
> tuning are performed only on the validation set; the test set is
> evaluated once at the end.

## Citing

### Zenodo (Data & Code Deposit)

Shahchera, M. J. (2025). _# Bank Liquidity Risk dataset (Data and Code)_ [Data set & Software]. Zenodo. [https://doi.org/10.5281/zenodo.17136508](https://doi.org/10.5281/zenodo.17136508)

**BibTeX**

    @dataset{shahchera_2025_blr_zenodo,
    author    = {Shahchera, M. J.},
    title     = {Bank Liquidity Risk dataset (Data and code)},
    year      = {2025},  publisher = {Zenodo},
    doi       = {10.5281/zenodo.17136508},
    url       = {https://doi.org/10.5281/zenodo.17136508}}

## License

-   Notebook/code in this repo: **MIT** (or your preferred OSI license)
    
-   Data: see the **Zenodo record** license and original **World Bank** terms.

