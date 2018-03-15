# __JO__ int __R__apid __D__NA __A__nalysis of __N__anoparticles (JORDAN) Data Tools

Contents of this directory and all supporting documentation \
Copyright (c) Christopher M. Monaco, 2016-2018

## Introduction

This repository serves as an archive of my work during completion of my M.S. in Bioinformatics from Georgia Tech from 2016-2018. The subdirectories contain custom tools and scripts written in R and Python that were used for data processing and analysis for the [Dalhman Lab's](http://dahlmanlab.org) JORDAN high-throughput nanoparticle characterization system.

The tools in this repository are no longer maintained by me and I will not be offering any support for use of these tools. Up to date versions of the tools and protocol can be found on the [Dahlman Lab]((http://dahlmanlab.org) website. 

## Repository Contents

The following directories can be found in this repository:

1. `Barcode-Extractor` is the main tool used to extract barcode counts from raw Illumina FASTQ files. The user supplies a list of known barcodes and the tool searches all files within an experimental directory to count the number of occurrences of those barcodes. In addition, the tool generates quality control plots showing the percentage of identified barcodes, sequencing depth, and average q-score within the barcode region.
2. `Normalization-Quality-Control` is a set of R scripts used to conduct normalization and quality control assessments of the raw counts data after using the Barcode Extractor tool. The directory contains scripts for barcode counts normalization, bio-replicate correlations studies, and runaway identification using hierarchical clustering and PCA.
3. `Barcode-Generator` is a simple R script used to generate DNA barcodes for use with the JORDAN system that work well with Illumina sequencing color chemistry.
4. `Data-Preprocessing-Protocol` is an unfinished protocols document outlining the use of the JORDAN system to conduct a nanpoparticle screen. While the wet-lab portion of the document was never finished, the Data Processing portion shows how all these tools work together to yield high quality final count data.
5. `Publications` contains PDF versions of publications in which these tools were used to generate experimental data and results.

For more information on each tool or to see how they work, see the READMEs located in each directory.

## Publications`

These tools were used to generate experimental data and results for the following publications:

- [High throughput in vivo functional nanoparticle screening identifies nanoparticles for RNA delivery](). TBA.
- [A Direct Comparison of in Vitro and in Vivo Nucleic Acid Delivery Mediated by Hundreds of Nanoparticles Reveals a Weak Correlation](https://pubs.acs.org/doi/10.1021/acs.nanolett.8b00432). Kalina Paunovska, Cory D. Sago, Christopher M. Monaco, William H. Hudson, Marielena Gamboa Castro, Tobi G. Rudoltz, Sujay Kalathoor, Daryll A. Vanover, Philip J. Santangelo, Rafi Ahmed, Anton V. Bryksin, and James E. Dahlman. __Nano Letters__. DOI: 10.1021/acs.nanolett.8b00432

---

**Disclaimer:** This software is offered as is with no warranty.