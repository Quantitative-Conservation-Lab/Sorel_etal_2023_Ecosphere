# Wenatchee-survival


The purpose of the repository is to estimate survival, smolt-to-adult return rates, and return age probabilities for spring Chinook salmon (*Cncorhynchus tshawytscha*) marked as juveniles within the Wenatchee River Basin when emigrating from their natal stream. 

The controlling script is  `manuscript/fit_wen_MSCJS_play3.Rmd`.
Please direct any questions or comments to me, Mark Sorel, at marks6@uw.edu.



## Table of Contents
archive folder - contains old material not used in the paper

Data folder - contains data used in the analysisx

manuscrift folder - contains the main script, `fit_wen_MSCJS_play3.Rmd`,which conducts the analysis and generates figures and tables. Also contains files for formatting references and a style template for Rmarkdown.

src folder - contains r and TMB/c++ code processing data, fitting model, and presenting results
- `data_proc.R` takes files downloaded from PTAGIS.org and turns them into capture histories
- `Env data funcs.R` downloads and processes environmental covariate data
- `mscjs_wen_helper_funcs.R` functions for plotting data and printing tables
- `Wen_MSCJS_re_3.R` functions to takes capture histories and covariate data and format them for model fitting. Also, a helper function to fit the model.
- `wen_mscjs_re_4.cpp` the TMB model code

## Required Packages and Versions Used
here_1.4.4

tidyverse_1.3.0

dataRetrieval_4.3.0

ggthemes_1.5.1

TMB_1.13.0

bookdown_1.4.5

captioner_3.3.2

DHARMa_0.4.0


## Attractant One: visual survey (VIS) lure/no lure

Data were collected in 2015 where biologists walked transects in CP that either had no traps (no lure) or traps with mice (lure)

The goal was to understand if encounter rate and detection probability were different between these two scenarios

We use an indicator variable (STATUS) to denote when 1 = a transect was not surveyed, 2 = a transect was surveyed but no lures were used, and 3 = a transect was surveyed and lures were used 

## Attractant Two: visual survey (VIS) scent/no scent

Data were collected in 2016 where biologists walked transects in CP that either had no scent applied (no scent), were freshly sprayed earlier that evening with fish fertilizer (fresh scent), or had been sprayed 24-hours previously with that scent (old scent)

The goal was to understand if encounter rate and detection probability were different between these three scenarios

We use an indicator variable (STATUS) to denote when 0 = a transect was not surveyed, 2 = a transect was surveyed but no scent was sprayed, 3 = a transect was surveyed and fresh scent was applied, and 4 = a transect was surveyed and scent had been applied the day before

We fit two models in a Spatially Explicit Capture-Recapture framework. 

## Details of article

Details of this work can be found in the published journal article on this topic:

Sorel MH, Murdoch AR, Zabel RW, Jorgensen JC, Kamphaus CM, and Converse SJ. Juvenile life history diversity is associated with life-long demographic heterogeneity in a migratory fish. Ecosphere.

## How to use this repository

Start in the files `manuscript\fit_Wen_MSCJS_play3.Rmd` file. This can be knitted to run the entire analysis and create all the results, figures, and tables included in the paper.