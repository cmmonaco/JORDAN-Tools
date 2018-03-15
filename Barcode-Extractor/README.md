# Barcode Counts Extractor

Barcode Counts Extractor and all supporting documentation
Copyright (c) Dahlman Lab, 2016-2018

## About

Barcode Counts Extractor (BCCE) is a simple python tool to extract barcode counts from a series of FASTQ files. It is intended to be used with the JORDAN nanoparticle DNA barcoding system developed by the [Dahlman Lab](http://www.dahlmanlab.org). It was built under Python 2.7.13 but should still run on later versions.

## Usage

BCCE operates on a directory of indexed FASTQ files to generate a counts file. It can run on data *in place*, meaning that sequencing data does not need to manipulated or moved prior to running the tool.

Once the prerequisites are in place, BCCE can be run from the terminal as follows

	usage: bccextractor [-h] [-v] -l <lib.txt> -i <indir> -o <out.csv> [-s <int>] [-b <int>] [-p <str>] [-t <int>]

	Barcode Counts Extraction Tool for Dahlman Lab JORDAN System

	Required Arguments:
	  -l, --lib	Experimental barcode library file. Should be tab-delimited text.
	  -i, --inDir	Input directory containing FastQ files to be processed.
	  -o, --outFile	Output file name. Should be contains CSV file extension.

	Optional Arguments:
	  -p, --prefix	File name prefix to drop in output file sample names.
	  -s, --start   Barcode start position (nucleotide number starting at 5' end from 1). Default = 55.
	  -b, --length  Barcode length. Default = 8.
	  -t, --thread  Number of processing threads to use during execution. Default = 8.

	Information Arguments:
	  -v, --version Show program's version number and exit.
	  -h, --help	Show this help message and exit.

## Execution Stats

Upon completion, the script will return a CSV file containing a table of raw counts formatted so that columns are samples extracted from the names of the FASTQ files and rows are barcodes from the supplied library file. In addition, a log file will be generated containg run time statistics from the tool including mean quality scores in the barcode region and number of barcodes identified versus number of total sequence processed. Plots of these stats are also created to provide a quick instight into overall data quality.

## Dependencies

BCCE requires the following Python libraries:

- [pandas](https://pandas.pydata.org/)
- [numpy](http://www.numpy.org/)
- [matplotlib](https://matplotlib.org/)

---

*Originally authored by:* [Christopher M. Monaco](https://github.com/cmmonaco) \
*Currently maintained by:* Christopher M. Monaco
