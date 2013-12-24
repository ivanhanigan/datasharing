---
name: how-to-code-variables
layout: default
title: how-to-code-variables
---


When you put variables into a spreadsheet there are several main categories you will run into depending on their [data type](http://en.wikipedia.org/wiki/Statistical_data_type):

1. Continuous
1. Ordinal
1. Categorical
1. Missing 
1. Censored

Continuous variables are anything measured on a quantitative scale that could be any fractional number. An example
would be something like weight measured in kg. 

[Ordinal data](http://en.wikipedia.org/wiki/Ordinal_data) are data that have a fixed, small (< 100) number of levels but are ordered. 
This could be for example survey responses where the choices are: poor, fair, good. 

[Categorical data](http://en.wikipedia.org/wiki/Categorical_variable) are data where there
are multiple categories, but they aren't ordered. One example would be sex: male or female. 

[Missing data](http://en.wikipedia.org/wiki/Missing_data) are data
that are missing and you don't know the mechanism. You should code missing values as `NA`. 

[Censored data](http://en.wikipedia.org/wiki/Censoring_(statistics\)) are data
where you know the missingness mechanism on some level. Common examples are a measurement being below a detection limit
or a patient being lost to follow-up. They should also be coded as `NA` when you don't have the data. But you should
also add a new column to your tidy data called, "VariableNameCensored" which should have values of `TRUE` if censored 
and `FALSE` if not. In the code book you should explain why those values are missing. It is absolutely critical to report
to the analyst if there is a reason you know about that some of the data are missing. You should also not [impute](http://en.wikipedia.org/wiki/Imputation_(statistics\))/make up/
throw away missing observations.

- TODO truncated?

In general, try to avoid coding categorical or ordinal variables as numbers. When you enter the value for sex in the tidy
data, it should be "male" or "female". The ordinal values in the data set should be "poor", "fair", and "good" not 1, 2 ,3.
This will avoid potential mixups about which direction effects go and will help identify coding errors. 

Always encode every piece of information about your observations using text. For example, if you are storing data in Excel and use a form of colored text or cell background formatting to indicate information about an observation ("red variable entries were observed in experiment 1.") then this information will not be exported (and will be lost!) when the data is exported as raw text.  Every piece of data should be encoded as actual text that can be exported.
