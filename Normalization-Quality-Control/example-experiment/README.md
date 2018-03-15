# Example Experiment for Normalization and Post Normalization QC

Here we present raw count data from an actual experiment conducted by the [Dahlman Lab](http://dahlmanlab.org). The scripts here show how to configure and run through the normalization and post-normalization quality control process.

The scripts should be executed in the following order:

1. `normalization.Rmd`
2. `replicate_correlation.Rmd`
3. `runaway_id.Rmd`

*Note:* It is not recommended to edit the `raw_counts.csv` file found in this folder.