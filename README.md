## *Robust Curve Fitting Under Low SNR: A Perfusion-MRI Simulation Study*

### *Why I built this*
Brain perfusion and permeability MRI depend on accurate kinetic-curve fitting.  
Low signal-to-noise ratio and motion degrade parameter stability.  
This project explores whether a compact neural regressor can produce more stable fits than classical least-squares under noisy conditions.

### *What this repository contains*
- Python simulation of perfusion-like time–intensity curves  
- Baseline least-squares curve fitting  
- A small PyTorch regression model for denoising/fitting  
- RMSE vs SNR comparison  
- Example fitted curves (figure included)  
- Fully reproducible Jupyter notebook

### *Key finding*
The neural regressor reduced RMSE by *~60–70%* under high noise compared to classical least-squares fitting.

### *Reproducibility*
- One notebook (01_dl_fit.ipynb) reproduces all experiments  
- Fixed random seed for deterministic results  
- requirements.txt included for environment setup  

### *Why this matters*
This proof-of-concept aligns with current work in robust perfusion and permeability MRI modelling, and demonstrates how data-driven priors can stabilise parameter estimation in low-SNR regimes.
