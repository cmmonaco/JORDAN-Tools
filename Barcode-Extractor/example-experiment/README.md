# Example Experiement for Barcode Counts Extraction

This repository contains a sample dataset from an actual experiment conducted by the Dahlman Lab. It is meant to test the installation of and provide an sample of using the BCCE tool on real data. In this repository you will find the Experiment's Barcode Library file (`bclib.txt`), a folder containing indexed FASTQ files (`data`), and a folder containing the output from execution of the tool.

## Running BCCE on Sample Data

To run the tool on the sample data provided, simply type the following command

   ../bccextractor -l bclib.txt -i data/ -o output/example_raw.csv

For more information on using and running the tool, see the detailed experiemtnal protocol available on the Dahlman Lab [website](http://dahlmanlab.org).