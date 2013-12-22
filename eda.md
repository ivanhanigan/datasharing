--- 
name: eda
layout: default
title: Exploratory Data Analysis
---

- Into a spreadsheet take a list of all files, tables, queries, worksheets (using RODBC sqlTables to extract this list from databases or spreadsheets) 
- assign a new variable based on the observational types, these will act as an umbrella to collect the [LPU](/datasharing/least-publishable-units).
- Then I'd try to carve these umbrella groups into separate LPU ie: Jellybean\_History \_by\_site, Jellybean\_Interval\_Table, Days\_Since\_Jellybean) and Jellybean\_Response.
- And then start a script in whatever language (like R),
- Structure the script into sections, the first section would be Jellybean, then first subsection Jellybean\_History, then another subsection Jellybean\_Response.
- Then move on to the next section/subsection.
- Then scroll up and down between sections adding in exploratory code (maps, graphs, cross-tabs) and comments about what you find, think, decide, change in main data files (if appropriate).
- Then shuffle these around like moving blocks of a jigsaw puzzle until happy enough to share with someone else.
- Do a presentation of the work so far and make notes immediately afterward about things you thought of during the presentation
