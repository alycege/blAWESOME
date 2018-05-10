blAWESOME: a means to optimize BLOSUM matrices for detecting horizontal gene transfers

Columbia University
CBMF 4761: Computational Genomics
Final Project
Collaborated with Sal Volpe

Folders for each species (R. felis, E. coli, M. tuberculosis) contains the following files:
-BLASTP query results for each species' proteome (.faa files obtained from NCBI) for each BLOSUM and PAM matrix ([speciesname]_blastp_[blosum/pam][value].csv)
-Query results separated into 'close' and 'distal' groups for each BLOSUM matrix ([speciesname]_[close/distal][value]_2.csv). These files are generated from the Visualization Jupyter notebooks (below).
-Jupyter notebook to process and visualize the bit scores for matrix queried (Visualization_[speciesname].ipynb)
The R. felis folder also contains additional .csv's which were needed to process the change in NCBI accession numbers.

In the main repository, there is also a Jupyter notebook and Excel spreadsheet for statistical analysis, which outputs the results of linear regression on our data. This analysis requires first obtaining results from the close vs. distal groups.

All code was written in Python 3 and can be run directly on the csv files which are the output of commandline BLASTP queries, which should be run on Google Cloud. We also installed the SwissProt database from NCBI (https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download) to run BLASTP locally in Google Cloud. Python libraries we used for this project include: numpy, scipy, scikit-learn, pandas, pyplot, and several other packages built into Anaconda. 