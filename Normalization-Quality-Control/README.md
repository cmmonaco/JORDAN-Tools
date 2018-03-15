# Normalization and Post-Normalization Quality Control

All scripts contained in this repository along with all supporting documentation Copyright (c) Dahlman Lab, 2018

## About

This reposistory contains the [R Markdown](http://rmarkdown.rstudio.com) scirpts used to normalize raw counts data and assess its quality. The use of R Markdown allows the script to be self-documenting and automatically generates an HTML report upon execution. Templates of these scripts are found unt the `template-scripts` folder. These are skeleton scripts ready to be customized for a new experiment. An example of how these scripts are to be used along with test data is located in the `example-experiment` folder.

For deatils on how these scripts are used in the Dahlman Lab JORDAN pipeline, please see our detailed protocol on the Dahlman Lab [website](http://www.dahlmanlab.org).

### Normalization

Normalization of raw counts data is performed using the `normalization.Rmd` script. This script will analyze the injection inputs and normalize the samples back to those inputs and to unity. The script will generate a CSV file containing normalized sample counts.

### Quality Control Assessment

Post-normalization Qualiy Control is performed using two seperate R Markdown scripts.

#### Biological Replicate Correlation Studies

We wish to assess correlation between biological replicates prior to averaging counts into single samples. To do this, we employ pairwise Pearson Correlation tests to each replicate group to identify low correlation outliers that should be removed. This is accomplished with the `replicate_correlation.Rmd` script.

#### Run-aways Barcode Identification

We also wish to identify any potential run-away barcodes occuring in our experiemnt to assess experimental conditions. `runaway_id.Rmd` performs single linkage hierarchical clustering and principal components analysis to identify outlying barcodes that may be potential run-aways.

## Usage

These scripts require R and R Studio be installed with the following libraries:

- [ggplot2](http://ggplot2.org)
- [ggfortify](https://cran.r-project.org/web/packages/ggfortify/vignettes/plot_pca.html)
- [ComplexHeatmap](https://bioconductor.org/packages/release/bioc/html/ComplexHeatmap.html)

For details on preparation and use, please see the commented sections within each script.

---

*Originally authored by:* [Christopher M. Monaco](https://github.com/cmmonaco) \
*Currently maintained by:* Christopher M. Monaco
