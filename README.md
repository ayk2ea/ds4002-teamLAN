# Project 1 - Team LAN 

## Repository Contents 

## SRC
### Installing/Building the Code
In order to conduct a sentiment analysis of Washinton, D.C. Airbnbs, a sentiment analysis using the AFINN sentiment lexicon is applied. The AFINN dataframe assigns a sentiment value to individual words between -5(most negative sentiment), and +5(most positive sentiment) (AFINN Lexicon). By unnesting text in the "comments" column of the airbnb dataset, and conducting an inner_join with the AFINN lexicon, each word in the airbnb reviews that has a match to the AFINN dictionary is assigned a sentiment score. After assigning individual words a numerical value, a sentiment score for each review is calculated in a new column in the airbnb dataframe.

The following packages will need to be installed in order to build the code: tidyverse, tidytext, plotly, htmltools, caret, NbClust, and dplyr.

### Code Usage
Using the code above, found in SRC/Proj 1, run the file SRC/MI3 after downloading the following additional packages: cluster, facetoextra, caret, devtools, ggplot, and gridExtra. MI3 will use the final airbnb dataframe created in Proj 1 to conduct kmeans clustering with three clusters for each of the six neighborhoods in D.C. with the highest quantity of airbnb reviews.

## Data
### Data Dictionary
| Column | Data Type | Description|
| --- | --- | --- |
| Listing ID | Numeric (Integer) | AirBNB’s unique identifier for each listing. This column was used to join together the two datasets of “listing” and “reviews” for our established dataset “airbnb”|
| Comments | Character (Text) | Reviews left by individuals who have stayed at the AirBNB |
| Name | Character (Text) | Name of each AirBNB listing. For example: “Vitas Hideaway” or “Cozy apt in Adams Morgan" |
| Neighborhood | Character (Text) | Lists the Washington DC neighborhood each AirBNB is located in; most neighborhoods are grouped together to cover more area |
| Room Type | Character (Text) | All AirBNB listings are grouped into the following room types: entire place, private room, and shared room |
| Price | Numeric (Integer) | Price for one night at each AirBNB listing |
| Number of Reviews | Numeric (Integer) | Total number of reviews the AirBNB listing has |

Neighborhoods with most Airbnb listings included in analysis (>10,000 listings): 
1. Capitol Hill/Lincoln Park (CHLP)
2. Union Station, Stanton Park, Kingman Park (USSPKP)
3. Columbia Heights, Mt. Pleasant, Pleasant Plains, Park View (CHMPPPPV)
4. Edgewood, Bloomingdales, Truxton Circle, Eckington (EBTCE)
5. Shaw, Logan Circle (SLC)
6. Dupont Circle, Connecticut Ave/K Street (DCCAS)

### Link to Data
[Data](https://drive.google.com/drive/folders/1a0n-NMq7w3JVi8Uqd9f58lnLSFnOSaRh?usp=share_link)

### Notes about Data
Use datasets "listings" and reviews" for file Proj 1.rmd for Sentiment Analysis and then utilize "airbnbFinal" dataset for file MI3.Rmd for K-Means Clustering.

Dataset "airbnb" was combining "listing" and "reviews", "airbnb_filtered" dropped inessential columns from either datasets.

## Figures 

| Figure | Image | Description|
| --- | --- | --- |
| Elbow Plots | ![Elbow Plots](/Figures/ElbowPlots.png) | Elbow Plots are a graphical means to determine the appropriate numbers of clusters, 'k', that should be used in K-Means clustering; because the 'elbow' begins to bend around k=3, three clusters are selected for running the k-means clustering |
| K-Means Clustering | ![K-Means Clustering](/Figures/kmeans.JPG) | Cluster plots for top 6 DC neighbourhood's with Airbnb listings > 10000, with 3 centers |

## References
[AFINN Lexicon](https://search.r-project.org/CRAN/refmans/corpus/html/sentiment_afinn.html#:~:text=The%20AFINN%20lexicon%20is%20a,but%20they%20are%20excluded%20here)
[Clustering Reviews Case Study](https://ieeexplore.ieee.org/document/7439368)  
[Creating Tidy Text](https://afit-r.github.io/tidy_text)  
[D.C. Crime Rates](https://www.neighborhoodscout.com/dc/washington/crime)
[D.C. Gentrification Map](https://storymaps.arcgis.com/stories/009773cc5c224421a66d1ce9ff089849)   
[K-Means Clustering](https://uc-r.github.io/kmeans_clustering)  
[Word Clouds](https://towardsdatascience.com/create-a-word-cloud-with-rbde3e7422e8a)  
[Tidy Text Mining](https://www.tidytextmining.com/index.html)  



