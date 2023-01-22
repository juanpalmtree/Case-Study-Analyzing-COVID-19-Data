As a data analyst, I have used SQL to analyze data and answer various questions related to the Covid-19 pandemic.

## Data questions:
- How many confirmed cases of Covid-19 have there been in a specific country?
- What is the breakdown of confirmed cases by age group in a specific country?
- What is the trend of confirmed cases over time in a specific country?
- How do confirmed cases in a specific country compare to other countries?
- What is the mortality rate for Covid-19 in a specific country?

## SQL solutions:


To find the number of confirmed cases of Covid-19 in a specific country (e.g. United States), the following SQL query can be used:

SELECT COUNT(*) FROM Covid19_cases WHERE country='United States';

To find the breakdown of confirmed cases by age group in a specific country (e.g. United States), the following SQL query can be used:

SELECT age_group, COUNT(*) FROM Covid19_cases WHERE country='United States' GROUP BY age_group;

To find the trend of confirmed cases over time in a specific country (e.g. United States), the following SQL query can be used:

SELECT date, COUNT(*) FROM Covid19_cases WHERE country='United States' GROUP BY date ORDER BY date;

To compare the confirmed cases in a specific country (e.g. United States) to other countries, the following SQL query can be used:

SELECT country, COUNT(*) FROM Covid19_cases GROUP BY country ORDER BY COUNT(*) DESC;

To find the mortality rate for Covid-19 in a specific country (e.g. United States), the following SQL query can be used:

SELECT (COUNT(Covid19_cases.deaths)/COUNT(Covid19_cases.cases))*100 as mortality_rate  FROM Covid19_cases WHERE country='United States'
