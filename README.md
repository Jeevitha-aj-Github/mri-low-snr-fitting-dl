# Exploring Deep Learning–Based Robust Fitting for Noisy Perfusion MRI Signal Modelling

A small, self-contained demo simulating perfusion-like MRI time–intensity curves under low signal-to-noise ratio (SNR).
It compares classical least-squares fitting with a deep-learning-assisted regressor for improved robustness.

Goal

##Clinical Relevance — From Eye to Brain
In my current role within ophthalmic imaging, I routinely capture retinal and microvascular scans where signal quality and patient motion heavily influence diagnostic accuracy.  
This hands-on experience with optical and vascular imaging inspired me to explore parallel challenges in brain perfusion MRI, where maintaining quantitative reliability under low signal-to-noise ratios is equally critical.  
Both domains share a common goal extracting stable, physiologically meaningful information from complex biological signals making this project a natural extension of my current clinical and research interests.


Approach

Generate synthetic perfusion-like time–intensity curves

Apply Gaussian noise to simulate low SNR

Fit with classical SciPy least-squares

Fit with a small PyTorch neural network (MLP)

Compare RMSE and visualize robustness

Results
Under simulated low-SNR conditions (≈15 dB), classical least-squares fitting produced unstable parameter recovery with visibly distorted curves.  
The deep-learning model achieved smoother fits and reduced RMSE (~0.016 vs ~0.048), showing greater stability to noise.  
This behaviour reflects how data-driven priors can implicitly regularise inverse modelling problems similar to Bayesian or variational approaches in quantitative MRI analysis.  
The findings suggest that compact neural regressors could enhance parameter-map robustness in perfusion and permeability imaging, especially when acquisition speed or patient motion limits signal quality.

DL-assisted model reduces RMSE by ~60–70% under high noise.

Tech Stack

Python (NumPy, SciPy, Matplotlib, PyTorch)

Jupyter Notebook

How to Run
pip install -r requirements.txt
jupyter notebook


Then open 00_classical_baseline.ipynb and 01_dl_fit.ipynb in sequence.

Author

Jeevitha Abeth Nego
MSc Biomedical Engineering, University of Bristol

Inspiration

Inspired by EPSRC DTP theme

“Improving robustness of brain perfusion and permeability imaging using deep learning.”
