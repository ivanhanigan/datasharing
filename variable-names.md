---
name: variable-names
layout: default
title: variable-names
---

This comes from [Josh Reich's blog](http://blog.i2pi.com/post/52812976752/joshs-postgresql-database-conventions):

1. Programming does support AnYSortOF casing that you’d like, it makes cross-project work painful. 
1. All names (table, column, sequence, index, constraint, role, etc.) should be lowercase with underscores.  
1. Table names should be a singular noun that describes one row. “account”, not “accounts”. Some people prefer plural, we just need a standard, my vote is for singular as it makes SQL a little more natural to read e.g.,

#### SQL code:
    SELECT * FROM account WHERE account.balance > 5000;
    

<p></p>
### Let's try this in Ecology: e.g.

    SELECT * FROM tree WHERE tree.species = 'Corymbia maculata';
    
1. Can't name a table 'Species' then.
1. Also Hadley Wickham commented that all names should be lowercase in his [Video about Tidy  Data](http://vimeo.com/33727555).
