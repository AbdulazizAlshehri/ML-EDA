
# Exploratory Data Analysis (EDA) Project

This project seeks to answer the analysis questions by Discovering, Cleaning, Preparing, Visualizing the data from three datasets MTA, Taxi, Stations datasets discussed in more details below. The project explaind in six main sections as following:

## 1. ANALYSIS QUESTIONS
1. What patterns people follows in the NYC subway?
2. Relationship between the NYC subway and taxies?

## 2. DATA
Three datasets were used in this analysis, as follows:

1. MTA Dataset:
  provides the basic data about NYC subway turnstyles, e.g. number of entries, number of exits, dataset can be found [here](http://web.mta.info/developers/turnstile.html)
  
  <table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>C/A</th>
      <th>Unit</th>
      <th>Scp</th>
      <th>Station</th>
      <th>Date</th>
      <th>Time</th>
      <th>Entries</th>
      <th>Exits</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A002</td>
      <td>R051</td>
      <td>02-00-00</td>
      <td>LEXINGTON AVE</td>
      <td>12/19/2015</td>
      <td>03:00:00</td>
      <td>5460344</td>
      <td>1843674</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A002</td>
      <td>R051</td>
      <td>02-00-00</td>
      <td>LEXINGTON AVE</td>
      <td>12/19/2015</td>
      <td>07:00:00</td>
      <td>5460357</td>
      <td>1843686</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A002</td>
      <td>R051</td>
      <td>02-00-00</td>
      <td>LEXINGTON AVE</td>
      <td>12/19/2015</td>
      <td>11:00:00</td>
      <td>5460448</td>
      <td>1843797</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A002</td>
      <td>R051</td>
      <td>02-00-00</td>
      <td>LEXINGTON AVE</td>
      <td>12/19/2015</td>
      <td>15:00:00</td>
      <td>5460702</td>
      <td>1843864</td>
    </tr>
    <tr>
      <th>4</th>
      <td>A002</td>
      <td>R051</td>
      <td>02-00-00</td>
      <td>LEXINGTON AVE</td>
      <td>12/19/2015</td>
      <td>19:00:00</td>
      <td>5461157</td>
      <td>1843945</td>
    </tr>
  </tbody>
</table>
</div>

<!-- ![Alt text](/extra/MTA%20Original.png?raw=true "MTA Dataset") -->
  
2. NYC Yellow Taxi dataset: which provide the info about each taxi trip in NYC e.g. pickup location, dropoff location, pickup datetime, datetime dropoff, dataset can be found [here](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
  

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Pickup Datetime</th>
      <th>Dropoff Datetime</th>
      <th>Passenger Count</th>
      <th>Pickup Longitude</th>
      <th>Pickup Latitude</th>
      <th>Dropoff Longitude</th>
      <th>Dropoff Latitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2016-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>2</td>
      <td>-73.990372</td>
      <td>40.734695</td>
      <td>-73.981842</td>
      <td>40.732407</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2016-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>5</td>
      <td>-73.980782</td>
      <td>40.729912</td>
      <td>-73.944473</td>
      <td>40.716679</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2016-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>1</td>
      <td>-73.984550</td>
      <td>40.679565</td>
      <td>-73.950272</td>
      <td>40.788925</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2016-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>1</td>
      <td>-73.993469</td>
      <td>40.718990</td>
      <td>-73.962242</td>
      <td>40.657333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2016-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>3</td>
      <td>-73.960625</td>
      <td>40.781330</td>
      <td>-73.977264</td>
      <td>40.758514</td>
    </tr>
  </tbody>
</table>
</div>

<!-- ![Alt text](/extra/TAXI%20Original.png?raw=true "Taxi Dataset") -->

3. Stations dataset: which provide stations names and locations, we need this dataset inorder to know the location for each turnstyle, dataset can be found [here](https://qri.cloud/nyc-transit-data/turnstiles_station_list)

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Astoria-Ditmars Blvd</td>
      <td>40.775036</td>
      <td>-73.912034</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Astoria Blvd</td>
      <td>40.770258</td>
      <td>-73.917843</td>
    </tr>
    <tr>
      <th>2</th>
      <td>30 Av</td>
      <td>40.766779</td>
      <td>-73.921479</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Broadway</td>
      <td>40.761820</td>
      <td>-73.925508</td>
    </tr>
    <tr>
      <th>4</th>
      <td>36 Av</td>
      <td>40.756804</td>
      <td>-73.929575</td>
    </tr>
  </tbody>
</table>
</div>

<!-- ![Alt text](/extra/STATIONS%20Original.png?raw=true "Stations Dataset") -->

## 3. CLEANING
**MTA Dataset: MTA Wrong Data**
After calculating the daily entries/exits `df_mta['Daily Entries'] = df_mta[['Entries']].diff()`
**MTA Dataset: Off-Duty Turnstyles**
**MTA Dataset: Outliers**
**Taxi Dataset: Zeros & Duplicates**
**Taxi Dataset: LOcations outside NYC**

## 4. PREPERATION


## 5. VISUALIZATION / RESULTS


## 6. CONCLUSION
- MTA and STATIONS datasets joined to get stations locations.
- SATAIONS dataset didn’t require any cleaning.
- Plotting entries/exits shows that Manhattan is the busiest area.
- Plotting entries/exits vs drop-off/pickups show possible spots that have crowded by poeple coming from subway but uncovered by taxi.



This project devoloped to fullfill SDAIA T5 bootcamp requirements. It includes exploring, cleaning, and visualizing data, and making sure its outliers free. This project has a large space of creativity and brining any data set that can be used along with MTA dataset.

