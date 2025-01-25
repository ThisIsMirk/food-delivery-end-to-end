# food-delivery-end-to-end
Predicting food delivery times based on variables: total distance (km), weather, traffic level, time of day, vehicle type, preparation time (min)

#### Steps taken in this project: 
1. Data exploration
2. Data cleaning
3. Data transformation pipeline creation
4. Training and evaluating models (and creating a pipeline to do so)
5. Hyperparameter tuning
6. Evaluating using test set

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

`.info()` shows us there are missing values to deal with, both categorical and numerical. 

![image](https://github.com/user-attachments/assets/517d9f24-770f-4413-bed3-e7daca85f7a2)

Visualization correlation between variable and target using a scatter plot matrix. We see a strong correlation between Distance_km and Delivery_Time_min (target variable) and a weaker but still noticeable correlation with Preparation_Time_min.

![image](https://github.com/user-attachments/assets/c0b2179d-a085-4ffd-bffb-e96442e3b612)







