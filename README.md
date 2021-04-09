# hydromet_dengue

Data and `R` code to support Lowe *et al.*, (2021). Combined effects of hydrometeorological hazards and urbanisation on dengue risk in Brazil: a spatiotemporal modelling study. *The Lancet Planetary Health* (https://doi.org/10.1016/S2542-5196(20)30292-8). 

To cite this repo:

Rachel Lowe. (2021). Data and R code to accompany 'Combined effects of hydrometeorological hazards and urbanisation on dengue risk in Brazil: a spatiotemporal modelling study' (Version v1.0.0). Zenodo. http://doi.org/10.5281/zenodo.4632205

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4632205.svg)](https://doi.org/10.5281/zenodo.4632205)

--------------------------------------------------------------------------------

This study details a methodological framework to estimate the delayed and nonlinear impact of hydrometeoroloigcal hazards on dengue risk according to different socio-economic factors. The approach builds upon previous studies to model the impact of climate and socio-economic factors in Brazil by coupling distributed lag nonlinear models (DLNM) ([Gasparrini *et al.*, 2013](https://doi.org/10.1002/sim.3940)) with space-time Bayesian hierarchical models ([Lowe *et al.*, 2014](https://doi.org/10.1016/S1473-3099(14)70781-9), [Lowe *et al.*, 2018](https://doi.org/10.1371/journal.pmed.1002613)) fitted using integrated nested Laplace approximations in `R` (R-INLA) ([Lindgren *et al.*, 2015](https://www.jstatsoft.org/article/view/v063i19)). The modelling approach simultaneously describes space-varying, non-linear, and delayed associations between dengue incidence rates and hydrometeorological variables. These exposure-lag-response associations can reveal how hydrometeorological hazards might impact dengue risk in the months leading up to an outbreak. 

--------------------------------------------------------------------------------

A description of each file and folder is provided below:

  **00_load_packages_data.R:** `R` script to load and process data needed to run DLNMs in INLA models. There is no need to run this script. It is sourced by the following scripts. 

  **01_visual_data.R:** `R` script to explore and visualise dengue, hydrometeorological and socio-economic datasets.

  **02_model_models.R:** `R` script to run DLNM-INLA models of increasing complexity.

  **03_model_output.R:** `R` script to explore and visualise model outputs from the selected model.

  **04_lag_nonlinear_output.R:** `R` script to explore and visualise exposure-lag-response associations given different socio-economic scenarios.

  **05_sensitivity_analysis.R:** `R` script to test sensitivity of exposure-lag-response associations.
  
  **data:** a folder containing the database, data description, and a grid file for `facet_geo()` plots (in .csv format), and shapefiles (.shp, .shx, .dbf, .prj). 
  
  **figs:** a folder to save the figures generated by the `R` scripts.
  
  **output:** a folder to save the model outputs. This also contains a subfolder named **preds**, with the R script used to generate the cross-validation exercise and associated output files. 
  
  **hydromet_dengue.Rproj:** An `RStudio` project file, to avoid having to set your working directory to the hydromet_dengue folder on your computer. 

Download the repository as a ZIP file using the green button *Clone or download* above, then open the .Rproj file in `RStudio` to begin. 

The analysis was performed using R version 4.0.2 (2020-06-22).

For any issues with the code please contact [Rachel Lowe](https://www.lshtm.ac.uk/aboutus/people/lowe.rachel).
