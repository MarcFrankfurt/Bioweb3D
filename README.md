Bioweb3D
========

Visualisation of sex worker arrests statistical data sets with Bioweb3D open software tool.

This novel interactive visual aproach to check sex worker arrest data from the US has been added by Arrest Mapper Project bit.ly/arrestmap. One only needs to download two text files with FBI arrest data, start a browser app and then you can display millions of arrest data points for intuitive 3D data reviewing. The open software is developed at European Molecular Biology Laboratory Cambrige and somehow related to this years nobel price for chemistry.



[![Arrests for prostitution](http://farm3.staticflickr.com/2879/10194975484_08b5e6b7e4_c.jpg "screen shot")](http://www.bit.ly/arrestmap)

## 1.) Download U.S.A. prostitution arrest data in two text files:
1. arrest-dataset.jason
2. arrest-cluster.jason

Use the "Download ZIP" button on the right to fetch all files in one archive (or click one by one a file name, then the "Raw" button in the frame headline to get it displayed raw in black font only, and then select "save as" from your browser menue). 

The files contain data of 24 million arrests in 2,040 records categorized by:
- arrests for prostitution or disorderly conduct
- male/female
- 17 age groups -9 ... 65+
- 30 years

## 2.) Start [bioWeb3D](http://www.ebi.ac.uk/~jbpettit/bioWeb3D/) java software

**2.1) Load the arrest-dataset.jason file into the software** You see a grey mountain of connected data points (arrest figures of the same year of all the different age groups are connected)

x axis: years from 1981 to 2010

z axis: age groups -9, -12, -14, -15, -16, -17, -20, -24, -29, -34, -39, -44, -49, 54, -59, -64 and 65+

y axis: number of arrests from 0 to 159.735 arrests (this max is for males 21-24 years and arrested 1982 for disorderly conduct)

**2.2) Load the arrest-cluster.jason file into the software** With the "select data" drop down menue you can select and deselect clusters and assign colors. There are sets for the 4 main arrest groups (female/male for prostitution or disorderly conduct), which are equivalent to 4 penetrating surfaces and sets for all age groups and years which are like curves, when the 3D surface cuts the parallel plane slices. In "View" you can mount different coordinate systems side by side and rotate them simultaneously. One handy setting for data interpretation is to have only arrests for prostitution male/female selected in blue/red in world 1, disorderly conduct with 2 lighter colors in wold 2, all age groups in world 3 and years in 4. (Coloring vector startes white followed by red.) In "Settings" you can adjust axis magnification and size of marks. (Adjust window magnification in firefox browser with 'ctrl\_+' and 'ctrl\_-').

## Some results

Most arrests are for disorderly conduct. For prostitution mostly females get arrested: 1.9 million females compared to 1 million males arrested in the US 1980-2010.

Through the years more and more older women (sex workers) get arrested for prostitution, outnumbering men (possible clients), although there is an outspoken 'end demand' policy in place in the US. 

Arrests for prostitution is very low for minors. Figures or curves go only up after age of maturity with the 18-20 years age group (default color code light green).

## How were the data input files created:

Collect the data with spreadsheet software e.g. openOffice.org.

Create additional table colums for sorting, grouping and number export. They contain all the brackets, commas and format syntax required for the two JASON files. Btw. text files.csv (comma separated values) can also be used and directly exported form a spreadsheet. Search and replace with [regular expression](http://wiki.openoffice.org/wiki/Documentation/How_Tos/Regular_Expressions_in_Writer) available in openOffice text files is an alternative option to generate the correct file format.

Copy the generated data colums from the spreadsheed into the right place in the manually edited JASON text file. There is also an on-line tool jsoneditoronline.org. Scientist can use a pascal script given with the Bioweb3D source code for automated .csv into .jason conversion and file generation.


Arrest data source: FBI, via [bjs.ojp.usdoj.gov](http://www.bjs.ojp.usdoj.gov/index.cfm?ty=datool&surl=/arrests/index.cfm) and [PoliceProstitutionandPolitics.com](http://www.PoliceProstitutionandPolitics.com).

More information: [Arrest Mapper Project bit.ly/arrestmap](http://www.bit.ly/arrestmap), [open access publication and bioWeb3D user manual](http://www.ncbi.nlm.nih.gov/pubmed/23758781) and [bioWeb3D software and data source code](https://github.com/jbogp/bioWeb3D).
