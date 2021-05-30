# NYC_CitiBike

[See the Tableau Story Here](https://public.tableau.com/shared/BXTBY244J?:display_count=n&:origin=viz_share_link)

# Purpose
To analyze CitiBike bike-share data from NYC using Python and Tableau.</br>
By honing in on key datapoints, we can determine the operational details for expanding this service to other cities.

# Results

*To work with interactive plots, please go to the Tableau link above*

While I was asked to convert the Tripduration column to datetime, it became apparent shortly after loading the dataset into Tableau that the original values for this column would still be needed to plot relevant data.</br>
Using Tableau's built in Calculated Field option, I was able to create a second column for Tripduration that contained the number of seconds for every trip on a CitiBike.</br>

![calculated field](https://user-images.githubusercontent.com/14188580/120109073-7aa11c00-c12d-11eb-95ba-3de6b1ae3a3b.PNG)

Similarly, the Gender column contained discrete values of 0, 1, 2 and relating to gender data that needed to be transformed into something more useful.</br>
Using the documentation for the data from CitiBike, an additional Gender column was created to hold the string value of each original integer</br>

![calc](https://user-images.githubusercontent.com/14188580/120109293-614c9f80-c12e-11eb-8976-da91494787d3.PNG)
