bioWeb3D
========

Visualisation of FBI arrests and statistical data sets with bioWeb3D open software tool.

This novel interactive visual approach to recheck sex worker arrest data from the US has been added by Arrest Mapper Project `bit.ly/arrestmap`. One only needs to download two text files with nationwide police arrest data, start a browser app and then you can display millions of arrest data points for intuitive 3D reviewing. The open software was developed at European Molecular Biology Laboratory Cambridge (_and its use was somehow inspired by this years Nobel price for chemistry and the recent success of the gamer community to resolve HIV puzzle with 3D structure folding..._;-).



[![Arrests for prostitution](http://farm6.staticflickr.com/5486/10420986775_e22620dac2_o.jpg "screen shot")](http://www.bit.ly/arrestmap)

Watch this how-to video http://www.youtube.com/watch?v=y1yviO6R7m4 (6 min).

## 1.) Download U.S.A. prostitution arrest data in two text files:
1. arrest-dataset.jason
2. arrest-cluster.jason

Use the `Download ZIP` button on the right to fetch all files in one archive (or click one by one a file name, then the `Raw` button in the frame headline to get it displayed raw in black font only, and then select `save as` from your browser menu). 

The files contain adjusted data of 24 million arrests in 2,040 records categorized by:
- arrests for prostitution or disorderly conduct
- male/female
- 17 age groups -9 ... 65+
- 30 years

## 2.) Start [bioWeb3D](http://www.ebi.ac.uk/~jbpettit/bioWeb3D/) java software in (this) browser window

**2.1) Load the arrest-dataset.jason file into the software** 

You get to see a grey mountain of data points in 3D year-age-arrests space:

x axis: year from 1981 to 2010

z axis: age group -9, -12, -14, -15, -16, -17, -20, -24, -29, -34, -39, -44, -49, 54, -59, -64 and 65+

y axis: number of arrests from 0 to 159.735 arrests (this maximum is for males 21-24 years arrested 1982 for disorderly conduct)

Connected are arrest figures of one same year comprising all different age groups. 

(Lines can be switched off by changing the chain variable's bolean value from "true" into "false" in this JASON text file. Since that is the default one can delete the full code line or better switch it temporarily off (comment off) by inserting the comment tag `//` at the beginning of the chain code line.)

        // 	"chain" : true,
        
(The axes names in the display window can be overwritten with custom labels in each direction e.g. the values in that direction 1981 - 2010, 9 - 65, 0 - 160,000. Double click to close input field.)

**2.2) Load the arrest-cluster.jason file into the software** 

With the `select data` drop down menue you can select and deselect clusters and assign colors. There are sets for the 4 main arrest groups (female/male for prostitution and disorderly conduct), which are equivalent to 4 penetrating 3D surfaces and there are sets for all age groups and all years which show up like curves, when the arrest surfaces cut parallel plane slices of constant year or age. 

In `View` you can mount different coordinate systems side by side and rotate them simultaneously. One handy setting for data interpretation is to have only arrests for prostitution male/female selected in blue/red in world 1, disorderly conduct with two lighter colours in world 2, all age groups in world 3 and years in 4. (Colouring vector starts "white" followed by "red" for age groups and years respectively) 

In `Settings` you can adjust axis magnification (coefficients) and size and transparency of marks. 

Zoom in and out with mouse wheel or two fingers. Maximum zoom is when the center of rotation or coordinate system is in the plane of your computer screen and you are sitting virtually within the data cloud. (Adjust window magnification in Firefox browser with `ctrl_+` and `ctrl_-`).

## Some preliminary findings

Most arrests are for disorderly conduct. For prostitution mostly females get arrested: 1.9 million females compared to 1 million males arrested in the US 1980-2010.

Through the years more and more older women (sex workers of more age groups) have been arrested for prostitution, outnumbering men (clients or possible male and trans* sex workers), although there is an outspoken 'end demand' policy in place in the US. Counterfactual and hegemonistically sex workers are categorized as victims in the media driven public discourse, but we found that females are targeted number one by police arrests on prostitution. On `bit.ly/arrestmap` we provide maps with geocoded data, costs of arrests, more analysis and raw data.

Regarding so called "child prostitution" the anti-prostitution media propaganda can not be substanciated with FBI data. Contrary to public belief, prostitution of minors is low as data for prostitution arrests from the very many sting operations reveal. Figures or curves only raise after age of maturity with the 18-20 years age group (default color code light green). Younger than 21 years are 13.38% of all female prostitution arrests, < 18 years are 1.16%, < 16 are 0.28% and [younger than 14 years (child) are only 0.02%](http://bit.ly/19xHowd).

## How the input data files are created

Collect the data with spreadsheet software e.g. [openOffice.org](http://en.wikipedia.org/wiki/OpenOffice.org) or [Gnumeric](http://en.wikipedia.org/wiki/Gnumeric).

Create additional table columns for adjustment, sorting, clustering and finally number export. The export column contains text formulas to add all the necessary brackets, spaces, comma/point, adjustment factors and format syntax required for the two JASON files. E.g. when age, arrests and year figures are given in column cells A2, B2 and C2, respectively, then the export formula may look like this `E2="["&A2*3&", "&substitute(B2/400;",";".")&", "&substitute((C2-1980)*3;",";".")&"],"`.

Alternatively text files.csv (comma separated values format) can also be used as input files for bioWeb3D and directly exported from spreadsheet software. Use advanced search and replace with [regular expression](http://wiki.openoffice.org/wiki/Documentation/How_Tos/Regular_Expressions_in_Writer), which is available in openOffice text files, as an alternative option to generate the needed JASON file format. E.g. to individually include all lines from a long file list into brackets, find each line start by searching for `^(.)` (a character at the beginning) and replace all found with `[$1` (the found expression per line $1 plus the bracket), then search for line endings `(.)$` and replacement all at once with `$1],`.

Copy the generated data columns from the spreadsheet or processed text file into the right place in the manually edited JASON text file. This on-line parsing tool [jsonEditoronline.org](http://www.jsoneditoronline.org) can help to find editing errors. For frequent .csv into .jason conversion and file generation scientists have provided a pascal script for automation, with is available at the bioWeb3D source code files on github.

## References and sources

bioWeb3D: [open access publication and user manual](http://www.ncbi.nlm.nih.gov/pubmed/23758781) and [examples from biology and software source code](https://github.com/jbogp/bioWeb3D).

Our [how-to video](http://www.youtube.com/watch?v=y1yviO6R7m4) (6 min).

Arrest data source: FBI via [bjs.gov data tool](http://www.bjs.gov/index.cfm?ty=datool&surl=/arrests/index.cfm) and [PoliceProstitutionandPolitics.com](http://www.PoliceProstitutionandPolitics.com).


More information and home page: [Arrest Mapper Project: bit.ly/arrestmap](http://www.bit.ly/arrestmap).
