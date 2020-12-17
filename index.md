# Why are we doing this ?

Being able to identify the predominant human fluxes and mobility patterns in the world is crucial for effectively modelling the spreading of diseases, establishing effective mobility connections and understanding the travelling habits of different populations. This project extension continues the exploration of human geographic movement by relating the latitude and longitude coordinates of check-ins (to the Gowalla and Brightkite social networks) to the respective countries where the localization took place. This is done with the purpose of investigating human migration patterns within and among countries. We are looking for eventual correlation between the users’ home location and their travelling destinations, possibly identifying what are the most frequent connections among countries. 

# The main questions we asked ourselves

1. What are the main fluxes of people over the world ?
2. Have some countries different trips habits than others ?
3. What is the influence of factors like the language, the distance or the GDP on travlling habits ? 

# What was our input data ?

We were given several millions of check-ins and the friendship network coming from two social networks : Brightkite and Gowalla. 

Here's a summary of this data :

Social network | Number of check-ins | Number of users | Number of countries and places | Number of nodes | Number of edges 
------------ | ------------- | ------------- | ------------- | ------------- | ------------- 
Brightkite | 4 491 035 | 50 686 | 242 | 58 228 | 214 078
Gowalla | 6 442 728 | 107 069 | 196 | 196 591 | 950 327

You can see the distribution of these millions over the planet right there : 
![Check-ins map](/images/checkins_map.jpeg)

# How do we shaped this data ? 

# Conclusion

# The team

Our team is composed of 3 students from EPFL : 

Chiara ONGARO
Cyril CHAMBE
Matthieu SOUTTRE

# Appendix

## Datasets used 

[Check-ins from Gowalla](https://snap.stanford.edu/data/loc-gowalla.html) 

[Check-ins from Brightkite](http://snap.stanford.edu/data/loc-brightkite.html)

[Country Mapping - ISO, Continent, Region](https://www.kaggle.com/andradaolteanu/country-mapping-iso-continent-region)

[Countries of the world](https://www.kaggle.com/fernandol/countries-of-the-world)

[Language list by country and place](https://www.kaggle.com/zinovadr/language-list-by-country-and-place?select=Language+List+by+Country+and+Place.xlsx)

## Methods 

### Help for markdown

[Help](https://guides.github.com/features/mastering-markdown/)
