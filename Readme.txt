Readme file for Generalist Evolution Project

	- Latest update 9-24-2021
	- Overview of code and data used in preparation of manuscript submitted to Scientific Reports, Sept. 2021 (J. R. Morris, K. A. Allhoff, F. S. Valdovinos)

Contents:
	1) Eco-evolutionary food web (C code)
	2) Data processing and analysis (R code)
	3) Summary data file documentation (R output)
	4) R version and package info


1) Eco-Evolutionary Food Web Model (C code)

The code can be run using the following commands below. See comments in MODEL_CLEAN.c file for details.

  Create executable file:
	gcc MODEL_CLEAN.c -std=c99 -lm -lgsl -lgslcblas -ffast-math -o MODEL_CLEAN.out

  Run simulation:
	./MODEL_CLEAN.out res_CLEAN 12345 0.05 1 0.5 0.2 0.4 0.4 0.3 1


2) Data Processing and Analysis Code (R code)

Two files are included for all data processing and analysis performed in the manuscript.

	ANALYSIS_ZSWEEP_HIST_FINAL.R
	ANALYSIS_ZSWEEP_COM_FINAL.R

Both files include code for processing raw data output from simulations, but also summary data generated in R. Statical analysis and figure generation code is included in both files. Import summary data files included here to run this analysis. See R code files for further details.


3) Data Summary Files (from R output)

All data summary files used in statical and visual output for the manuscript are included here. File names and description are listed below. See data analysis code for more details. All files are located in the folder Z_SWEEP_DATA_SUMMARY_FINAL

ALLBINDsub.csv	Species traits, biomass, etc. (subset of replicates)
ALLTROPsub.csv	Species trophic position, etc. (subset of replicates)
CBsum.csv	Community biomass (SD)
FINALFRBINDSAMPLE.csv	Realized feeding range for example simulation
GSLSEXTALL.csv	Generalist/specialist lifespan (mean)
MIFRALL.csv	Feeding range (mean)
MIFRALLmed.csv	Feeding range (median)
RBMsum.csv	Resource biomass (SD)
REALFRSUM.csv	Realized feeding range (mean)
SLOPEALL.csv	Lifespan slope coefficients
SLOPEEXAMPLE.csv	Lifespan to feeding range for z sweep replicate example
TOSsum.csv	Species turnover (mean)


4) R Version and Package Details for Data Processing and Analysis

Output from R sessionInfo()

R version 4.1.0 (2021-05-18)