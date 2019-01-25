# Exploring Weather Trends

## Table of Contents
<ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#data">Data</a></li>
<li><a href="#assesment">Data Assesment</a></li>
<li><a href="#cleaning">Data Cleaning</a></li>
<li><a href="#visualization">Data Analysis and Visualization</a></li>
</ul>

<a id='data'></a>
## Data

The following SQL queries were used on the database to extract the global data, as well as the GCC countries (Riyadh, Abu Dhabi, Manama, Doha). A .CSV file was downloaded for each query result.

* Global

``` SELECT * FROM global_data; ```

* Riyadh

``` SELECT year, avg_temp FROM city_data WHERE city = 'Riyadh'; ```

* Abu Dhabi

``` SELECT year, avg_temp FROM city_data WHERE city = 'Abu Dhabi'; ```

* Manama

``` SELECT year, avg_temp FROM city_data WHERE city = 'Manama'; ```

* Doha

``` SELECT year, avg_temp FROM city_data WHERE city = 'Doha'; ```



<a id='assesment'></a>
## Data Assesment
The registered temperatures in all cities were between 1843 and 2013. Thus, only this period was studied in the global data.



<a id='cleaning'></a>
## Data Cleaning

1. Filling the missing data with the mean value: I checked for missing values in the data in the previous step using Pandas info(). Riyadh, Abu Dhabi, Manama, and Doha had missing temperature values. Thus, for each city, I’ve filled the missing cells with the mean value.

2. Checking for duplicate data: I've also checked for duplicate data by using Pandas as shown below. However, there were no duplicates found in any of the dataframes.



<a id='visualization'></a>
## Data Analysis and Visualization
1. The **global** average temparature is between 7.97 and 9.56.
2. On the other hand, in the geographically adjacent countries' capitals **Riyadh, Abu Dhabi, Manama,** and **Doha** it's at minimum 23.50 and maximum 28.31.
3. The hottest city is **Doha**, and the least hot is **Riyadh**. However, before 1864 **Abu Dhabi** was hotter than **Doha**.
4. Over time, these cities remian hotter on average compared to the global average.
5. The average temparature of both these cities and the globe, continue to rise over time, i.e. the world is getting hotter.
