Bioweb3D
========

Visualisation of sex worker arrests statistical data sets with Bioweb3D software.

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

## 2.) Start [BioWeb3D](http://www.ebi.ac.uk/~jbpettit/bioWeb3D/) java software

**2.1) Load the dataset file into the software** You see a grey mountain of connected data points (arrest figures of the same year of all the different age groups are connected)

x axis: years from 1981 to 2010

z axis: age groups -9, -12, -14, -15, -16, -17, -20, -24, -29, -34, -39, -44, -49, 54, -59, -64 and 65+

y axis: number of arrests from 0 to 159.735 arrests (this max is for males 21-24 years and arrested 1982 for disorderly conduct)

**2.2) Load the cluster file into the software** With the "select data" drop down menue you can select and deselect clusters and assign colors. There are sets for the 4 main arrest groups (female/male for prostitution or disorderly conduct), which are equivalent to 4 penetrating surfaces and sets for all age groups and years which are like curves, when the 3D surface cuts the parallel plane slices. In "View" you can mount different coordinate systems side by side and rotate them simultaneously. In "Settings" you can adjust axis magnification and size of marks.


Data source FBI, via [bjs.ojp.usdoj.gov](http://www.bjs.ojp.usdoj.gov/index.cfm?ty=datool&surl=/arrests/index.cfm) and [PoliceProstitutionandPolitics.com](http://www.PoliceProstitutionandPolitics.com).

More information: [bit.ly/arrestmap](http://www.bit.ly/arrestmap).
