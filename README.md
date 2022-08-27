# D212: K-Means Clustering of Hospital Data

## Question
Which patients are most likely to be readmitted into the hospital?

## Goal
K-means will be used in this analysis to determine which patients are most likely to be readmitted back into the hospital after his or her initial stay. 

## Justification
K -means clustering will attempt to divide the data into non-overlapping clusters based on values for a subset of the variables.  The members of the individual clusters are grouped based on their similarities.  The grouping of new data points will help to indicate which patients are more likely to be readmitted based on which cluster they are associated with. 
      
## Assumption
K-means clustering is not well suited for clusters having complex shapes (Arvai, 2020).  I assumed the clustering shape would be spherical enough to meet this criterion. 

## Libraries
** Data Manipulation**
* pandas
* numpy

** Data Visualization **
* seaborn
* matplotlib

**K-means**
* kneed
* sklearn - datasets, cluster(kmeans), metrics, preprocessing, 
* yellowbrick

## Data Preparation
