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

## Literature Context
This independent project aligns with ongoing efforts in the University of Manchester neuroimaging group to improve the stability and reproducibility of quantitative MRI analysis.  
It draws conceptual inspiration from recent work by the supervisory team and collaborators, including:

- **Ohene et al. (2025, npj Imaging):** detection of blood–brain barrier alterations in low-SNR MRI data from Alzheimer’s and infection models.  
- **Dickie et al. (2024, Magnetic Resonance in Medicine):** open-source consensus guidelines for contrast-agent–based perfusion MRI, promoting reproducible parameter fitting.  
- **Harris et al. (2023, European Journal of Nuclear Medicine and Molecular Imaging):** in vivo approaches for assessing blood–brain barrier function and dysfunction.  
- **Jia et al. (2025, IEEE Transactions on Medical Imaging):** development of deep-learning frameworks for image registration using decoder-only architectures.  
- **Ghodrati et al. (2025, Medical Image Analysis):** acceleration of cardiac MRI reconstruction using compressed sensing and neural priors.  

Together, these studies illustrate a shared goal: integrating data-driven methods and quantitative modelling to enhance physiological imaging.  
This exploratory work contributes to that direction by testing deep-learning–based fitting for noisy perfusion-like signals.


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

---

##Author & Context
**Created by:** Jeevitha Abeth Nego  
**Current Role:** Associate Vision Science Practitioner – Ophthalmic Imaging (Great Ormond Street Hospital, London)  
**Academic Background:** MSc Biomedical Engineering – University of Bristol  
**Research Focus:** Translating quantitative imaging and AI methods between retinal and brain microvascular systems.  
**Purpose:** Independent pilot to support PhD application for “Improving Robustness of Brain Perfusion and Permeability Imaging Using Deep Learning” at the University of Manchester.

