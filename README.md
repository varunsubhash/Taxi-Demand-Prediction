# Taxi-Demand-Prediction

# Data Information

Get the data from : http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml (2016 data).
The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC)

## Information on taxis:

<h5> Yellow Taxi: Yellow Medallion Taxicabs</h5>
<p> These are the famous NYC yellow taxis that provide transportation exclusively through street-hails. The number of taxicabs is limited by a finite number of medallions issued by the TLC. You access this mode of transportation by standing in the street and hailing an available taxi with your hand. The pickups are not pre-arranged.</p>

<h5> For Hire Vehicles (FHVs) </h5>
<p> FHV transportation is accessed by a pre-arrangement with a dispatcher or limo company. These FHVs are not permitted to pick up passengers via street hails, as those rides are not considered pre-arranged. </p>

<h5> Green Taxi: Street Hail Livery (SHL) </h5>
<p>  The SHL program will allow livery vehicle owners to license and outfit their vehicles with green borough taxi branding, meters, credit card machines, and ultimately the right to accept street hails in addition to pre-arranged rides. </p>

<h5>Footnote:</h5>
In this solution we are considering only the yellow taxis for the time period between Jan - Mar 2015 & Jan - Mar 2016

# ML Problem Formulation
<p><b> Time-series forecasting and Regression</b></p>
<br>
- To find number of pickups, given location cordinates(latitude and longitude) and time, in the query reigion and surrounding regions.
<p> 
-To solve the above we would be using data collected in Jan - Mar 2015 to predict the pickups in Jan - Mar 2016.
</p>

# Performance metrics
1. Mean Absolute percentage error.
2. Mean Squared error.

## Data Cleaning

In this section we will be doing univariate analysis and removing outlier/illegitimate values which may be caused due to some error

### 1. Pickup Latitude and Pickup Longitude

It is inferred from the source https://www.flickr.com/places/info/2459115 that New York is bounded by the location cordinates(lat,long) - (40.5774, -74.15) & (40.9176,-73.7004) so hence any cordinates not within these cordinates are not considered by us as we are only concerned with pickups which originate within New York.

<b>Observation:-</b> Plotting pickup cordinates which are outside the bounding box of New-York  we will collect all the points outside the bounding box of newyork city to outlier_locationswe can see that there are some points just outside the boundary but there are a few that are in either South america, Mexico or Canada.

### 2. Dropoff Latitude & Dropoff Longitude

It is inferred from the source https://www.flickr.com/places/info/2459115 that New York is bounded by the location cordinates(lat,long) - (40.5774, -74.15) & (40.9176,-73.7004) so hence any cordinates not within these cordinates are not considered by us as we are only concerned with dropoffs which are within New York.

<b>Observation:-</b> The observations here are similar to those obtained while analysing pickup latitude and longitude

 ### 3. Trip Durations:

<p style="font-size:18px">According to NYC Taxi &amp; Limousine Commision Regulations <b style= "color:blue">the maximum allowed trip duration in a 24 hour interval is 12 hours.</b> </p>

<b>Observation:-</b> <br/>
1. We plot box plot to chcek for  the presence of outliers.After plotting it, the presence of outliers are confirmed.<br/>
2. We calculate 0-100th percentile value to find where the outlier lies.<br/>
3. We observe that the outlier lies btween 90-100th percentile.<br/>
4. On further inspection we find that outlier lies  between 99-100th percentile after which it has been removed.<br/>

### 4. Speed:

<b>Observation:-</b> <br/>
1. We plot box plot to chcek for  the presence of outliers.After plotting it, the presence of outliers are confirmed.<br/>
2. We calculate 0-100th percentile value to find where the outlier lies.<br/>
3. We observe that the outlier lies btween 90-100th percentile.<br/>
4. On further inspection we find that outlier lies  between 99.9-100th percentile after which it has been removed.<br/>

<b style='font-size:16px'>The avg speed in Newyork speed is 12.45miles/hr, so a cab driver can travel <font color='blue'> 2 miles per 10min on avg.</font> </b>

### 5. Total Fare:

<b>Observation:-</b> <br/>
1. We plot box plot to chcek for  the presence of outliers.After plotting it, the presence of outliers are confirmed.<br/>
2. We calculate 0-100th percentile value to find where the outlier lies.<br/>
3. We observe that the outlier lies btween 90-100th percentile.<br/>
4. We find that even the 99.9th percentile value doesnt look like an outlier,as there is not much difference between the 99.8th percentile and 99.9th percentile, hence we move on to do graphical analyis.<br/>
5. By plotting the sorted fare vs index grpahs , we come to a conclusion to remove fare above 1000 as those values are extremly high and unrealistic.


