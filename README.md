### Lab 5 – Face Clustering using K-Means Algorithm

## Objective

The objective of this experiment is to detect faces in an image and organize them into groups based on similarity using the K-Means clustering algorithm. Colour-based features, specifically Hue and Saturation values, are extracted from each detected face. These features are then used to cluster faces and classify a new input face according to the learned clusters.

## Procedure

The experiment was carried out in the following stages:

1. Face Detection

The input image was first converted into grayscale format to simplify processing.

OpenCV’s Haar Cascade Classifier was used to identify human faces within the image.

Bounding boxes were drawn around each detected face to mark their locations.

2. Feature Extraction

The original image was converted from BGR colour space to HSV colour space.

For every detected face region:

The average Hue value was computed to represent the dominant colour.

The average Saturation value was calculated to represent colour intensity.

Each face was represented as a feature vector containing two values:
(Mean Hue, Mean Saturation)

3. Clustering using K-Means

The K-Means clustering algorithm was applied with the number of clusters set to 2.

Faces with similar Hue and Saturation values were grouped into the same cluster.

The algorithm calculated centroids representing the centre of each cluster.

4. Classification of a New Face

A separate image containing Dr. Shashi Tharoor was used as a test sample.

The face was detected and its Hue and Saturation values were extracted.

These features were passed to the trained K-Means model to determine the closest cluster.

5. Data Visualisation

All detected faces were plotted on a graph with Hue on one axis and Saturation on the other.

Each cluster was displayed using a different colour for clear distinction.

Cluster centroids were highlighted.

The test face was also plotted to show its cluster assignment.

## Observations

Haar Cascade successfully detected faces from the image.

HSV colour features provided a useful and simple representation of facial characteristics.


K-Means clustering effectively separated faces based on colour similarity.

The new test face was correctly assigned to the nearest cluster.

Graphical representation helped in clearly understanding cluster formation.

## Outputs and Figures

![Plaksha_Faculty](https://github.com/user-attachments/assets/9735f076-6fec-4d35-8dba-df88e33ad9aa)

![Dr_Shashi_Tharoor](https://github.com/user-attachments/assets/2dd06290-e8f8-4505-8804-a05f1455244a)

<img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/41d1585a-acba-410e-8a0d-01b79aae8d37" />

<img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/4a0ea5d4-04ea-4625-b34e-f482d45ea7f8" />

<img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/a6579cb1-ffd7-4794-9b3f-b0c2de9a1c97" />

<img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/873e2b1e-c2ed-49b0-ab48-2841cfdfe984" />

## Conclusion

This lab demonstrated how computer vision and unsupervised machine learning techniques can be used together for face grouping and classification. Faces were detected using OpenCV, and HSV-based colour features were extracted to represent each face numerically. The K-Means algorithm grouped similar faces into clusters, and a new face was successfully classified based on its feature similarity. This experiment highlights the importance of feature extraction, clustering algorithms, and visual analysis in image processing tasks.










