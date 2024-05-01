Zackery Anderson <br>
Math 3080 <br>
Final Project

# Earthquake Predictions

My final project I decided to try and predict the magnitude of Earthquakes at certain latitude and longitude. The data set I found from Kraggle was labeled Significant Earthquake Dataset 1900-2023 that you can find in my project or at https://www.kaggle.com/datasets/jahaidulislam/significant-earthquake-dataset-1900-2023.<br>

The data set that I selected has information about Earthquakes ranging from the years 1900 to 2023 and shows the time, place, depth, magnitude and several other information.<br>

When I loaded the data I first checked for any values that didn't exist and there was quite a bit of data that didn't have any information. Much of the missing data were all in similar columns that I didn't need for my objective so I just ended up dropping those columns. There was some data in the depth column that didn't have any information and since I didn't know if depth was needed for my analysis I had to figure out what to do with that data. <br>

Since the location data was valid I went and found the latitude and longitude for the missing data and from what I could tell it was an Earthquake that happened in the ocean. Since I didn't know what depth the Earthquake happened in the oceans I just set the missing values to 0.<br>

After the data was cleared of missing values I then went to see if there was any correlations with the data that was left. There was a strong correletion with latitude and longitude but the other data that had a slight correlation was the magnitude with both latitude and longitude. I then create graphs to see if the correlation was worth diving into more and there was some hope for it. <br>

After figuring out the data I wanted to use I decided I was going to use a linear regression model to try and predict the magnitude at a certain latitude and longitude. I know basically I was doing a multilinear regression but I used my linear regression method that I created from a past assignment and made some modification. I got the linear regression model for both latitude and longitude and combined them together to try and predict the magnitude and returned the results. <br>

After I had finished with the prediction I did an evaluation of the predicted value with the actual value. The results of the evaluation are the following.

- Mean Absolute Error (MAE): 0.34
- Mean Squared Error (MSE): 0.21
- Root Mean Squared Error (RMSE): 0.45
- R-squared (R2): 0.00
- Median Absolute Error (MedAE): 0.32

As you can see the models average predition is pretty close to the original values since MAE and MSE were relatively low. However the R-squared value being 0 means that the model doesn't really explain the variance of the magnitude very well so it means the relation isn't really captured the best.<br>

So just for fun I wanted to see what magnitude Earthquake would be predicted for Snow College. I went and created a new data frame with the latitude and longitude values for Snow College and ran that data frame through my predict method. The result for the magnitude prediction at Snow College is 5.947526. What this means is if an Earthquake were to happen at Snow College we would probably get about a 6.0 magnitude. <br>

The Last part of my final project is a interactive map that shows the locations of each Earthquake and shows the original magnitude and the predicted magnitude.