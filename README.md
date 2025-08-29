# MSc_Project-Bayesian-Inference-for-Geospatial-Network-Models

This repository contains the code and notebooks used in my research on **Bayesian Inference for Geospatial Network Models** and their evaluation. The work combines IPF algorithm to retrieve census data, intervening opportunities modeling and Bayesian spatial modeling.

## Repository Structure

- **`notebooks/`**
  - `ipf_01_nuts3.ipynb` : Implementation of **Iterative Proportional Fitting (IPF)** for fitting marginals on NUTS3 socio-ddemographic data. Contains generaed synthetic populations to test algorithm. This notebook contained a Bayesian estimation of temporal transition matrix I carried out during my research.
  - `SCI_IO.ipynb` : Model comparison notebook that evaluates the fit of **SCI (Spatial Comparative Index)** under different specifications (distance-based vs. intervening opportunities), using normalized MSE as performance metric.
  - `Bayesian_Modeling_Notebook.ipynb` : Bayesian modeling of the baseline interaction model referred as simple model in the Report.
    - Due to limited computational resources, this notebook was adapted to run on **Google Colab with GPU support**.

- **`figures/`**
  Contains the plots and figures generated during the analyses.

## Data

The datasets used in this project are publicly available from **[Eurostat](https://ec.europa.eu/eurostat)**. They provide regional statistics, including population, socio-demographic characteristics, and economic indicators.


## Methodological Context

The project explores multiple approaches for modeling spatial interactions:

- **Classical distance-based models**
- **Fuzzy intervening opportunities models** (Kotsubo-type variants)
- **Bayesian hierarchical spatial models** implemented with **NumPyro**

The evaluation is based on **SCI indices** and comparative goodness-of-fit measures (normalized MSE).

## Purpose

This repository documents the reproducible workflow behind my research project focusing on:

- The implementation of IPF for population synthesis

- Comparative analysis of spatial interaction models

- Bayesian modeling under computational constraints

## Requirements

- Python 3.10+
- Common data science stack: `numpy`, `pandas`, `matplotlib`
- Bayesian inference: `jax`, `numpyro`

Install dependencies with:

```bash
pip install -r requirements.txt

