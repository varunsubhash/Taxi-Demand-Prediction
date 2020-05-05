#  Taxi-Demand-Prediction
- The man objective is to predict the number of pickup points for each region as accuratley as possible.

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


# Features in the data set

- VendorId -- A code indicating the TPEP provider that provided the record.<br/>
               1.Creative Mobile<br/>
	       2.TechnologieseriFone Inc<br/>
- tpep_pickup_datetime --The date and time when the meter was engaged.<br/>
- tpep_dropoff_datetime --The date and time when the meter was disengaged.<br/>
- Passenger_count --The number of passengers in the vehicle. This is a driver-entered value.<br/>
- Trip_distance --The elapsed trip distance in miles reported by the taximeter.<br/>
- Pickup_longitude --Longitude where the meter was engaged.<br/>
- Pickup_latitude --Latitude where the meter was engaged.<br/>
- RateCodeID -- The final rate code in effect at the end of the trip.<br/>
              1.Standard rate<br/>
              2.JFK<br/>
              3.Newark<br/>
              4.Nassau or Westchester<br/>
              5.Negotiated fare<br/>
              6.Group ride<br/>
- Store_and_fwd_flag --This flag indicates whether the trip record was held in vehicle memory before sending to the vendor,
aka “store and forward,” because the vehicle did not have a connection to the server.<br/>
             Y= store and forward trip<br/>
             N= not a store and forward trip<br/>


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

-It is inferred from the source https://www.flickr.com/places/info/2459115 that New York is bounded by the location cordinates(lat,long) - (40.5774, -74.15) & (40.9176,-73.7004) so hence any cordinates not within these cordinates are not considered by us as we are only concerned with pickups which originate within New York.

<b>Observation:-</b> Plotting pickup cordinates which are outside the bounding box of New-York  we will collect all the points outside the bounding box of newyork city to outlier_locations we can see that there are some points just outside the boundary but there are a few that are in either South america, Mexico or Canada.

### 2. Dropoff Latitude & Dropoff Longitude

It is inferred from the source https://www.flickr.com/places/info/2459115 that New York is bounded by the location cordinates(lat,long) - (40.5774, -74.15) & (40.9176,-73.7004) so hence any cordinates not within these cordinates are not considered by us as we are only concerned with dropoffs which are within New York.

<b>Observation:-</b> The observations here are similar to those obtained while analysing pickup latitude and longitude. <br/>

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
- Trying different cluster sizes to choose the right K in K-means.<br/>
- We need to choose number of clusters so that, there are more number of cluster regions that are close to any cluster center.<br/>
- Make sure that the minimum inter cluster distance be between 0.5 to 2 miles.<br/>
- Make sure that the minimum inter cluster distance be between 0.5 to 2 miles.<br/>
- On writing a functions to find the minimum cluster distance for different size of clusters we get the below results.

   - On choosing a cluster size of  10 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 2.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 8.0 <br/>
   - Min inter-cluster distance =  1.0933194607372518 <br/>
---
   - On choosing a cluster size of  20 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 4.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 16.0 <br/>
   - Min inter-cluster distance =  0.7123318236197774 <br/>
---
   - On choosing a cluster size of  30 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 8.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 22.0 <br/>
   - Min inter-cluster distance =  0.5179286172497254 <br/>
---
   - On choosing a cluster size of  40 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 9.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 31.0 <br/>
   - Min inter-cluster distance =  0.5064095487015858 <br/>
---
   - On choosing a cluster size of  50 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 12.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 38.0 <br/>
   - Min inter-cluster distance =  0.36495419250817024 <br/>
---
   - On choosing a cluster size of  60 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 14.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 46.0 <br/>
   - Min inter-cluster distance =  0.346654501371586 <br/>
---
   - On choosing a cluster size of  70 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 16.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 54.0 <br/>
   - Min inter-cluster distance =  0.30468071844965394 <br/>
---
   - On choosing a cluster size of  80 <br/>
   - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 18.0 <br/>
   - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 62.0 <br/>
   - Min inter-cluster distance =  0.29187627608454664 <br/>
---
  - On choosing a cluster size of  90 
  - Avg. Number of Clusters within the vicinity (i.e. intercluster-distance < 2): 21.0 <br/>
  - Avg. Number of Clusters outside the vicinity (i.e. intercluster-distance > 2): 69.0 <br/>
  - Min inter-cluster distance =  0.18237562550345013 <br/>

