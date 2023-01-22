As a data analyst, I have used SQL to analyze data and answer various questions related to the Covid-19 pandemic.

## Data questions:
- :bar_chart: **How many confirmed cases** of Covid-19 have there been in a specific country?
- :older_man: **What is the breakdown** of confirmed cases by age group in a specific country?
- :chart_with_upwards_trend: **What is the trend** of confirmed cases over time in a specific country?
- :earth_americas: How do confirmed cases in a specific country compare to other countries?
- :skull: What is the **mortality rate** for Covid-19 in a specific country?

## SQL solutions:


:bar_chart: To find the number of confirmed cases of Covid-19 in a specific country (e.g. United States), the following SQL query can be used:

SELECT COUNT(*) FROM Covid19_cases WHERE country='United States';

:older_man: To find the breakdown of confirmed cases by age group in a specific country (e.g. United States), the following SQL query can be used:

SELECT age_group, COUNT(*) FROM Covid19_cases WHERE country='United States' GROUP BY age_group;

:chart_with_upwards_trend: To find the trend of confirmed cases over time in a specific country (e.g. United States), the following SQL query can be used:

SELECT date, COUNT(*) FROM Covid19_cases WHERE country='United States' GROUP BY date ORDER BY date;

:earth_americas: To compare the confirmed cases in a specific country (e.g. United States) to other countries, the following SQL query can be used:

SELECT country, COUNT(*) FROM Covid19_cases GROUP BY country ORDER BY COUNT(*) DESC;

:skull: To find the mortality rate for Covid-19 in a specific country (e.g. United States), the following SQL query can be used:

SELECT (COUNT(Covid19_cases.deaths)/COUNT(Covid19_cases.cases))*100 as mortality_rate  FROM Covid19_cases WHERE country='United States'

## Fictional Covid-19 Data for United States:

| country   | gender | age_group  | cases | deaths |
|-----------|------------|------------|-------|--------|
| United States | Male | Child   | 10000   | 20      |
| United States | Male | Teen | 15000   | 50      |
| United States | Male | Adult | 200000   | 10000      |
| United States | Female | Child   | 9000   | 15     |
| United States | Female | Teen | 12000   | 35     |
| United States | Female | Adult | 180000   | 8000     |


## Fictional Covid-19 Data for India:

| country   | gender | age_group  | cases | deaths |
|-----------|------------|------------|-------|--------|
| India | Male | Child   | 10000   | 20      |
| India | Male | Teen | 15000   | 50      |
| India | Male | Adult | 200000   | 10000      |
| India | Female | Child   | 9000   | 15     |
| India | Female | Teen | 12000   | 35     |
| India | Female | Adult | 180000   | 8000     |


## Fictional Covid-19 Data for Canada:

| country   | gender | age_group  | cases | deaths |
|-----------|------------|------------|-------|--------|
| Canada | Male | Child   | 10000   | 20      |
| Canada | Male | Teen | 15000   | 50      |
| Canada | Male | Adult | 200000   | 10000      |
| Canada | Female | Child   | 9000   | 15     |
| Canada | Female | Teen | 12000   | 35     |
| Canada | Female | Adult | 180000   | 8000     |

