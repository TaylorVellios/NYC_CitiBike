# NYC_CitiBike

[See the Tableau Story Here](https://public.tableau.com/shared/BXTBY244J?:display_count=n&:origin=viz_share_link)

# Purpose
To analyze CitiBike bike-share data from NYC using Python and Tableau.</br>
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

![1](https://user-images.githubusercontent.com/14188580/120111307-05d2df80-c137-11eb-8709-22912f23b6bf.PNG)

![2](https://user-images.githubusercontent.com/14188580/120111813-02405800-c139-11eb-8d8b-b8cc9394dc7a.PNG)

![3](https://user-images.githubusercontent.com/14188580/120111817-03718500-c139-11eb-9d04-2c789acd6927.PNG)

![4](https://user-images.githubusercontent.com/14188580/120111821-05d3df00-c139-11eb-9330-ad4d3a6000ad.PNG)

![5](https://user-images.githubusercontent.com/14188580/120111823-07050c00-c139-11eb-956b-019c56f9ef81.PNG)

![6](https://user-images.githubusercontent.com/14188580/120111829-09fffc80-c139-11eb-8f42-92010e2f919e.PNG)

![6(1)](https://user-images.githubusercontent.com/14188580/120111832-0bc9c000-c139-11eb-9c0b-11229da5497b.PNG)

![7](https://user-images.githubusercontent.com/14188580/120111835-0cfaed00-c139-11eb-83d0-d13e74486e92.PNG)


# Summary
