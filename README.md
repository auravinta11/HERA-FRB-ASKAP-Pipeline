# Dual-representation CNNs for classifying simulated fast radio bursts

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/auravinta11/HERA-FRB-CNN-Classification-Pipeline/blob/main/HERA_FRB_CNN_Classification.ipynb)

Code for the paper "Evaluating dual-representation CNNs for classifying simulated fast radio bursts". The notebook injects simulated FRBs into HERA background data, converts them to frequency-time and DM-time images, and compares three CNNs (FT, DM, Dual) with baseline classifiers on a development test set and a separate final holdout set.

## Data availability
Raw data are not included. Download the HERA background data from Mesarcik et al. (2022), "Learning to detect RFI in radio astronomy without seeing it", Zenodo, https://doi.org/10.5281/zenodo.6724065, and place `HERA_04-03-2022_all.pkl` in Google Drive (or edit `PKL_PATH` in the notebook).

## Installation
pip install -r requirements.txt

## Usage
Open `HERA_FRB_CNN_Classification.ipynb` in Google Colab (or Jupyter), mount your Drive, and run all cells. Outputs are saved to `results/`. Results can vary between runs because GPU training is not fully deterministic; the saved outputs in the notebook are the run reported in the paper.

## Key features
- Background arrays split before injection (leakage audit included)
- Robust z-score normalisation; training-set DM-time statistics reused for validation, test and holdout
- Three CNNs, ten baseline models, three random seeds
- Independent final holdout set and hard-negative stress test

## Figures
See the `figures/` folder for the ROC, precision-recall, confusion-matrix and detection-efficiency plots from the final holdout evaluation.

## Citation
DOI: (add after Zenodo release)

## License
MIT
