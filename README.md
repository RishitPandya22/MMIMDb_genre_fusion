# Multimodal Movie Genre Classification (MM-IMDb), Group 17

Multi-label genre classification (23 genres) from movie posters and plot summaries, comparing unimodal baselines, early fusion, late fusion and a Gated Multimodal Unit (GMU).

## Contents

| file | purpose |
|---|---|
| `MMIMDb_initial_analysis.ipynb` | Initial dataset analysis used for the proposal (quality checks, GPU feasibility) |
| `MMIMDb_genre_fusion.ipynb` | Final solution: preprocessing, feature extraction, all models, evaluation, failure cases and bias analysis |
| `requirements.txt` | Python packages |
| `results/` | Tables (CSV) and figures (PNG) produced by the final notebook |

## How to reproduce

1. Open `MMIMDb_genre_fusion.ipynb` in Google Colab (Runtime: T4 GPU) or any Jupyter environment with a GPU.
2. Run all cells. On the first run the notebook downloads the dataset (about 8 GB) from
   https://archive.org/download/mmimdb/mmimdb.tar.gz, extracts it and caches the extracted features
   (`visual_features.pt`, `text_features.pt`). On Colab these are stored in Google Drive under `MyDrive/mmimdb_project`.
3. Feature extraction takes about 20 to 30 minutes on a T4 GPU and is done once. Training and evaluating all models then takes a few minutes.
4. All result tables and figures are written to `results/`.

All randomness is seeded with 0. The dataset is not included in this repository; it is used for non-commercial academic research only.

## Data

MM-IMDb: Arevalo, J., Solorio, T., Montes-y-Gómez, M., & González, F. A. (2017). Gated Multimodal Units for Information Fusion. ICLR Workshop.
