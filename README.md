<h1>COVID19-Data-Exploratory-Analysis</h1>
<h2>About</h2>
<li>The analysis was done to better understand how COVID19 outbreak affected nations of the world</li>
<li>The analysis also helps in understanding trends in the COVID19 pandemic</li>
<h2>Data Source and Structure</h2>
<p>The three datasets used was scraped from <a href = "https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series">CSSEGISandData</a>
<p>The following datasets were used for the analysis</p>
<li><a href = "https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv">Confirmed COVID19 cases (Global)</a></li>
<li><a href = "https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv">Death COVID19 cases (Global)</a></li>
<li><a href = "https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_recovered_global.csv">Survived COVID19 cases (Global)</a></li>
<p>N.B: The datasets are cummulative i.e. values are addded till date</p>
<p>The datasets gets real-time update</p>
<p>The Dashboard consist of 6 Tabs 
  
   ```Analysis``` and ```Dashboard``` are visible while  ```ConsolidatedData```, ```Confirmed```, ```Death``` and ```Recovered``` are hidden

<h2>Analysis Tool</h2>
<pre>Microsoft Excel</pre>

<h2>Data Scraping</h2>
<p>The data was scraped from web in order to get real-time updates using 

  
 ```From web``` option in the ```Get data``` Tab in Microsoft Excel
<p>Click <a href = "https://support.microsoft.com/en-us/office/import-data-from-the-web-b13eed81-33fe-410d-9247-1747269c28e4">here</a> to learn more</p>
  
  <h2>Data Transformation</h2>
  <p>The dataset was transformed accordingly using power query editor. The datasets were then merged togegther to form the 
  
  ```ConsolidatedData``` 
  
  <h2>Pre-Proceesing</h2>
  <p>Since the datasets have cummulative values, in order to get the latest number of <strong>Confirmed</strong> and <strong>Death</strong> cases, 2 new columns were created in <strong>ConsolidatedData</strong> Tab</p>
  
  <p>The following formula was used to get the latest <strong>Confirmed</strong> and <strong>Death</strong> values for each countries, then they were summed up</p>
  
  ```=IF(E2 = (TODAY()-2), F2, "")``` and ```=IF(E2 = (TODAY()-2), G2, "")```
