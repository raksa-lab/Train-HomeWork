# Train-HomeWork: Wide Dense Autoencoder on MNIST

This repository contains the autoencoder implementation trained on MNIST to reconstruct digits degraded by Gaussian noise.

## Overview
- **Architecture**: 784 -> 512 -> 256 (bottleneck) -> 512 -> 784
- **Loss & Metrics**: Mean Squared Error (MSE), Mean Absolute Error (MAE)
- **Evaluation**:
  - Training, Validation, and Test MSE
  - Classification accuracy on reconstructed noisy test digits
  - Confusion matrices and per-digit visual reconstruction comparisons

## Repository Structure
- `mnist_wide_dense_simple.ipynb`: Main Jupyter notebook with data loading, training, evaluation, and plotting.
- `output/`:
  - `results.csv`: Summary results across configurations.
  - `epochs_size*_epochs*.csv`: Per-epoch logs (Train/Val Loss, MSE, MAE, Test MSE, Loss Gap, Epoch Time).
  - `graph_loss_size*_epochs*.png`: Training & validation MSE and MAE curve graphs.
  - `graph_samples_size*_epochs*.png`: Visual comparison of original, noisy test, and reconstructed digits.
  - `graph_confusion_size*_epochs*.png`: Confusion matrix plots.
  - `result_10_digits_size*_epochs*.png`: Digit-by-digit (0-9) reconstructions.
  - `graph_summary_comparison.png`: Overall configuration comparison charts.

## Results Summary

| Size | Epochs | Train Loss | Val Loss | Train MSE | Val MSE | Train MAE | Val MAE | Test MSE | Digit Accuracy |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2500 | 50 | 0.0047 | 0.0088 | 0.0047 | 0.0088 | 0.0214 | 0.0292 | 0.0110 | 87.8% |
| 2500 | 100 | 0.0033 | 0.0094 | 0.0033 | 0.0094 | 0.0193 | 0.0305 | 0.0119 | 88.0% |
| 5000 | 50 | 0.0038 | 0.0063 | 0.0038 | 0.0063 | 0.0198 | 0.0244 | 0.0092 | 90.9% |
| 5000 | 100 | 0.0032 | 0.0068 | 0.0032 | 0.0068 | 0.0193 | 0.0261 | 0.0101 | 91.5% |