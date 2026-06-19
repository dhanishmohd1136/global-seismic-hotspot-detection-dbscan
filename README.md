# Global Seismic Hotspot Detection and Anomaly Identification using DBSCAN

## Overview

This project applies **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** to historical global earthquake records to identify seismic hotspot regions and detect anomalous earthquake events. Unlike centroid-based clustering methods, DBSCAN can discover clusters of arbitrary shapes while naturally identifying noise points, making it suitable for geospatial earthquake analysis.

The project uses more than **1 million earthquake records** and focuses on uncovering spatial patterns in seismic activity through unsupervised machine learning.

---

## Objectives

* Identify global seismic hotspot regions.
* Detect anomalous earthquake events.
* Analyze earthquake distribution based on location, depth, and magnitude.
* Apply density-based clustering techniques to real-world geospatial data.
* Generate insights into earthquake occurrence patterns.

---

## Dataset

**Source:** Historical Global Earthquake Records

**Dataset Size:** 1,060,550 records

### Features Used for Clustering

| Feature   | Description           |
| --------- | --------------------- |
| latitude  | Earthquake latitude   |
| longitude | Earthquake longitude  |
| depth     | Earthquake depth (km) |
| mag       | Earthquake magnitude  |

---

## Project Workflow

### 1. Data Preprocessing

* Dataset inspection
* Missing value analysis
* Duplicate record detection
* Earthquake-specific exploratory data analysis
* Feature selection
* Processed dataset generation

### 2. DBSCAN Clustering

* Feature scaling using StandardScaler
* K-distance graph analysis
* DBSCAN parameter tuning
* Cluster generation
* Noise point detection

### 3. Cluster Analysis

* Hotspot identification
* Cluster profiling
* Magnitude analysis
* Anomaly investigation

### 4. Visualization

* Global earthquake distribution
* K-distance graph
* Earthquake hotspot visualization
* Anomaly event visualization
* Cluster magnitude distributions

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Repository Structure

```text
global-seismic-hotspot-detection-dbscan/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   └── 02_dbscan_hotspot_analysis.ipynb
│
├── outputs/
│   ├── figures/
│   └── results/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Methodology

### Data Preprocessing

The raw earthquake dataset was cleaned and analyzed to ensure data quality. Missing values, duplicate records, and feature relevance were assessed before preparing the dataset for clustering.

### Feature Scaling

Since DBSCAN relies on distance calculations, numerical features were standardized using StandardScaler.

### DBSCAN Clustering

DBSCAN was selected because:

* It does not require specifying the number of clusters.
* It can discover clusters with irregular shapes.
* It naturally identifies anomalies and noise points.
* It performs well for geospatial pattern discovery.

### Parameter Selection

A K-distance graph was used to identify an appropriate epsilon (`eps`) value for clustering.

---

## Key Outputs

* Seismic hotspot regions
* Earthquake cluster assignments
* Noise point identification
* Cluster profiles
* Geospatial visualizations

---

## Results

The project identifies regions with concentrated seismic activity and isolates anomalous earthquake events that do not belong to any major hotspot cluster.

Generated outputs include:

* Clustered earthquake dataset
* Cluster summary statistics
* Hotspot visualizations
* Anomaly visualizations

---

## Future Improvements

* Compare DBSCAN with HDBSCAN and OPTICS.
* Incorporate tectonic plate boundary information.
* Develop earthquake risk scoring models.
* Build an interactive Streamlit dashboard.
* Explore temporal clustering of seismic events.

---

## Installation

```bash
git clone https://github.com/dhanishmohd1136/global-seismic-hotspot-detection-dbscan.git

cd global-seismic-hotspot-detection-dbscan

pip install -r requirements.txt
```

---

## Usage

Run the notebooks in sequence:

```text
01_data_preprocessing.ipynb

02_dbscan_hotspot_analysis.ipynb
```

The processed dataset, figures, and clustering results will be generated inside the `outputs` directory.

---

## Author

**Muhammed Dhanish**

M.Sc. Applied Statistics and Data Analytics

Interests: Data Science, Machine Learning, Artificial Intelligence, Statistical Modeling, and Geospatial Analytics.

