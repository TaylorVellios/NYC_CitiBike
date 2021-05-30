# NYC_CitiBike

[See the Tableau Story Here](https://public.tableau.com/shared/BXTBY244J?:display_count=n&:origin=viz_share_link)

# Purpose
To analyze CitiBike bike-share data from NYC (pre-pandemic) using Python and Tableau.</br>
By honing in on key datapoints, we can determine the operational details for expanding this service to other cities.

# Preparation

*To work with interactive plots, please go to the Tableau link above*

While I was asked to convert the Tripduration column to datetime, it became apparent shortly after loading the dataset into Tableau that the original values for this column would still be needed to plot relevant data.</br>
Using Tableau's built in Calculated Field option, I was able to create a second column for Tripduration that contained the number of seconds for every trip on a CitiBike.</br>

![calculated field](https://user-images.githubusercontent.com/14188580/120109073-7aa11c00-c12d-11eb-95ba-3de6b1ae3a3b.PNG)

Similarly, the Gender column contained discrete values of 0, 1, 2 and relating to gender data that needed to be transformed into something more useful.</br>
Using the documentation for the data from CitiBike, an additional Gender column was created to hold the string value of each gender integer</br>

![calc](https://user-images.githubusercontent.com/14188580/120109293-614c9f80-c12e-11eb-8976-da91494787d3.PNG)

# Results

### Starting Dashboard

![1](https://user-images.githubusercontent.com/14188580/120111307-05d2df80-c137-11eb-8709-22912f23b6bf.PNG)

The above image is a dashboard made to highlight a few key datapoints that are answers to the most obvious questions regarding CitiBike usage.</br>
* Total rides
* Distinct number of bikes that were used
* Heatmap showing the most popular days and times of day when bikes are used
* Geographic map showing the spread of starting locations for rides

As can be seen in the heatmap, there is a significant concentration of daily usage from 6a-9a and 4p-8p on weekdays, and 8a-7p on weekends.</br>
Thursday and Friday show much more mid-day usage compared to the first three workdays in the week.</br>
Using this data from an operational standpoint, bike maintenance/cleanup should take place when the fewest number of bikes are in service: from 1am-5am.</br>

The geographic map shows the concentration of rides based on where they begin.</br>
The locations that are the most red indicate the most popular locations for CitiBikes trips to be started.</br>
Grand Central Station is where the deepest red marker is.</br>
Public transportation stations and other high-foot-traffic areas such as parks are the perfect places to consider building stations in other cities.</br>

Now that we know when and where CitiBike services are wanted the most, we will look into the type of people that use these services.</br>

### Trip Times/Days by Gender

![2](https://user-images.githubusercontent.com/14188580/120111813-02405800-c139-11eb-8d8b-b8cc9394dc7a.PNG)

The image above is the same heatmap seen before, but this one split by user gender.</br>
Male and Female day/time usage follows a very similar pattern to what was described above.</br>
Users with an 'unknown' gender in their profile provide a very different picture:
* Usage is primarily on weekends only
* Some additional noteworthy usage in the afternoons of Thursday and Friday

What does this tell us about the majority of "Unknown" gender CitiBike users?

![5](https://user-images.githubusercontent.com/14188580/120111823-07050c00-c139-11eb-956b-019c56f9ef81.PNG)

Diving deeper into the same topic, the above image is showing the bike usage on each day of the week by gender and by usertype.</br>
Usertype only has two different values: Subscriber and Customer.</br>
A "Subscriber" is someone that has purchased an annual membership for the CitiBike service, whereas a "Customer" is someone that has purchased a 24-hour or 72-hour pass.</br>

In the "Customer" row above, the heatmap for "Unknown" gender shows a noticeable similarity to the prior plot, while "Unknown" Subscribers make up too small of a population to be graphed.</br>
From this we can determine that temporary "Customer" accounts:
* Do not feel a need to input their gender when purchasing a pass.
* Are not using CitiBikes to commute to/from work.

### Bike Usage Duration

![3](https://user-images.githubusercontent.com/14188580/120111817-03718500-c139-11eb-9d04-2c789acd6927.PNG)

![4](https://user-images.githubusercontent.com/14188580/120111821-05d3df00-c139-11eb-9330-ad4d3a6000ad.PNG)

Above are plots for all trip durations for the month of march (top), and all trip durations by gender.</br>
Some key takeaways:
* Men are much more likely to use a CitiBike for a 5-minute ride, indicating that this demographic is primarily a point-A to point-B user.
* Women are generally point-A to point-B users but have a much flatter peak topping out at 6-minutes
* Unknown users are nearly just as likely to ride for 10-minutes as they are to ride 25-minutes.

Since we have already determined a large percentage of Unknown users are temporary riders, a concern to keep in mind is that these users are putting 2 to 5 times the wear and tear on the bikes compared to the core demographic of users.</br>
Furthering the theory that most Unknown users are tourists, the flat curve indicates that these users have no specific destination in mind when using CitiBikes.</br>
Since CitiBikes are currently only available in NYC, it would make sense that a majority of Unknown gender users are Customers if they are only in the area for a short time and have no need for an annual pass.

### Start Locations by Gender

![6](https://user-images.githubusercontent.com/14188580/120111829-09fffc80-c139-11eb-8f42-92010e2f919e.PNG)



![6(1)](https://user-images.githubusercontent.com/14188580/120111832-0bc9c000-c139-11eb-9c0b-11229da5497b.PNG)



### Usertype by Gender/Trip Duration by Gender/Usertype

![7](https://user-images.githubusercontent.com/14188580/120111835-0cfaed00-c139-11eb-83d0-d13e74486e92.PNG)


# Summary
