# Figures Descriptions
## Elbow Plots
Elbow Plots are a graphical means to determine the appropriate numbers of clusters, 'k', that should be used in K-means clustering. Because the 'elbow' begins to bend around k=3, three clusters are selected for running the K-means clustering.

## Neighborhood Wordclouds
These plots are representation of the top 200 words per neighborhood which contain sentiment value as determined by AFINN lexicon. Size is proportional to the frequency of the words in the reviews for the neighborhoods. 

## Word Proportion by Neighborhood
This figure was created to identify whether there are any words that appear in higher proportion for a particular neighborhood. To create this figure, the top 15 words appearing across all reviews in all neighborhoods was determined (by measure of frequency). Then, the frequency of these words in reviews pertaining to our neighborhoods of interest was determined, and the proportions were consequently calculated. 

## K-means
This figure is a visualization of the k-means algorithm run using the sentiment data collected and subsetted by neighborhood. The features of interest for the clustering were Sentiment Score, Word Count, and Positive Word Count. 
