# COSMOS22-Cluster13

## Group 7: Data Analysis
We analyze the data, program the server and communication, process the data, make conclusions & cool models.

### OUR TEAM
* Tanmayi Dasari - @tanmayi2 - rising junior at Cupertino High School
* Sebastian Hazl - @ZopesPrograms - rising junior at the Webb Schools of California 
* Claire Lee - @clairecgl - rising senior at Canyon Crest Academy 
* Alex Miller - @Genos160 - rising senior at Mountain View High School
* Dorothy Zhang - @8Dorothy8 - rising junior at Menlo School

### BRAINSTORMING/PLANNING
During the first week of our 4-week program, our team worked on getting familiar with the project, what changes we would be making to our RC boat, dividing up tasks, learning CAD, and understanding Arduino. Below is a Gantt chart of our last 3 weeks that we created to map out our work. 

<p align="center">
<img src="https://user-images.githubusercontent.com/69954364/182426163-c05a0b1f-ace4-4735-a91f-ec857aa3c06a.png" width="50%"  />
</p>

Additonally, here is our initial brainstorming diagram displaying the flow of data towards the server from the boat/data buoy. This diagram is an overview of Groups 5, 6, and 7. The highlighted blue section on the right is what our team worked on and the formatting at the bottom is what our data looks like.

<p align="center">
<img src="https://user-images.githubusercontent.com/69954364/182431420-dfefae5f-bd22-47db-9a69-b4e65ec98f1d.jpg" width="50%"  />
</p>

### WEEK 2
During the second week, Group 7 learned about database structure using SQLite and created a database to store sensor, GPS, and timestamp data. We also decided on using serial with Group 6 to transfer the data. We started working on transferring the data from serial to the database using Python. The dashboard team decided on Plotly Dash as the library for the dashboard and planned out the layout. Other members started to learn Python to create models and delved into exploratory data analysis and started learning about K-means clustering, linear regression, and goodness of fit for our data analysis. We also set up the server with the Linux OS.

<img align = "left" src="https://user-images.githubusercontent.com/69954364/182485000-e2959fa7-6cc1-4af6-9022-d39418299fca.png" width="58%" style="margin:20px 0px"/>
<img align = "right" src="https://user-images.githubusercontent.com/69954364/182659949-eea206db-a29f-4eb1-8e14-8611bc46806f.jpeg" width="38%" />

$~$

### WEEK 3

We worked on OLS and ANOVA models for data analysis, as well as continuing work on the dashboard. We completed dashboard plot code and tested the live updates on dashboard. Finally, we CADed the radio-to-stand connector of LoRa and server, an esp32 protective box, and LoRa reciever case. On Friday, we went to the Miramar Lake for the final test of our roboboat. We got to see data send to our dashboard and update on refresh!

<p align="center">
  <img src="https://user-images.githubusercontent.com/69954364/182473304-3c8fe707-18ca-4bba-8e96-e721b1e15979.jpg" width="49%"  />
  <img src="https://user-images.githubusercontent.com/69954364/182474054-214cc68a-ca6b-4b52-8d15-42015d050fe6.jpeg" width="49%"  />
</p>
<p align="center">
  <img align="top" src="https://user-images.githubusercontent.com/69954364/182469746-49c51d90-2528-4192-bcd1-7e65fad7d31a.jpeg" width="45%" />
  <img align="top" src="https://user-images.githubusercontent.com/69954364/182478764-6995362e-a6c3-4817-ac1d-281dff6e10d7.jpeg" width="45%" />
</p>

### RESULTS
We cleaned the data to get rid of faulty data, convert the timestamps from a string to datetime, our measurements to floats, and also converted the timestamps to reflect our PDT time. Using the pH from the Data Acquisitions Team, we subtracted 9 from the pH data points to more accurately normalize the pH around the correct pH of 8. We then filtered to only include the datapoint from when the buoy was in the water by only including pH values above 4. We then created and analyzed the data using pairplots, correlation plots, and mapbox. To analyze the goodness of fit, we created a linear regression model, qq plot, and normality test. We found that the Independence Assumption and Normality Assumption, but the Constant of Variance assumption and Mean Zero Assumption did appear to hold. We cleaned the data to ignore the values in this smaller hump to see if that model would be better and ran the test again. The R-squared value went from around 4 to 15 percent, so using the dataset that was cleaned more may be a better model. In the end, however, it was seems that none of our models were ideal for predicting the pH based on temperature and total dissolved solids.

