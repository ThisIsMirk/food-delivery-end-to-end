# food-delivery-end-to-end
Predicting food delivery times based on variables: total distance (km), weather, traffic level, time of day, vehicle type, preparation time (min)

#### Steps taken in this project: 
1. Data exploration
2. Splitting data into train and test
3. Data cleaning
4. Data transformation pipeline creation
5. Training and evaluating models (and creating a pipeline to do so)
6. Hyperparameter tuning
7. Evaluating using test set

### Data Exploration

`.head()` of the dataset. 

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Order_ID</th>
      <th>Distance_km</th>
      <th>Weather</th>
      <th>Traffic_Level</th>
      <th>Time_of_Day</th>
      <th>Vehicle_Type</th>
      <th>Preparation_Time_min</th>
      <th>Courier_Experience_yrs</th>
      <th>Delivery_Time_min</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>522</td>
      <td>7.93</td>
      <td>Windy</td>
      <td>Low</td>
      <td>Afternoon</td>
      <td>Scooter</td>
      <td>12</td>
      <td>1.0</td>
      <td>43</td>
    </tr>
    <tr>
      <th>1</th>
      <td>738</td>
      <td>16.42</td>
      <td>Clear</td>
      <td>Medium</td>
      <td>Evening</td>
      <td>Bike</td>
      <td>20</td>
      <td>2.0</td>
      <td>84</td>
    </tr>
    <tr>
      <th>2</th>
      <td>741</td>
      <td>9.52</td>
      <td>Foggy</td>
      <td>Low</td>
      <td>Night</td>
      <td>Scooter</td>
      <td>28</td>
      <td>1.0</td>
      <td>59</td>
    </tr>
    <tr>
      <th>3</th>
      <td>661</td>
      <td>7.44</td>
      <td>Rainy</td>
      <td>Medium</td>
      <td>Afternoon</td>
      <td>Scooter</td>
      <td>5</td>
      <td>1.0</td>
      <td>37</td>
    </tr>
    <tr>
      <th>4</th>
      <td>412</td>
      <td>19.03</td>
      <td>Clear</td>
      <td>Low</td>
      <td>Morning</td>
      <td>Bike</td>
      <td>16</td>
      <td>5.0</td>
      <td>68</td>
    </tr>
  </tbody>
</table>
</div>

`.info()
Data columns (total 8 columns):
 #   Column                  Non-Null Count  Dtype  
---  ------                  --------------  -----  
 0   Distance_km             1000 non-null   float64
 1   Weather                 970 non-null    object 
 2   Traffic_Level           970 non-null    object 
 3   Time_of_Day             970 non-null    object 
 4   Vehicle_Type            1000 non-null   object 
 5   Preparation_Time_min    1000 non-null   int64  
 6   Courier_Experience_yrs  970 non-null    float64
 7   Delivery_Time_min       1000 non-null   int64  
dtypes: float64(2), int64(2
