# Face Detection and Clustering using HSV and K-Means

## 📌 Aim

The objective of this project is to:
- Detect faces in a faculty group image using Haar Cascade classifiers.
- Extract meaningful color features (Hue and Saturation) from detected faces.
- Perform clustering using the K-Means algorithm.
- Classify a template image (`Dr_Shashi_Tharoor.jpg`) into one of the learned clusters.
- Visualise clustering results using scatter plots and image embeddings.

---

## 🧠 Methodology

### 1️⃣ Face Detection
- Used OpenCV’s Haar Cascade classifier.
- Converted image to grayscale for detection.
- Detected bounding boxes around faces.

### 2️⃣ Feature Extraction (HSV Color Space)
- Converted detected face regions from BGR to HSV.
- Extracted:
  - Mean Hue
  - Mean Saturation
- Constructed a feature vector for each face.

Why HSV?
- Hue captures dominant color tone.
- Saturation captures intensity of color.
- More robust for clustering compared to raw RGB.

---

### 3️⃣ Clustering using K-Means
- Applied K-Means with `n_clusters = 2`.
- Grouped faces based on similarity in HSV feature space.
- Computed centroids for each cluster.

---

### 4️⃣ Template Classification
- Detected face in `Dr_Shashi_Tharoor.jpg`.
- Extracted HSV features.
- Used trained K-Means model to predict cluster membership.
- Visualised template point in feature space.

---

## 📊 Visualisations

### 🔹 Face Detection Result
<img width="1695" height="965" alt="image" src="https://github.com/user-attachments/assets/eaec151c-014a-4685-a4b2-90deee65dd70" />

<img width="588" height="583" alt="image" src="https://github.com/user-attachments/assets/41180814-ff8d-4503-ba80-901355e3bd95" />


---


## 📈 Key Findings

- HSV-based features effectively separate faces into clusters based on dominant color characteristics.
- K-Means successfully identified two distinct groups in feature space.
- The template image was classified based on proximity to cluster centroids.
- Visualization confirmed that clustering aligns well with visual color similarity.

---

## ⚖️ Model Insights

### Distance Metric
K-Means uses Euclidean distance:

\[
d = \sqrt{\sum (x_i - y_i)^2}
\]

### Observations
- Small feature space (Hue, Saturation) works well for simple clustering.
- Model performance depends heavily on good face detection.
- Lighting conditions influence HSV values.

---

## 🔍 Limitations

- Clustering is based only on color, not facial structure.
- Sensitive to lighting variations.
- Haar Cascade may miss faces at extreme angles.

---

## 🚀 Future Improvements

- Use facial embeddings instead of color features.
- Apply dimensionality reduction (PCA).
- Use DBSCAN or hierarchical clustering.
- Improve detection using deep learning models.

---

## 🛠 Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn

---

## 📌 Conclusion

This project demonstrates how classical computer vision techniques combined with unsupervised learning can be used to cluster and classify faces based on color characteristics.

While simple, the approach highlights the importance of feature selection and distance metrics in clustering tasks.

---

## 👤 Author

Himesh Agarwal  
B.Tech – Data Science, Economics & Business  
Plaksha University
