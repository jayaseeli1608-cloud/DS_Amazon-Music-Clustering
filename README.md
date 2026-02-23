# DS_Amazon-Music-Clustering
Here is a **professional GitHub README.md file** for your project:

---

# Amazon Music Clustering Using Unsupervised Machine Learning

## Project Overview

This project applies **Unsupervised Machine Learning (K-Means Clustering)** to group Amazon Music tracks based on their audio characteristics.

Instead of manually labeling genres, this model automatically discovers patterns in features like:

* Danceability
* Energy
* Loudness
* Speechiness
* Acousticness
* Instrumentalness
* Valence
* Tempo
* Duration

The goal is to identify meaningful clusters that represent musical moods or styles.

---

##  Problem Statement

With millions of songs available on streaming platforms like **Amazon Music**, manually categorizing tracks is impractical.

This project builds a clustering model that:

* Groups similar songs together
* Identifies hidden music patterns
* Supports recommendation systems
* Enables playlist automation

---

##  Objectives

* Perform Data Exploration & Cleaning
* Normalize audio features
* Apply K-Means clustering
* Determine optimal number of clusters
* Evaluate clusters using multiple metrics
* Visualize cluster patterns
* Interpret cluster characteristics

---

## 📂 Dataset Information

* **Dataset Name:** `single_genre_artists.csv`
* **Total Records:** 95,837 songs
* **Features Used for Clustering:**Removed duplicates
Dropped irrelevant text columns
Used StandardScaler for normalization
Scaling prevents dominance of loudness & tempo
<img width="1808" height="196" alt="image" src="https://github.com/user-attachments/assets/051a7104-2a3a-4a20-b399-3a022ed3b1c9" />


```
danceability
energy
loudness
speechiness
acousticness
instrumentalness
liveness
valence
tempo
duration_ms
```

Text columns removed:

```
id_songs
name_song
id_artists
release_date
genres
name_artists
```

---

## ⚙️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* PCA
* t-SNE

---

## Methodology

###  Data Exploration & Preprocessing

* Checked missing values & duplicates
* Removed non-relevant text columns
* Selected only sound-related features

### Feature Scaling

Used **StandardScaler** because clustering is distance-based.

Without scaling, features like loudness & tempo dominate.

###  Finding Optimal Clusters

#### Elbow Method

Elbow observed around **k = 4**

####  Silhouette Scores

| k | Score |
| - | ----- |
| 2 | 0.203 |
| 3 | 0.242 |
| 4 | 0.231 |
| 5 | 0.186 |

Final choice: **k = 4**

---

## 📊 Cluster Evaluation Metrics

* **Silhouette Score:** `0.231`
* **Davies-Bouldin Index:** `1.53`
* **Inertia:** Used for compactness evaluation

---

## 🎼 Cluster Interpretation

### 🎹 Cluster 0 – Instrumental / Acoustic Focus

* Very high instrumentalness
* High acousticness
* Low loudness
* Calm / atmospheric

---

### 🎉 Cluster 1 – Party / Dance Pop

* High energy
* High danceability
* High valence (happy mood)
* Loud and energetic

---

### 🎙 Cluster 2 – Rap / Spoken Content

* Extremely high speechiness
* Very low instrumentalness
* Moderate energy

---

### 🎵 Cluster 3 – Chill Acoustic / Soft Pop

* Very acoustic
* Low energy
* Emotional / indie feel

---

## 📊 Visualizations Included

* Distribution plots of audio features
* Elbow curve
* Silhouette comparison
* PCA 2D visualization
* t-SNE visualization
* Heatmap of cluster feature averages

---

## 💼 Business Use Cases

* 🎧 Personalized playlist generation
* 🔍 Improved song discovery
* 🎤 Artist similarity analysis
* 📊 Market segmentation for streaming platforms
* 🤖 Music recommendation engines


## 📈 Results

The clustering successfully identified:

* Energetic commercial music
* Instrumental tracks
* Rap / spoken word tracks
* Emotional acoustic tracks

These clusters align with real-world musical patterns and can support recommendation systems.

---

## 🔮 Future Improvements

* Deploy as a Streamlit web app
* Add Spotify API integration
* Try DBSCAN & Hierarchical Clustering
* Improve silhouette score with feature engineering

Tell me which version you prefer 😊
