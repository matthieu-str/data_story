<p align="justify">Being able to identify the predominant human fluxes and mobility patterns in the world is crucial for effectively modelling the spreading of diseases, establishing effective mobility connections and understanding the travelling habits of different populations. This project extension continues the exploration of human geographic movement by relating the latitude and longitude coordinates of check-ins (to the Gowalla and Brightkite social networks) to the respective countries where the localization took place. This is done with the purpose of investigating human migration patterns within and among countries. We are looking for eventual correlation between the users’ home location and their travelling destinations, possibly identifying what are the most frequent connections among countries.</p>

# The main questions we asked ourselves

1. What are the main fluxes of people over the world ?
2. Have some countries different trips habits than others ?
3. What is the influence of factors like the language, the distance or the GDP on travlling habits ? 

# What was our input data ? 

We were given several millions of check-ins and the friendship network coming from two social networks : Brightkite and Gowalla. 

Here's a summary of this data :


Social network | Number of check-ins | Number of users | Number of countries and places | Number of nodes | Number of edges | Date of collection
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
Brightkite | 4 491 035 | 50 686 | 242 | 58 228 | 214 078 | April 2008 - October 2010
Gowalla | 6 442 728 | 107 069 | 196 | 196 591 | 950 327 | February 2009 - October 2010

You can see the distribution of these millions over the planet right there : 
![Check-ins map](/images/checkins_map.jpeg)

# How do we shaped this data ? 

## 1. Finding user's home

At the beginng, the only thing we had was a huge amount of check-ins. Before everything else, we had to define a house for each user, in order to know its nationality and the distances that the users travel when they leave their home. 

To achieve this, we divided the all world into 25 km x 25 km cells. The home location of a user was the average location of his or her check-ins, within the cell into which he or she had the more check-ins. 

You can see here the distribution of home location over the world :

*Add the picture*

Once this was done, we were able to give a nationality to each user. 

## 2. Geographical boundaries of our study 

<p align="justify">As you can see on the distribution of check-ins and home locations, these lasts are not equally distributed on earth. These two social networks are more popular in the US and some European countries. Therefore, we had to set on threshold to apply our study only in places where we had enough data. 
In this analysis, we only kept the countries in which at leat 1 person over 100 000 was a user for both social networks.</p> 
The selected countries are represented on this map :

*Add the picture*

# Results 

## 1. Comparison between United-States and Europe 

<p align="justify">For each check-in, we could compute the distance between the user's location while checking in and his or her home location. Therefore, we have been able to compute various kind of statistics. Given the geographical boundaries of our stidues, we have chosen to compare the US and the average results of European countries that are part of the study (namely Europe in what follows).</p> 

Moreover, as we are only interested in travelling habits, the following statistics are based on check-ins that were done at a distance from home greater than 200 km, which is how we define a travel. 

Here are the results : 

<p align="justify">Please note that in order not to account twice some users that could use both Brightkite and Gowalla, we will always present you the results for both of them separately and analyse the similarities and differences between these two.</p> 

The following figure shows how far from their home are people when they leave their country. 

![Distance EU vs US](/images/distance_eu_vs_us.png)

You can see that American people go much further than European when they leave the US. That makes sense because the US is almost as big as all Europe in terms of surface. 
<br/><br/>
The next figure shows the how far people go on average, when they travel (i.e. 200 km or more from their house), with or without leaving their country. 

![Distance EU vs US 2](/images/distance_without_leaving_country_eu_vs_us.png)

<p align="justify">One can observe that Gowalla's Americans users travel further than Gowalla's European users and Brightkite's European users travel further than Brightkite's American users. Therefore, we can unefortunately not conclude much due to this lack of data in Europe. Indeed, the big gap between Gowalla's and Brightkite's users in Europe is quite surprising and shows that more data is needed in Europe to draw strong conlusions about this aspect of the study.</p>
<br/><br/>
<p align="justify">The next figure shows the percentage of people who leaves their country when travelling. This corresponds to the percentage of people who, when travelling, left their country over the data collecting period (20 months for Gowalla and 30 months for Brightkite).</p> 

![Part of population EU vs US](/images/part_of_pop_out_eu_vs_us.png)

As the collection time was 10 months longer for the Brightkite dataset, it is not surprising to see higher numbers, as people will travel more over this longer period. It is also not surprising to see that American people leave less their country as Europeans, as US is much bigger in terms of surface. 

![Countries per traveller EU vs US](/images/countries_per_traveller_eu_vs_us.png)


## 2. But where are they going ?!

![Departures US Gowalla](/images/gowalla_departures_from_us.jpg)

![Departures Sweden Gowalla](/images/gowalla_departures_from_sweden.jpg)

![Departures US Brightkite](/images/brightkite_departures_from_us.jpg)

![Departures Sweden Brightkite](/images/brightkite_departures_from_sweden.jpg)

## 3. What is influencing travellers ? 

![Regression Brightkite](/images/polynomial_reg_brightkite.png)

![Regression Gowalla](/images/polynomial_reg_gowalla.png)

# Conclusion

# The team

Our team is composed of 3 students from EPFL : 

Chiara ONGARO, Cyril CHAMBE and Matthieu SOUTTRE

# Appendix

## Datasets used 

[Check-ins from Gowalla](https://snap.stanford.edu/data/loc-gowalla.html) 

[Check-ins from Brightkite](http://snap.stanford.edu/data/loc-brightkite.html)

[Country Mapping - ISO, Continent, Region](https://www.kaggle.com/andradaolteanu/country-mapping-iso-continent-region)

[Countries of the world](https://www.kaggle.com/fernandol/countries-of-the-world)

[Language list by country and place](https://www.kaggle.com/zinovadr/language-list-by-country-and-place?select=Language+List+by+Country+and+Place.xlsx)

[Continent - Country](https://www.kaggle.com/sarques/conticountry)

## Methods 

<br/><br/>

### Help for markdown

[Help](https://guides.github.com/features/mastering-markdown/)
