The purpose of the repository is to estimate survival, smolt-to-adult return rates, and return age probabilities for spring Chinook salmon (*Oncorhynchus tshawytscha*) marked as juveniles within the Wenatchee River Basin when emigrating from their natal stream. This is accomplished by fitting a multi-state mark-recapture model to capture histories of PIT tagged fish. The model tracks demographic rates of fish that express different juvenile life history pathways (i.e., ages of emigration from natal streams).

## Table of Contents

-   *archive* folder - contains old material not used in the paper

-   *Data* folder - contains data used in the analysis

-   *manuscrift* folder - contains the main script, `fit_wen_MSCJS_play3.Rmd`,which conducts the analysis and generates figures and tables. Also contains files for formatting references and a style template for Rmarkdown.

-   *src* folder - contains r and TMB/c++ code processing data, fitting model, and presenting results

    -   `data_proc.R` takes files downloaded from PTAGIS.org and turns them into capture histories

    -   `Env data funcs.R` downloads and processes environmental covariate data

    -   `mscjs_wen_helper_funcs.R` functions for plotting data and printing tables

    -   `Wen_MSCJS_re_3.R` functions to takes capture histories and covariate data and format them for model fitting. Also, a helper function to fit the model.

    -   `wen_mscjs_re_4.cpp` the TMB model code

## Required Packages and Versions Used

`R version 4.1.2`

`viridis_0.6.2` `viridisLite_0.4.0` `DHARMa_0.4.4` `glmmTMB_1.1.2.3` `TMBhelper_1.3.0` `TMB_1.7.22` `forcats_0.5.1` `stringr_1.4.0` `dplyr_1.0.7`  
`purrr_0.3.4` `readr_2.1.0` `tidyr_1.1.4`  
`tibble_3.1.6` `ggplot2_3.3.5` `tidyverse_1.3.1`  
`here_1.0.1` `captioner_2.2.`

## Details of article

Details of this work can be found in the in-press journal article on this topic:

Sorel MH, Murdoch AR, Zabel RW, Jorgensen JC, Kamphaus CM, and Converse SJ. Juvenile life history diversity is associated with life-long demographic heterogeneity in a migratory fish. Ecosphere.

### Abstract

Differences in the life history pathways of juvenile animals are often associated with differences in demographic rates in later life stages. For migratory animals, different life-history pathways often result in animals from the same population occupying distinct habitats subjected to different environmental drivers. Understanding how demographic rates differ among animals expressing different life history pathways may reveal fitness tradeoffs that drive the expression of alternative life history pathways and enable better prediction of population dynamics in a changing environment. To understand how demographic outcomes and their relationships with environmental variables differ among animals with different life history pathways, we analyzed a long-term (2006–2021) mark-recapture dataset for Chinook salmon (*Oncorhynchus tshawytscha*) from the Wenatchee River, Washington, USA. Distinct life history pathways represented in this population include either remaining in the natal stream until emigrating to the ocean as a one-year-old (natal-reach rearing) or emigrating from the natal stream and rearing in downstream habitats for several months before completing the emigration to the ocean as a one-year-old (downstream rearing). We found that downstream-rearing fish emigrated to the ocean 19 days earlier on average and returned as adults from the ocean at higher rates. We detected a positive correlation between rate of return from the ocean by downstream-rearing fish and coastal upwelling in their spring of outmigration, whereas for natal-reach-rearing fish we detected a positive correlation with sea surface temperature during their first marine summer. Different responses to environmental variability should lead to asynchrony in adult abundance among juvenile life history pathways. A higher proportion of downstream-rearing fish returned at younger ages compared to natal-reach-rearing fish, which contributed to variability in age at reproduction and greater mixing across generations. Our results demonstrate how diversity in juvenile life history pathways is associated with heterogeneity in demographic rates during subsequent life stages, which can in turn affect variance in aggregate population abundance and response to environmental change. Our findings underscore the importance of considering life history diversity in demographic analyses and provide insights into the effects of life history diversity on population dynamics and tradeoffs that contribute to the maintenance of life history diversity.

## How to use this repository

Start in the `manuscript\fit_Wen_MSCJS_play3.Rmd` file. This can be knitted to run the entire analysis and create all the results, figures, and tables included in the paper.

Questions regarding this repository can be directed to Mark Sorel, [marksorel8\@gmail.com](mailto:marksorel8@gmail.com)