### Inference:
- The main objective was to find a optimal min. distance(Which roughly estimates to the radius of a cluster) between the clusters which we got was 40.

## Time-binning:
- We use 10 minute bins.<br/>
- Using unix time stamp makes it easier to create bins.<br/>
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

- When you are using smoothing we are looking at the future number of pickups which might cause a data leakage.<br>

- So we use smoothing for jan 2015th data since it acts as our training data.<br>
- And we use simple fill_misssing method for 2016th data.<br>

## Modelling: Baseline Models

Now we get into modelling in order to forecast the pickup densities for the months of Jan, Feb and March of 2016 for which we are using multiple models with two variations 
1. Using Ratios of the 2016 data to the 2015 data.
2. Using Previous known values of the 2016 data itself to predict the future values

### Simple Moving Averages
- The First Model used is the Moving Averages Model which uses the previous n values in order to predict the next value <br>

- Using Ratio Values - R_{t} = ( R_{t-1} + R_{t-2} + R_{t-3} .... R_{t-n} )/n .<br>

- For the above the Hyperparameter is the window-size (n) which is tuned manually and it is found that the window-size of 3 is optimal for getting the best results using Moving Averages using previous Ratio values therefore we get R_{t} = ( R_{t-1} + R_{t-2} + R_{t-3})/3 .<br>

- Next we use the Moving averages of the 2016  values itself to predict the future value using P_{t} = ( P_{t-1} + P_{t-2} + P_{t-3} .... P_{t-n} )/n .<br>

- For the above the Hyperparameter is the window-size (n) which is tuned manually and it is found that the window-size of 1 is optimal for getting the best results using Moving Averages using previous 2016 values therefore we get P_{t} = P_{t-1} .<br>

### Weighted Moving Averages
The Moving Avergaes Model used gave equal importance to all the values in the window used, but we know intuitively that the future is more likely to be similar to the latest values and less similar to the older values. Weighted Averages converts this analogy into a mathematical relationship giving the highest weight while computing the averages to the latest previous value and decreasing weights to the subsequent older ones.<br>

- Weighted Moving Averages using Ratio Values - R_{t} = ( N*R_{t-1} + (N-1)*R_{t-2} + (N-2)*R_{t-3} .... 1*R_{t-n} )/(N*(N+1)/2)<br>.

- For the above the Hyperparameter is the window-size (n) which is tuned manually and it is found that the window-size of 5 is optimal for getting the best results using Weighted Moving Averages using previous Ratio values therefore we get  R_{t} = ( 5*R_{t-1} + 4*R_{t-2} + 3*R_{t-3} + 2*R_{t-4} + R_{t-5} )/15 <br>.

- Weighted Moving Averages using Previous 2016 Values - P_{t} = ( N*P_{t-1} + (N-1)*P_{t-2} + (N-2)*P_{t-3} .... 1*P_{t-n} )/(N*(N+1)/2)<br>.

- For the above the Hyperparameter is the window-size (n) which is tuned manually and it is found that the window-size of 2 is optimal for getting the best results using Weighted Moving Averages using previous 2016 values therefore we get P_{t} = ( 2*P_{t-1} + P_{t-2} )/3 <br>

### Exponential  Weighted Moving Averages
Through weighted averaged we have satisfied the analogy of giving higher weights to the latest value and decreasing weights to the subsequent ones but we still do not know which is the correct weighting scheme as there are infinetly many possibilities in which we can assign weights in a non-increasing order and tune the the hyperparameter window-size. To simplify this process we use Exponential Moving Averages which is a more logical way towards assigning weights and at the same time also using an optimal window-size.<br>

In exponential moving averages we use a single hyperparameter alpha which is a value between 0 & 1 and based on the value of the hyperparameter alpha the weights and the window sizes are configured.<br>
For eg. If alpha=0.9\ then the number of days on which the value of the current iteration is based is 1/(1-\alpha)=10i.e. we consider values 10 days prior before we predict the value for the current iteration. Also the weights are assigned using 2/(N+1)=0.18 ,where N = number of prior values being considered, hence from this it is implied that the first or latest value is assigned a weight of 0.18 which keeps exponentially decreasing for the subsequent values.<br>

R^{'}_{t} = \alpha*R_{t-1} + (1-\alpha)*R^{'}_{t-1}  .<br>

