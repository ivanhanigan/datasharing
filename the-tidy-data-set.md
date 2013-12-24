---
name: the-tidy-data-set
layout: default
title: the-tidy-data-set
---


The general principles of tidy data are laid out by [Hadley Wickham](http://had.co.nz/) in [this paper](http://vita.had.co.nz/papers/tidy-data.pdf)
and [this video](http://vimeo.com/33727555). The paper and the video are both focused on the [R](http://www.r-project.org/) package, which you
may or may not know how to use. Regardless the four general principles you should pay attention to are:

1. Each variable you measure should be in one column
1. Each different observation of that variable should be in a different row
1. There should be one table for each "kind" of variable
1. If you have multiple tables, they should include a column in the table that allows them to be linked

While these are the hard and fast rules, there are a number of other things that will make your data set much easier
to handle. First is to include a row at the top of each data table/spreadsheet that contains full row names. 
So if you measured age at diagnosis for patients, you would head that column with the name `AgeAtDiagnosis` instead
of something like `ADx` or another abbreviation that may be hard for another person to understand. 


Here is an example of how this would work from genomics. Suppose that for 20 people you have collected gene expression measurements with 
[RNA-sequencing](http://en.wikipedia.org/wiki/RNA-Seq). You have also collected demographic and clinical information
about the patients including their age, treatment, and diagnosis. You would have one table/spreadsheet that contains the clinical/demographic
information. It would have four columns (patient id, age, treatment, diagnosis) and 21 rows (a row with variable names, then one row
for every patient). You would also have one spreadsheet for the summarized genomic data. Usually this type of data
is summarized at the level of the number of counts per exon. Suppose you have 100,000 exons, then you would have a
table/spreadsheet that had 21 rows (a row for gene names, and one row for each patient) and 100,001 columns (one row for patient
ids and one row for each data type). 

If you are sharing your data with the collaborator in Excel, the tidy data should be in one Excel file per table. They
should not have multiple worksheets, no macros should be applied to the data, and no columns/cells should be highlighted. 
Alternatively share the data in a [CSV](http://en.wikipedia.org/wiki/Comma-separated_values) or [TAB-delimited](http://en.wikipedia.org/wiki/Tab-separated_values) text file.
