#  Taxi-Demand-Prediction

# Data Information

The data was from : http://www.nyc.gov/html/tlc/html/about/trip_record_data.html (2016 data).
The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC).
These can be found in the data folder in the repositry.

## Information on taxis:

<h5> Yellow Taxi: Yellow Medallion Taxicabs</h5>
<p> These are the famous NYC yellow taxis that provide transportation exclusively through street-hails. The number of taxicabs is limited by a finite number of medallions issued by the TLC. You access this mode of transportation by standing in the street and hailing an available taxi with your hand. The pickups are not pre-arranged.</p>

<h5> For Hire Vehicles (FHVs) </h5>
<p> FHV transportation is accessed by a pre-arrangement with a dispatcher or limo company. These FHVs are not permitted to pick up passengers via street hails, as those rides are not considered pre-arranged. </p>

<h5> Green Taxi: Street Hail Livery (SHL) </h5>
<p>  The SHL program will allow livery vehicle owners to license and outfit their vehicles with green borough taxi branding, meters, credit card machines, and ultimately the right to accept street hails in addition to pre-arranged rides. </p>

<h5>Footnote:</h5>
In this solution we are considering only the yellow taxis for the time period between Jan - Mar 2015 & Jan - Mar 2016


# Data Collection
We Have collected all yellow taxi trips data from jan-2015 to dec-2016(Will be using only 2015 data)
<table>
<tr>
<th> file name </th>
<th> file name size</th>
<th> number of records </th>
<th> number of features </th>
</tr>
<tr>
<td> yellow_tripdata_2016-01 </td>
<td> 1. 59G </td>
<td> 10906858 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-02 </td>
<td> 1. 66G </td>
<td> 11382049 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-03 </td>
<td> 1. 78G </td>
<td> 12210952 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-04 </td>
<td> 1. 74G </td>
<td> 11934338 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-05 </td>
<td> 1. 73G </td>
<td> 11836853 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-06 </td>
<td> 1. 62G </td>
<td> 11135470 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-07 </td>
<td> 884Mb </td>
<td> 10294080 </td>
<td> 17 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-08 </td>
<td> 854Mb </td>
<td> 9942263 </td>
<td> 17 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-09 </td>
<td> 870Mb </td>
<td> 10116018 </td>
<td> 17 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-10 </td>
<td> 933Mb </td>
<td> 10854626 </td>
<td> 17 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-11 </td>
<td> 868Mb </td>
<td> 10102128 </td>
<td> 17 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-12 </td>
<td> 897Mb </td>
<td> 10449408 </td>
<td> 17 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-01 </td>
<td> 1.84Gb </td>
<td> 12748986 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-02 </td>
<td> 1.81Gb </td>
<td> 12450521 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-03 </td>
<td> 1.94Gb </td>
<td> 13351609 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-04 </td>
<td> 1.90Gb </td>
<td> 13071789 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-05 </td>
<td> 1.91Gb </td>
<td> 13158262 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-06 </td>
<td> 1.79Gb </td>
<td> 12324935 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-07 </td>
<td> 1.68Gb </td>
<td> 11562783 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-08 </td>
<td> 1.62Gb </td>
<td> 11130304 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-09 </td>
<td> 1.63Gb </td>
<td> 11225063 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-10 </td>
<td> 1.79Gb </td>
<td> 12315488 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-11 </td>
<td> 1.65Gb </td>
<td> 11312676 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-12 </td>
<td> 1.67Gb </td>
<td> 11460573 </td>
<td> 19 </td>
</tr>
</table>


<tr>
		<td>Dropoff_longitude</td>
		<td>Longitude where the meter was disengaged.</td>
	</tr>
	<tr>
		<td>Dropoff_ latitude</td>
		<td>Latitude where the meter was disengaged.</td>
	</tr>
	<tr>
		<td>Payment_type</td>
		<td>A numeric code signifying how the passenger paid for the trip.
		<ol>
			<li> Credit card </li>
			<li> Cash </li>
			<li> No charge </li>
			<li> Dispute</li>
			<li> Unknown </li>
			<li> Voided trip</li>
		</ol>
		</td>
	</tr>
	<tr>
		<td>Fare_amount</td>
		<td>The time-and-distance fare calculated by the meter.</td>
	</tr>
	<tr>
		<td>Extra</td>
		<td>Miscellaneous extras and surcharges. Currently, this only includes. the $0.50 and $1 rush hour and overnight charges.</td>
	</tr>
	<tr>
		<td>MTA_tax</td>
		<td>0.50 MTA tax that is automatically triggered based on the metered rate in use.</td>
	</tr>
	<tr>
		<td>Improvement_surcharge</td>
		<td>0.30 improvement surcharge assessed trips at the flag drop. the improvement surcharge began being levied in 2015.</td>
	</tr>
	<tr>
		<td>Tip_amount</td>
		<td>Tip amount – This field is automatically populated for credit card tips.Cash tips are not included.</td>
	</tr>
	<tr>
		<td>Tolls_amount</td>
		<td>Total amount of all tolls paid in trip.</td>
	</tr>
	<tr>
		<td>Total_amount</td>
		<td>The total amount charged to passengers. Does not include cash tips.</td>
	</tr>

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

