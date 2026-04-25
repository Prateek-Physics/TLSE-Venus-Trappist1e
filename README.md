# TLSE-Venus-Trappist1e

# Quantifying Apparent Radius Inflation in Transits due to Starspots: A Comparative Study of Venus and TRAPPIST-1e

## Project Overview
This repository contains the computational pipeline used to investigate the **Transit Light Source Effect (TLSE)**. By modeling the Venusian transit of 2012 as a ground-truth benchmark, this project quantifies the bias introduced by stellar limb darkening and non-uniform photospheric features (starspots) when measuring planetary radii in M-dwarf systems like TRAPPIST-1e.

## Repository Structure
The project is organized into three modular pipelines:

* `/detrending`: Pre-processing of raw SDO/HMI continuum FITS data to extract clean light curves.
* `/mcmc`: Bayesian MCMC framework implemented to derive transit parameters and evaluate posterior distributions.
* `/simulation`: Numerical engine for sub-pixel stellar disc integration and non-linear limb darkening modeling.

## Methodology
The pipeline utilizes high-cadence SDO/HMI data spanning from June 3, 2012, to June 6, 2012. We employ a Bayesian MCMC approach to fit light curves, integrating PHOENIX stellar models to account for wavelength-dependent contrast ratios—a critical factor often overlooked in standard transit analysis.



## Code Availability & Reproducibility
All numerical engines and analytical tools are written in Python. The repository is fully reproducible; users can replicate the analysis by following the sequence:
1. `detrending/Detrending.ipynb`
2. `mcmc/mcmc_sampler.ipynb`
3. `simulation/stellar_grid.py`

*Note: The pipeline is optimized for Google Colab environments. See individual notebooks for dependency requirements (`batman`, `emcee`, `corner`).*

## License
This project is licensed under the MIT License.

## Acknowledgements
We acknowledge the support of the Observational Astronomy Lab and the mentorship of Dr. Sanjeev Kumar Verma and Dr. Arun Kumar Awasthi. We thank Google's Gemini AI for assistance in pipeline optimization and code documentation.
