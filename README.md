# Dual-representation CNNs for classifying simulated fast radio bursts

Code for the paper "Evaluating dual-representation CNNs for classifying simulated fast radio bursts". The notebook injects simulated FRBs into HERA background data, converts them to frequency-time and DM-time images, and compares three CNNs (FT, DM, Dual) with baseline classifiers on a development test set and a separate final holdout set.

## Data availability
Raw data are not included. Download the HERA background data from Mesarcik et al. (2022), "Learning to detect RFI in radio astronomy without seeing it", Zenodo, https://doi.org/10.5281/zenodo.6724065, and place `HERA_04-03-2022_all.pkl` in Google Drive (or edit `PKL_PATH` in the notebook).

## Installation
pip install -r requirements.txt

## Usage
Open `FRB_Dual_Representation_CNN_Pipeline.ipynb` in Google Colab (or Jupyter), mount your Drive, and run all cells. Outputs are saved to `results/`.

## Key features
- Background arrays split before injection (leakage audit included)
- Robust z-score normalisation; training-set DM-time statistics reused for validation, test and holdout
- Three CNNs, ten baseline models (four algorithms), three random seeds
- Independent final holdout set and hard-negative stress test

## Citation
DOI: (add after Zenodo release)

## License
MIT