## Remove all outliers/erronous points.

### Removing outliers in the month of Jan-2015

Number of pickup records =  12748986.<br/>
Number of outlier coordinates lying outside NY boundaries: 293919.<br/>
Number of outliers from trip times analysis: 23889.<br/>
Number of outliers from trip distance analysis: 92597.<br/>
Number of outliers from speed analysis: 24473.<br/>
Number of outliers from fare analysis: 5275.<br/>
Total outliers removed 377910.<br/>

fraction of data points that remain after removing outliers 0.9703576425607495

# Data-preperation
## Clustering/Segmentation
- trying different cluster sizes to choose the right K in K-means.<br/>
- We need to choose number of clusters so that, there are more number of cluster regions.<br/>
- That are close to any cluster center.<br/>
- Make sure that the minimum inter cluster should not be very less.<br/>

### Inference:
- The main objective was to find a optimal min. distance(Which roughly estimates to the radius of a cluster) between the clusters which we got was 40.

## Time-binning:
- We use 10 minute bins.<br/>
- We add two more columns 'pickup_cluster'(to which cluster it belogns to) and 'pickup_bins' (to which 10min intravel the trip belongs to)<br/>.

## Data cleaning on the remaining data:

- Till now we cleaned data and prepared data for the months of 2015 and now to do the same operations for months Jan, Feb, March of 2016 we need to do the below steps.<br/>
 1. get the dataframe which inlcudes only required colums.<br/>
 2. adding trip times, speed, unix time stamp of pickup_time.<br/>
 3. remove the outliers based on trip_times, speed, trip_duration, total_amount.<br/>
 4. add pickup_cluster to each data point.<br/>
 5. add pickup_bin (index of 10min intravel to which that trip belongs to).<br/>
 6. group by data, based on 'pickup_cluster' and 'pickup_bin'.<br/>

- Below are the results of the data cleaning.<br/>
  Return with trip times...<br/>
  Remove outliers...<br/>
  Number of pickup records =  10906858.<br/>
  Number of outlier coordinates lying outside NY boundaries: 214677.<br/>
  Number of outliers from trip times analysis: 27190.<br/>
  Number of outliers from trip distance analysis: 79742.<br/>
  Number of outliers from speed analysis: 21047.<br/>
  Number of outliers from fare analysis: 4991.<br/>
  Total outliers removed 297784.<br/>

  Estimating clusters...<br/>
  Final groupbying...<br/>
  Return with trip times...<br/>
  Remove outliers...<br/>
  Number of pickup records =  11382049.<br/>
  Number of outlier coordinates lying outside NY boundaries: 223161.<br/>
  Number of outliers from trip times analysis: 27670.<br/>
  Number of outliers from trip distance analysis: 81902.<br/>
  Number of outliers from speed analysis: 22437.<br/>
  Number of outliers from fare analysis: 5476.<br/>
  Total outliers removed 308177.<br/>

  Estimating clusters...<br/>
  Final groupbying...<br/>
  Return with trip times...<br/>
  Remove outliers...<br/>
  Number of pickup records =  12210952.<br/>
  Number of outlier coordinates lying outside NY boundaries: 232444.<br/>
  Number of outliers from trip times analysis: 30868.<br/>
  Number of outliers from trip distance analysis: 87318.<br/>
  Number of outliers from speed analysis: 23889.<br/>
  Number of outliers from fare analysis: 5859.<br/>
  Total outliers removed 324635.<br/>

## Smoothing

- We get the unique bins where pickup values are present for each each reigion.<br/>
- For each cluster region we will collect all the indices of 10min intravels in which the pickups are happened and  we got an observation that there are some pickpbins that doesnt have any pickups.<br/>
- For every month we get all indices of 10min intravels in which atleast one pickup got happened.<br/>

- There are two ways to fill up these values.<br>
  1. Fill the missing value with 0's</li>
  2. Fill the missing values with the avg values.<br> 
     Case 1: (values missing at the start).<br>
     Case 2: (values missing in middle).<br>

- We fill a value of zero for every bin where no pickup data is present.<br> 
- The count_values: number pickps that are happened in each region for each 10min intervel.It wont have be any value if there are no     picksups.<br>
- For every 10min intravel(pickup_bin) we will check it is there in our unique bin.<br>
- If it is there we will add the count_values[index] to smoothed data,if not we add 0 to the smoothed data.<br>
- We finally return smoothed data.<br>
