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
**Data Manipulation**
* pandas
* numpy

**Data Visualization**
* seaborn
* matplotlib

**K-means**
* kneed
* sklearn - datasets, cluster(kmeans), metrics, preprocessing, 
* yellowbrick

## Data Preparation
K-means requires all analyzed variables to be numeric.  The values for several variables were encoded to numeric values

## Initial Variables
* Initial_days          Continuous
* TotalCharge           Continuous
* ReAdmitted            Categorical
* TimelyAdmissions      Categorical

## Analysis
The K-means clustering with centroids was used for this analysis. The K-mean algorithm is an unsupervised machine learning technique that groups data objects based on their similarities.  The grouping of my analysis is shown below (red x indicates centroid):
![image](https://user-images.githubusercontent.com/46407407/187055951-f6dd5e6b-77ce-455a-9428-aec313065995.png)

The ‘K’ value must be entered manually.  The ideal K-value can be determined through multiple runs of the K-means algorithm with different k-values.  Alternatively, the ideal K-value can be calculated programmatically.  The Silhouette Score metric was used to calculate the ideal K-value which was determined to be 2.

![image](https://user-images.githubusercontent.com/46407407/187055967-27984ecf-de42-48de-b7d7-079678638346.png)

## Accuracy
Silhouette Scoring was used to determine the goodness of the clustering technique.  The Silhouette score ranges from -1 to 1 where mean clusters of 1 are well apart.  A score of 1 is a perfect score and a score of 0 indicates no real grouping (Kumar, Sep 2020).   My analysis yielded a score of 0.8 

## Results and Implications
The clustering analysis displayed relatively dense clusters with good separation between clusters. 

## Limitations
One limitation to the analysis is K-means clustering is sensitive to outliers.  The variable ‘TimelyAdmissions’ does appear to have some outliers.  Refer to the box plot portion of the Univariate Analysis section of the attached Jupyter Notebook. 

## Recommendation
The executive team is advised to monitor their recently released patients.  Patients that had longer initial visits, higher total charges, and lower timely admission scores are more likely to be readmitted into the hospital.  
 
##  Source – Code Related.
1.	Kevin Arvai (July, 2020), K-Means Clustering in Python: A Practical Guide
https://realpython.com/k-means-clustering-python/
2.	Zach (Sep., 2021). “How to Create a Confusion Matrix in Python”, https://www.statology.org/confusion-matrix-python/
3.	Renesh Bedre (no date). K-means clustering in Python
https://www.reneshbedre.com/blog/kmeans-clustering-python.html
4.	Master Advanced Data Structures (Mar, 2022). Principal Component Analysis with Python.
https://www.geeksforgeeks.org/principal-component-analysis-with-python/

##  In-Line Sources.
1.	Ajitesh Kumar (Sep 2020), KMeans Silhouette Score Explained with Python
https://vitalflux.com/kmeans-silhouette-score-explained-with-python-example/
2.	Machine Learning Foundation (July, 2021). Difference between K means and Hierarchical Clustering.
https://www.geeksforgeeks.org/difference-between-k-means-and-hierarchical-clustering/
3.	Kevin Arvai (July, 2020), K-Means Clustering in Python: A Practical Guide
https://realpython.com/k-means-clustering-python//





