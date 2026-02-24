# Project Overview

With millions of songs available on music streaming platforms, manual categorization into genres or moods is inefficient and subjective.

This project applies unsupervised machine learning techniques to automatically group Amazon Music tracks based on their audio characteristics.

By analyzing features like danceability, energy, tempo, and acousticness, we identify meaningful clusters that represent different musical styles or moods — without using predefined labels.

# The objective 

* Automatically group similar songs
* Identify hidden patterns in music data
* Build interpretable clusters based on audio features
* Support recommendation systems and playlist generation

# Dataset Description

The dataset contains audio features of Amazon Music tracks.
* **Dataset Name:** `single_genre_artists.csv`
* **Total Records:** 95,837 songs
* **Features Used for Clustering:**

* danceability
* energy
* loudness
* speechiness
* acousticness
* instrumentalness
* liveness
* valence
* tempo
* duration_ms



# Text Fields (Removed Before Clustering):

* id_songs
* name_song
* id_artists
* release_date
* genres
* name_artists


# Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* PCA (Dimensionality Reduction)
* K-Means
* DBSCAN
* t-SNE
  
# Project Workflow
## 1. Data Exploration & Preprocessing

Checked dataset structure and data types

Handled missing values

Removed unnecessary columns

Normalized features using StandardScaler

## 2 Feature Selection

Used **StandardScaler** because clustering is distance-based.

Without scaling, features like loudness & tempo dominate.


## 3 Dimensionality Reduction

Applied PCA for:

Reducing dimensions

Visualizing clusters in 2D space

## 4️ Clustering Techniques Implemented
K-Means Clustering

Used the Elbow Method to determine optimal k

Evaluated using Silhouette Score

Added cluster labels to the dataset

DBSCAN

Tuned eps and min_samples

Detected noise/outliers

Discovered arbitrary-shaped clusters

# Model Evaluation Metrics
Metric	Purpose
Silhouette Score	Measures cluster separation quality
Davies-Bouldin Index	Evaluates intra/inter-cluster similarity
Inertia	Measures cluster compactness (K-Means)
Cluster Size Balance	Checks even distribution of songs
Feature Interpretability	: Understand dominant characteristics

# Visualizations

* Distribution plots of audio features
* Elbow curve
* Silhouette comparison
* PCA 2D visualization
* t-SNE visualization
* Heatmap of cluster feature averages
  
# Cluster Interpretation
##  Cluster Interpretation

###  Cluster 0 – Instrumental / Acoustic Focus

* Very high instrumentalness
* High acousticness
* Low loudness
* Calm / atmospheric


###  Cluster 1 – Party / Dance Pop

* High energy
* High danceability
* High valence (happy mood)
* Loud and energetic


###  Cluster 2 – Rap / Spoken Content

* Extremely high speechiness
* Very low instrumentalness
* Moderate energy


###  Cluster 3 – Chill Acoustic / Soft Pop

* Very acoustic
* Low energy
* Emotional/indie feel

Conclusion

* The clustering process successfully segmented the dataset into meaningful groups.
By exporting each cluster separately:
* The dataset becomes easier to interpret
* Enables deeper analysis
* Supports business intelligence and reporting
* Improves model deployment flexibility
* This marks the final stage of the clustering workflow.
