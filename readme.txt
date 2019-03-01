### Data Parsings and Prep

Data_Parse_All_csv is a python script for for converting .xyz files produced by
the publication "Quantum chemistry structures and properties of 134 kilo molecules"
by Ramakrishnan et al. (doi: 10.1038/sdata.2014.22)

Data_Parse_Small_csv_pif is a similar script, but only produces 1/10th of the data
rather than the whole set in both .csv and .pif formats.

These scripts are available in .ipynb format to show output history.

The files can be obtained as a zip archive from:
https://figshare.com/articles/Data_for_6095_constitutional_isomers_of_C7H10O2/1057646

This zipped file contains 133,885 GDB-9 generated .xyz files, which can be converted
into the .pif format for use with the Citrination platform.

This script will take a user specified range of files from the downloaded archive,
insert them into a Pandas dataframe, then convert that dataframe into .pif dump.  The
resulting file is an archive similar to a .json that more conveniently stores this data for
practical use in the context of chemistry, materials science, physics, and engineering.

For more information on using the pypif module, please read below:
https://github.com/CitrineInformatics/pypif


### EDA, Modeling

Clustering_Regression contains a notebook that uses the .csv output of the full dataset.
The methods used are sklearn's implementation of K-Means and various regression models
(Ridge, Lasso, DecTree).

The results show that it is possible to model some relevent physical properties of small 
organic molecules (HOMO, LUMO, Polarizability).  Althogh this is used a computational dataset,
this workflow demonstrates that using ML and big data techniques can be useful in physical sciences.