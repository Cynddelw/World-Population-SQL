# World-Population-SQL
Sample of SQL code for the codecademy project 'World Populations SQL Practice.' Code was run in terminal outside of CA learning environment using sqlite3. 

Q: What years are covered by the dataset? 

> SELECT DISTINCT year
   ...> FROM population_years
   ...> ORDER BY year DESC;
2010
2009
2008
2007
2006
2005
2004
2003
2002
2001
2000

Q: What is the largest population size for Gabon in this dataset?

SELECT population
   ...> FROM population_years
   ...> WHERE country ='Gabon'
   ...> ORDER BY population DESC;
1.54526
1.51499
1.48583
1.45645
1.42639
1.39569
1.36441
1.33262
1.30042
1.26915
1.23643

Q: What were the 10 lowest population countries in 2005?

SELECT country, population
   ...> FROM population_years
   ...> WHERE year = 2005
   ...> ORDER BY population ASC
   ...> LIMIT 10;
Niue|0.00216
Falkland Islands (Islas Malvinas)|0.00297
Montserrat|0.00453
Saint Pierre and Miquelon|0.0062
Saint Helena|0.00748
Nauru|0.01001
Cook Islands|0.0136
Turks and Caicos Islands|0.02057
Virgin Islands, British|0.02268
Gibraltar|0.02846

Q: What are all the distinct countries with a population of over 100 million in the year 2010?

 SELECT country
   ...> FROM population_years
   ...> WHERE population > 100 AND year = 2010
   ...> ORDER BY population DESC;
China
India
United States
Indonesia
Brazil
Pakistan
Bangladesh
Nigeria
Russia
Japan
Mexico

Q: How many countries in this dataset have the word “Islands” in their name?

SELECT DISTINCT country
   ...> FROM population_years
   ...> WHERE country LIKE '%islands%';
Cayman Islands
Falkland Islands (Islas Malvinas)
Turks and Caicos Islands
Virgin Islands,  U.S.
Virgin Islands, British
Faroe Islands
Cook Islands
Solomon Islands
U.S. Pacific Islands

Q: What is the difference in population between 2000 and 2010 in Indonesia? (28.29173)

SELECT population
   ...> FROM population_years
   ...> WHERE country = 'Indonesia'
   ...> ORDER BY population DESC;
242.96834
240.27152
237.51236
234.694
231.82024
228.89575
226.00413
223.06967
220.97191
217.83628
214.67661
