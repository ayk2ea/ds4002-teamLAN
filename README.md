# Project 2: Development of Convolutional Neural Network Model for Identification of Alzheimer’s Progression from MRI - Team LAN 

## Repository Contents 

## SRC
### Installing/Building the Code
In order to conduct a sentiment analysis of Washinton, D.C. Airbnbs, a sentiment analysis using the AFINN sentiment lexicon is applied. The AFINN dataframe assigns a sentiment value to individual words between -5(most negative sentiment), and +5(most positive sentiment) (AFINN Lexicon). By unnesting text in the "comments" column of the airbnb dataset, and conducting an inner_join with the AFINN lexicon, each word in the airbnb reviews that has a match to the AFINN dictionary is assigned a sentiment score. After assigning individual words a numerical value, a sentiment score for each review is calculated in a new column in the airbnb dataframe.

The following packages will need to be installed in order to build the code: tidyverse, tidytext, plotly, htmltools, caret, NbClust, and dplyr.

### Code Usage
Using the code above, found in SRC/Proj 1, run the file SRC/MI3 after downloading the following additional packages: cluster, facetoextra, caret, devtools, ggplot, and gridExtra. MI3 will use the final airbnb dataframe created in Proj 1 to conduct kmeans clustering with three clusters for each of the six neighborhoods in D.C. with the highest quantity of airbnb reviews.

## Data
### Data Dictionary
| Column | Data Type | Description |
| --- | --- | --- |
| nonDemented | Image | MRI scan presents no signs of dementia |
| veryMildDemented | Image | MRI scan presents very mild signs of dementia |
| mildDemented | Image | MRI scan presents mild signs of dementia |
| moderateDemented | Image | MRI scan presents moderate signs of dementia (the most extreme) |

### Link to Data
[Data](https://drive.google.com/drive/folders/1a0n-NMq7w3JVi8Uqd9f58lnLSFnOSaRh?usp=share_link)

### Notes about Data
Use datasets "listings" and reviews" for file Proj 1.rmd for Sentiment Analysis and then utilize "airbnbFinal" dataset for file MI3.Rmd for K-Means Clustering.

Dataset "airbnb" was combining "listing" and "reviews", "airbnb_filtered" dropped inessential columns from either datasets.

## Figures 

| Figure | Image | Description|
| --- | --- | --- |
| Neighborhood Wordclouds | ![Neighborhood Word Cloud](/Figures/Neighborhood Wordclouds/CHLP Wordcloud.png) | These plots are representation of the top 200 words per neighborhood which contain sentiment value as determined by AFINN lexicon. Size is proportional to the frequency of the words in the reviews for the neighborhoods |
| Elbow Plots | ![Elbow Plots](/Figures/ElbowPlots.png) | Elbow Plots are a graphical means to determine the appropriate numbers of clusters, 'k', that should be used in K-Means clustering; because the 'elbow' begins to bend around k=3, three clusters are selected for running the k-means clustering |
| Word Proportion by Neighborhood | ![Word Proportion by Neighborhood](/Figures/WordProportionbyNeighborhood.png) | Identifies whether there are any words that appear in higher proportion for a particular neighborhood |
| K-Means Clustering | ![K-Means Clustering](/Figures/kmeans.JPG) | Cluster plots for top 6 DC neighbourhood's with Airbnb listings > 10000, with 3 centers |

## References
[AFINN Lexicon](https://search.r-project.org/CRAN/refmans/corpus/html/sentiment_afinn.html#:~:text=The%20AFINN%20lexicon%20is%20a,but%20they%20are%20excluded%20here)  
[Airbnb Statistics & Insights](https://www.thezebra.com/resources/home/airbnb-statistics/)  
[Clustering Reviews Case Study](https://ieeexplore.ieee.org/document/7439368)  
[Creating Tidy Text](https://afit-r.github.io/tidy_text)  
[D.C. Crime Rates](https://www.neighborhoodscout.com/dc/washington/crime)  
[D.C. Gentrification Map](https://storymaps.arcgis.com/stories/009773cc5c224421a66d1ce9ff089849)   
[K-Means Clustering](https://uc-r.github.io/kmeans_clustering)  
[Word Clouds](https://towardsdatascience.com/create-a-word-cloud-with-rbde3e7422e8a)  
[Tidy Text Mining](https://www.tidytextmining.com/index.html)  



