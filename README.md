# Application of Azevedo et al. - Extracting Insights from NBA Data Using Topology - to the 2022 UAAP Dataset

### Benjamin Ang, Alexander Pino, Dane Rosario

## Introduction

The goal of this project is to apply the methods of Azevedo et al. to our procured dataset describing the Philippine intercollegiate league, University Athletics Association of the Philippines (UAAP), during its 2022 season. We will summarize the methods used in their study, naively apply their method to our dataset, then perform adaptations by comparing the quality of our obtained data to that used in Azevedo et al.

## Methods of Azevedo et al.

### Traditional Methods

Goal: Process the data to produce an input csv file that could directly be used in the Mapper pipeline, and using unsupervised methods to understand the data.

Components: 
* Dimensionality Reduction techniques to visualize the feature importance and correlation
* Feature selection methods to determine subsets of features that produce good results
* Compare the results of several cluster techniques
* Finally, understand if our data could be easily split into a small amount of clusters

#### Data Preprocessing and Dimensionality Reduction

* We chose to store in the dataset the logarithm of the player salaries, instead of using the actual salaries. This choice was motivated by the exponential shape of the salary distribution. 
* * Since PCA is a linear method, we decided to use logarithm scaled salaries in our analysis
* * **Normalize exponential shapes to linear shapes in our analysis**

* **We perform the PCA to two different datasets**
* * We drop the column containing player position labels
* * First dataset: Complete dataset
* * Second dataset: Time Normalized (time related features divide by the total time of participation)

* Graph created: PCA dimension (1 and 2) and (3 and 4). Each datapoint is colored according to their position. Can we identify visually the positions?

* Explained variance per eigenvector chart. The dimensions? we don't know what they are yet

* Chart between only PG and C

* Circle of correlations between variables chart - finding the highest correlation stats with dim 1 and dim 2

* Salary concern: irrelevant, we are analyzing collegiate basketball

* What are distinct features of collegiate basketball? Years of experience, coach quality, budget?

* Time normalized dataset - better uniformly distributed and worse results in clustering analysis?


