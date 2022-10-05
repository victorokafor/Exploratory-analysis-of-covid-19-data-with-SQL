# Exploratory Analysis of Covid-19 data with SQL

This project was made as one in the series of my portfolio projects.
## Acknowledgements

 - [Our world in Data](https://ourworldindata.com/)
 - [Big Query](https://console.cloud.google.com/bigquery)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Authors

- [Victor Okafor](https://www.linkedin.com/in/victor-okafor-/)


## Let's start
#### Data scrapping
The data set for this project was downloaded from [our world in data](ourworldindata.com)
website and is correct as at 28th September, 2022.


## Metadata 

Data Name: owid-covid-data.csv

File format: csv

File Size: 54 Mb

Number of rows: 219,637 

Number of columns: 67 

## Data cleaning
Upon download, the file of size 54 Mb was first opened with MS Excel.
I assessed the data for integrity and trustworthiness. 
 
The data contained details of Covid-19 cases from 1-1-2020 to 28-9-2022.
After checking with other sources available online, i found the data on this table to be exhaustive and the data source reputable.

#### Processes
* I made a copy of this data as a reference and also as a fallback incase of irrevertibe errors.
* Then i proceeded to profiling the data by carefully going through colums to understand the records they carry and the data types they were stored in. 
* The next step was to split the table and identify the primary key. I achieved this by dividing the table into the 'Deaths' and 'Vaccinations' table. My primary keys were date and country.
* The next step was to upload the tables on Google's Big Query platform. 

## Analysis
View the Deaths Table 

select *

from my-data-project-2244.covid.Deaths

View the Vaccinations table

--select *

--from my-data-project-2244.covid.Vaccinations

* Further test of the deaths table
Select location,
       date,
       total_cases,
       new_cases,
       total_deaths,
       population

from my-data-project-2244.covid.Deaths 

where continent is not null 

order by 1, 2  

### Areas  explored 
* Total cases Vs Total deaths
* Death percentage  in Nigeria
* Likelyhood of dying by contracting Covid-19  in Nigeria
* Percentage of cases to population in your country
* Countries with the highest infection compared to population
* Countries with highest death per Population 
* Break results of deaths by continent
* Most affected continent in terms of death
* Global numbers for new cases and new deaths grouped by dates
* Total global numbers of new deaths, new cases and percentage of deaths compared to number of cases
* Combining the Vaccinations and Deaths table for more insights
* Looking at total Population Vs. Vaccinations
* Create Create
* Create Temp table



