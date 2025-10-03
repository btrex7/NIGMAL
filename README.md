NIGMAL: A Dataset and R Codes for Comparative Analyses of Mammalian Extinction Risk and Human Impacts in Nigeria

Bernard Asanbe (2025)



[DOI](https://zenodo.org/badge/1069269813.svg)](https://doi.org/10.5281/zenodo.17259883)



Abstract

This repository contains the datasets and R scripts associated with the Master's thesis: "Assessing Patterns of Extinction Risk among Mammal Species in Nigeria: A Comparative Analysis of Human Impact". The dataset compiles species-level traits, IUCN Red List threat categories, and human impact variables, while the code supports trait-based and phylogenetic logistic regression models. Together, they provide a reproducible resource for studying biodiversity patterns and conservation priorities for mammals in Nigeria and globally.



Background \& Summary:

Nigeria is one of Africa’s biodiversity hotspots, yet mammalian species face growing pressures from habitat loss, hunting, and other human-driven threats. This dataset integrates ecological and life-history traits, phylogenetic information, and IUCN threat data for mammals occurring in Nigeria. The dataset supports trait–threat interaction models and comparative extinction risk analyses. The accompanying R code includes scripts for data cleaning, phylogenetic logistic regression, and model visualization. Openly sharing these resources will facilitate reproducibility and comparative research across other regions and taxa.



Methods:

Data Sources:

• Species list from IUCN Red List database obtained with the range data polygons (.SHP) from https://is.gd/dJAjyP.

• Threat categories from IUCN Red List (2025), https://www.iucnredlist.org.

• Life-history traits (body mass, brain mass reproductive rate, and range size) from IUCN Red List, PHYLACINE 1.2 and COMBINE (Faurby et al., 2018; Soria et al., 2021).

• Human and environmental impact data (land-use, hunting pressure proxies, protected area overlaps) from IUCN Red List.



Data Processing:

• Standardized trait values, log-transformed traits, categorical recording of threats.

• Constructed binary response variables for extinction risk (Threatened vs. Non-threatened).

• Phylogenetic tree obtained from \[Upham et al. 2019 Mammal supertree].



Code Development:

• Scripts in R for trait preprocessing (ETL), data cleaning, model fitting (phylogenetic logistic regression), and interaction effect testing.

• Visualization code for plotting predicted probabilities and trait–threat relationships.



Data Description:

• File 1: Nigerian\_mammal\_traits\_threats.csv

&nbsp;	o Columns: Sci\_name, Phylacine, Phylogeny, Scaled\_Log\_Mass\_g, Scaled\_Log\_Current\_Area\_KM2, Scaled\_Log\_Brain\_Mass\_g, IUCN\_threats, etc.

&nbsp;	o Rows: Each mammal species recorded in Nigeria (n ≈ 314 species).



• File 2: Phylogeny\_tree.tre

&nbsp;	o Pruned tree of Nigerian mammal species for phylogenetic analyses.



• File 3: Phyloglm\_modelling\_results.csv

&nbsp;	o Outputs extracted from trait–threat logistic regression models.



• File 4: README.md (this file)

&nbsp;	o Instructions on file structure, variable definitions, and repository usage.



Code Description:

Script 1: data\_cleaning.R – standardizes species names, formats trait data, merges sources.

Script 2: model\_fitting.R – fits logistic regression and phylogenetic logistic regression models.

Script 3: model\_outputs.R – extracts coefficients, AIC scores, predicted probabilities.

Script 4: visualization.R – generates plots of extinction risk vs. traits/threats.



Usage Notes:

Scripts are designed for R (version ≥ 4.2.0).

Requires packages: sf, readxl, writexl, dplyr, phylolm, ape, caper, car, corrplot, ggplot2 and scales.



Example workflow:

• Run data\_cleaning.R to prepare the dataset.

• Run model\_fitting.R to fit models.

• Continue with running model\_outputs.R to output models.

• Use model\_outputs.R and visualization.R to extract and visualize results.



Limitations:

Dataset restricted to Nigerian mammal species; generalization to other taxa or regions should be cautious.

Some traits have missing values (see File 1 for imputation methods).

Threat categories reflect IUCN assessments up to 2023.



Data \& Code Availability:

All files are available on Zenodo \[DOI](https://zenodo.org/badge/1069269813.svg)](https://doi.org/10.5281/zenodo.17259883).

GitHub repository: \[https://github.com/btrex7/NIGMAL].



Citation:

If using these data/code, please cite as:

Asanbe, B. (2025). NIGMAL: A Dataset and R Code for Comparative Analyses of Mammalian Extinction Risk and Human Impacts in Nigeria. Zenodo. DOI: https://doi.org/10.5281/zenodo.17259883



Reference:

Faurby, S., Davis, M., Pedersen, R., Schowanek, S., Antonelli, A., \& Svenning, J. (2018). PHYLACINE 1.2: The Phylogenetic Atlas of Mammal Macroecology. Ecology, 99(11), 2626. https://doi.org/10.1002/ecy.2443

IUCN (2025, January 12). The IUCN Red List Categories and Criteria. International Union for Conservation of Nature’s Red List database, 1(8), Retrieved 01/12/2025 from https://www.iucnredlist.org/

Soria, C., Pacifici, M., Di Marco, M., Stephen, S., \& Rondinini, C. (2021). COMBINE: a coalesced mammal database of intrinsic and extrinsic traits. Ecology 102(6). https://doi.org/10.1002/ecy.3344