P^{'}_{t} = \alpha*P_{t-1} + (1-\alpha)*P^{'}_{t-1} <br>.

## Comparison between baseline models
We have chosen our error metric for comparison between models as <b>MAPE (Mean Absolute Percentage Error)</b> so that we can know that on an average how good is our model with predictions and <b>MSE (Mean Squared Error)</b> is also used so that we have a clearer understanding as to how well our forecasting model performs with outliers so that we make sure that there is not much of a error margin between our prediction and the actual value.<br>.

 Error Metric Matrix (Forecasting Methods) - MAPE & MSE
--------------------------------------------------------------------------------------------------------
- Moving Averages (Ratios) -                             MAPE:  0.182115517339       MSE:  400.0625504032258<br>
- Moving Averages (2016 Values) -                        MAPE:  0.14292849687        MSE:  174.84901993727598<br>
--------------------------------------------------------------------------------------------------------
- Weighted Moving Averages (Ratios) -                    MAPE:  0.178486925438       MSE:  384.01578741039424<br>
- Weighted Moving Averages (2016 Values) -               MAPE:  0.135510884362       MSE:  162.46707549283155<br>
--------------------------------------------------------------------------------------------------------
- Exponential Moving Averages (Ratios) -              MAPE:  0.177835501949       MSE:  378.34610215053766<br>
- Exponential Moving Averages (2016 Values) -         MAPE:  0.135091526367       MSE:  159.73614471326164<br>
- From the above matrix it is inferred that the best forecasting model for our prediction would be:- 𝑃′𝑡=𝛼∗𝑃𝑡−1+(1−𝛼)∗𝑃′𝑡−1 i.e Exponential Moving Averages using 2016 Values.<br>

## Regression Models

### Train-Test Split
Before we start predictions using the tree based regression models we take 3 months of 2016 pickup data and split it such that for every region we have 70% data in train and 30% in test, ordered date-wise for every region.<br>


### Using Random Forest Regressor
- Training a hyper-parameter tuned random forest regressor on our train data.<br>
- Predicting on test data using our trained random forest model.<br> 
- The models regr1 is already hyper parameter tuned.<br>
- The parameters that we got above are found using grid search.<br>
- Feature importances based on analysis using random forest.<br>
   - Index(['ft_5', 'ft_4', 'ft_3', 'ft_2', 'ft_1', 'lat', 'lon', 'weekday',
       'exp_avg'],
      dtype='object')
[ 0.00477243  0.07614745  0.14289548  0.1857027   0.23859285  0.00227886
  0.00261956  0.00162121  0.34536947]
  
### Using XgBoost Regressor.
- Training a hyper-parameter tuned Xg-Boost regressor on our train data.<br>
- Predicting with our trained Xg-Boost regressor.<br>
- The models x_model is already hyper parameter tuned.<br>
- The parameters that we got above are found using grid search.<br>
- Feature importances.<br>
  {'exp_avg': 806,
 'ft_1': 1008,
 'ft_2': 1016,
 'ft_3': 863,
 'ft_4': 746,
 'ft_5': 1053,
 'lat': 602,
 'lon': 612,
 'weekday': 195}
 
 
 ### Calculating the error metric values for various models
 
 - Error Metric Matrix (Tree Based Regression Methods) -  MAPE
--------------------------------------------------------------------------------------------------------
- Baseline Model -                             Train:  0.140052758787       Test:  0.136531257048.<br>
- Exponential Averages Forecasting -           Train:  0.13289968436       Test:  0.129361804204.<br>
- Linear Regression -                         Train:  0.13331572016       Test:  0.129120299401.<br>
- Random Forest Regression -                   Train:  0.0918514693197      Test:  0.127141622928.<br>
- Error Metric Matrix (Tree Based Regression Methods) -  MAPE.<br>
--------------------------------------------------------------------------------------------------------
- Baseline Model -                             Train:  0.140052758787       Test:  0.136531257048.<br>
- Exponential Averages Forecasting -           Train:  0.13289968436       Test:  0.129361804204.<br>
- Linear Regression -                         Train:  0.13331572016       Test:  0.129120299401.<br>
- Random Forest Regression -                   Train:  0.0917619544199      Test:  0.127244647137.<br>
- XgBoost Regression -                         Train:  0.129387355679       Test:  0.126861699078.<br>
