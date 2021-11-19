
# Exploratory Data Analysis (EDA) Project

This project seeks to answer the analysis questions by Discovering, Cleaning, Preparing, nad Visualizing the data from the three datasets MTA, Taxi, and Stations datasets discussed in details below. The project explaind in five main sections as following:

## 1. ANALYSIS QUESTIONS
- What patterns people follows in the NYC subway?
- Relationship between the NYC subway and taxies?

## 2. DATA
Three datasets were used in this analysis, for each dataset we selected only columns we are interested in, as following:

### 1. MTA Dataset [source](http://web.mta.info/developers/turnstile.html): 
provides the basic data about NYC subway turnstyles, e.g. number of entries (cumulative), number of exits (cumulative)
  
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


### 2. NYC Yellow Taxi dataset [source](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page): 
which provide the info about each taxi trip in NYC e.g. pickup location, dropoff location, pickup datetime, datetime dropoff, dataset can be found 
  

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

### 3. Stations dataset [source](https://qri.cloud/nyc-transit-data/turnstiles_station_list):
which provide stations' names and locations, we need this dataset inorder to know the location for each turnstyle, dataset preview:

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

## 3. CLEANING
### MTA Dataset (Wrong Data):

Scince the provided entries/exits data are comulative values (i.e. each observation represent the total number of entries/exits until observation time) we need to calculate daily entries/exits, for that we ordered the observations by datetime so that we can calculate the daily entries/exits by subtracting each observation with the previouse one, see the following code snippet `df_mta['Daily Entries'] = df_mta[['Entries']].diff()`. After calculating the daily entries and daily exits by subtracting, wrong values appeared in columns *daily_entries* and *daily_exits* science some rows are subtracted from the previouse rows that don't belong to the same turnstyle or/and same day as the first row, these rows with the wrong data were removed, see row with index 252 in the following table:

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Turn_ID</th>
      <th>Date</th>
      <th>Time</th>
      <th>Station</th>
      <th>Entries</th>
      <th>Exits</th>
      <th>Daily Entries</th>
      <th>Daily Exits</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>251</th>
      <td>A002R05102-00-0059 st</td>
      <td>2016-02-05</td>
      <td>23:00:00</td>
      <td>59 ST</td>
      <td>5530780</td>
      <td>1867104</td>
      <td>345.0</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>252</th>
      <td>A002R05102-00-00lexington ave</td>
      <td>2015-12-19</td>
      <td>03:00:00</td>
      <td>LEXINGTON AVE</td>
      <td>5460344</td>
      <td>1843674</td>
      <td>-70436.0</td>
      <td>-23430.0</td>
    </tr>
  </tbody>
</table>


### MTA Dataset (Off-Duty Turnstyles):
157229 rows founded with no change in entries and exits, see the following table:

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Turn_ID</th>
      <th>Date</th>
      <th>Time</th>
      <th>Station</th>
      <th>Entries</th>
      <th>Exits</th>
      <th>Daily Entries</th>
      <th>Daily Exits</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2627</th>
      <td>A002R05102-05-0059 st</td>
      <td>2015-12-26</td>
      <td>07:00:00</td>
      <td>59 ST</td>
      <td>1239</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2628</th>
      <td>A002R05102-05-0059 st</td>
      <td>2015-12-26</td>
      <td>11:00:00</td>
      <td>59 ST</td>
      <td>1239</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2629</th>
      <td>A002R05102-05-0059 st</td>
      <td>2015-12-26</td>
      <td>15:00:00</td>
      <td>59 ST</td>
      <td>1239</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2630</th>
      <td>A002R05102-05-0059 st</td>
      <td>2015-12-26</td>
      <td>19:00:00</td>
      <td>59 ST</td>
      <td>1239</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2631</th>
      <td>A002R05102-05-0059 st</td>
      <td>2015-12-26</td>
      <td>23:00:00</td>
      <td>59 ST</td>
      <td>1239</td>
      <td>0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>

### MTA Dataset (Outliers): 

outliers </br>
![alt text](/extra/MTA%20Outliers%20before.png "Outliers")

outliers removed </br>
![alt text](/extra/MTA%20Outliers%20after.png "Outliers Removed")


### Taxi Dataset (Missing values & Duplicates):
Moving to **Taxi dataset** some observations have missing  pickup and/or drop-off coordinates equal to zeros (missing), see the following table: </br>

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
      <th>38</th>
      <td>2016-01-01 00:00:19</td>
      <td>2016-01-01 00:19:33</td>
      <td>1</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>67</th>
      <td>2016-01-01 00:00:41</td>
      <td>2016-01-01 00:00:46</td>
      <td>5</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>150</th>
      <td>2016-01-01 00:01:34</td>
      <td>2016-01-01 00:15:38</td>
      <td>1</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>156</th>
      <td>2016-01-01 00:01:36</td>
      <td>2016-01-01 00:20:36</td>
      <td>1</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>158</th>
      <td>2016-01-01 00:01:37</td>
      <td>2016-01-01 00:25:25</td>
      <td>2</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
 </br>
 
 and found some duplicated rows, see the following table example: </br>
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
      <th>1773</th>
      <td>2016-01-02 00:50:32</td>
      <td>2016-01-02 00:51:16</td>
      <td>1</td>
      <td>-73.825645</td>
      <td>40.712231</td>
      <td>-73.83033</td>
      <td>40.714161</td>
    </tr>
    <tr>
      <th>1774</th>
      <td>2016-01-02 00:50:32</td>
      <td>2016-01-02 00:51:16</td>
      <td>1</td>
      <td>-73.825645</td>
      <td>40.712231</td>
      <td>-73.83033</td>
      <td>40.714161</td>
    </tr>
  </tbody>
</table>
 
 
### Taxi Dataset (Locations outside NYC):
According to [source](https://data.cityofnewyork.us/Transportation/NYC-Taxi-Zones/d3c5-ddgc) NYC is located between (40.496115395170364, -74.25559136315209) and (40.91553277700258, -73.7000090639354), so we removed all observations that have pickup or drop-off coordinates located outside these boundaries.
</br> 
observations with pickup or dropoff coordinates located outside NYC boundaries
</br>
![alt text](/extra/TAXI%20Wrong%20coord.png "Wrong coordinates")


## 4. VISUALIZATION (RESULTS)
By plotting MTA subway entries `plotly.express.scatter(df_mta_with_locations_uni, x="Longitude", y="Latitude", size="DailyEntries")` we can see the most crowded stations since each circle represent a subway station and size of the circle represent the total number of entries/exits in that stations, see the following graph: </br>

![alt text](/Output%20Screenshots/SUBWAY%20Entries%20with%20locations.png "Subway Stations")

</br>

Comparing daily subway exits with taxi pickups we can see the areas where there is a lot of poeple exiting subwway while there is much lesser or non taxi pickups, which indicate that either these poeple exiting to thier homes directly or there is a chance these areas need to be considered by taxies to cover, see the following gragh:

![alt text](/extra/Subway%20Exits%20vs%20Taxi%20Pickups.png "Subway Stations")


## 5. CONCLUSION
- MTA and STATIONS datasets joined to get stations locations.
- SATAIONS dataset didn’t require any cleaning.
- Plotting entries/exits shows that Manhattan is the busiest area.
- Plotting entries/exits vs drop-off/pickups show possible spots that have crowded by poeple coming from subway but uncovered by taxi.

</br>
This project (EDA Project) was done to fullfill SDAIA T5 bootcamp requirements.

by [Abdulaziz](https://github.com/AbdulazizAlshehri)

