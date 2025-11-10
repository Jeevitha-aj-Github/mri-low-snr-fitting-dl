# Deep Learning–Assisted Fitting of Noisy Perfusion-MRI Curves (Exploratory)

Small, self-contained demo to simulate perfusion-like MRI time–intensity curves under low SNR, 
apply simple denoising, and compare classical least-squares fitting with a tiny neural-network regressor.

**Why:** Inspired by the EPSRC DTP project “Improving robustness of brain perfusion and permeability imaging using deep learning.”

## Plan
- Generate synthetic perfusion-like curves at multiple SNR levels  
- Classical fit with SciPy least_squares  
- DL fit with small PyTorch MLP  
- Metrics: parameter RMSE vs SNR  
- Plots: true vs noisy vs fitted  

## Tech
Python (NumPy, SciPy, Matplotlib, PyTorch), Jupyter Notebook  

> Status: repo scaffolded; code coming next.
