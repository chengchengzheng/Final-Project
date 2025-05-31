
# Final-Project
## 1.Inland Water Body Detection with ML
### Normandy(flooded) vs Awbari(dray)
![S2B_MSIL2A_20250429T104619_N0511_R051_T31UET_20250429T130440-ql](https://github.com/user-attachments/assets/5c59e03f-83dd-4e65-a46a-10b090cfcc4f)
![S2A_MSIL2A_20250525T094051_N0511_R036_T33RUN_20250525T120714-ql](https://github.com/user-attachments/assets/e0843433-956b-4e61-ac41-ac8b0eeb2f8b)
## 2.Inland Water Detection in Flood-Prone Areas using Sentinel-2 and Unsupervised ML

“A study on NDWI + K-means classification of satellite imagery in Normandy and Awbari.”
## 3.About the Project 
This project was developed as part of the GEOL0069 AI4EO module at University College London. It focuses on applying machine learning to satellite imagery to detect and classify inland water bodies in both flood-prone and dry regions.The study uses freely available Sentinel-2 imagery and explores the performance of three key techniques in different hydrological settings.
### Techniques Applied 
·NDWI (Normalized Difference Water Index)

·MNDWI (Modified NDWI using Green & SWIR bands)

·K-means clustering (unsupervised learning algorithm)
### 4.🌍 Study Areas
·Normandy Estuary, France

A coastal deltaic zone located in western Normandy, characterized by dense river networks, tidal inlets, and dynamic hydrology. This region is prone to seasonal flooding due to both river overflow and tidal influence, making it an ideal candidate for assessing flood detection techniques.

·Awbari Region, Libya

A hyper-arid inland area near the town of Awbari in the Libyan Sahara. This region experiences extremely low annual rainfall, sparse vegetation, and minimal surface water presence, making it suitable as a non-flooded baseline. 

-This project uses open-access Sentinel-2 data to compare the performance of NDWI, MNDWI, and K-means clustering for detecting water bodies in both flooded and dry regions. By testing different band combinations and algorithm outputs, it evaluates the accuracy and adaptability of each method under varying environmental conditions.

Additionally, the project uses the CodeCarbon tool to estimate emissions from computation, highlighting the environmental efficiency of the approach.

## 5.Background

Inland water bodies, such as lakes, rivers, and reservoirs, are vital to ecosystems, agriculture, and human livelihoods. However, they are increasingly impacted by climate change and human activities, making accurate and timely monitoring essential (Zeng et al., 2023).

Remote sensing provides an efficient, scalable, and cost-effective approach for surface water detection. This project builds on existing research by applying Sentinel-2 satellite data and machine learning techniques to enhance the identification of inland water bodies.

## 6.Description of the Problem
Problem Overview

Flooding is one of the most widespread and destructive natural hazards, posing significant threats to human lives, infrastructure, and economies. Rapid and accurate flood detection is crucial for disaster response, risk management, and long-term resilience planning.

Conventional flood mapping methods—such as field surveys or drone-based inspections—can be time-consuming, expensive, and spatially limited. In contrast, satellite-based remote sensing offers a scalable, timely, and cost-effective solution for monitoring large areas and detecting water bodies with minimal delay.

This project investigates how to effectively identify inland water in both flood-prone and dry environments using freely available Sentinel-2 imagery and basic unsupervised machine learning techniques. Specifically, it explores:

The effectiveness of NDWI and MNDWI in detecting water bodies across various land types
Whether K-means clustering can enhance or complement traditional water indices
How different spectral band combinations perform under complex conditions such as urban shading or high sediment levels
By combining visual interpretation with quantitative evaluation, the project proposes a lightweight and adaptable framework for flood mapping, particularly suited for regions with limited data or infrastructure.

## 7. The SENTINEL-2 Satellite

Sentinel-2 data have a positive impact on land cover/use monitoring, especially in terms of crops, forests, urban areas and water resources. When combined with other remote sensing data, the accuracy rate is very high. 80%(Phiri et al., 2020).

<img width="678" alt="截屏2025-05-31 12 55 28" src="https://github.com/user-attachments/assets/40f4d85b-5054-4451-a06c-861d5bae239c" />
                        (Elspina, n.d.)
                        
---



In this project, we utilized selected spectral bands from the Sentinel-2 satellite to support optical remote sensing analysis. Specifically, four bands were employed due to their relevance to water and moisture detection:

·Band B03 (Green, 560 nm): Utilized for water body detection through the Normalized Difference Water Index (NDWI), which enhances the distinction between water features and surrounding land.

·Band B08 (Near-Infrared, 842 nm): Employed in conjunction with the green band to compute NDWI, contributing to improved water delineation accuracy.

·Band B11 (Short-Wave Infrared 1, 1610 nm): Applied in Modified NDWI (MNDWI) and other spectral water index (SWI) methodologies, providing sensitivity to surface moisture and wetness.

·Band B05 (Red Edge, 705 nm): Used for constructing SWI-based features within machine learning frameworks, especially for vegetation and moisture-related analyses.

## 8.Normalized Difference Water Index (NDWI)


```math

NDWI = \frac{Green - NIR}{Green + NIR}
```

<img width="370" alt="截屏2025-05-31 16 48 45" src="https://github.com/user-attachments/assets/abd085fa-5e88-4ca3-b9c7-c1a9a4f3d557" />



-- The NDWI, proposed by McFeeters (1996), enhances water features while suppressing non-water elements like vegetation or soil (Xu, 2006). Though widely used for water detection, it performs poorly in urban areas or turbid waters (Xu, 2006; Jiang et al., 2020). In this study, it serves as a baseline for evaluating machine learning-based methods.

## 9.MNDWI
```math

MNDWI = \frac{Green - SWIR1}{Green + SWIR1 + \epsilon}
```
MNDWI (Modified Normalized Difference Water Index) is an effective index used for water body detection and monitoring in remote sensing imagery. It is a modification of the traditional NDWI (Normalized Difference Water Index) and is designed to enhance the detection of water bodies while minimizing interference from land surfaces, such as buildings and vegetation. The index is calculated using the green band and the shortwave infrared (SWIR) band, which allows it to better distinguish water from non-water surfaces. MNDWI is widely used in various applications, including flood monitoring, lake and river changes, and urban water body analysis. Its ability to accurately identify water bodies, even in areas with significant land surface interference, makes it a valuable tool for environmental monitoring and management.

## 10.Machine Learning Methodology: K-Means Clustering

K-means clustering is an unsupervised machine learning algorithm widely applied in remote sensing to classify pixels based on spectral similarity—without requiring any labeled data or prior ground truth. In the context of Sentinel-2 imagery, K-means is particularly effective for exploratory analysis, such as water body detection.

<img width="701" alt="截屏2025-05-31 14 46 53" src="https://github.com/user-attachments/assets/6dcd0f3e-08f7-4f9e-8052-4f38ed23bb63" />

--- (Lindsey, 2021)


This method partitions the input dataset into K clusters, where each pixel is assigned to the nearest centroid based on Euclidean distance in feature space. The centroids are iteratively updated until the clusters stabilize. The algorithm is especially useful for identifying patterns in multispectral data, where the structure of the data may not be known a priori.

In our workflow, K-means is applied to various spectral indices calculated from Sentinel-2 bands, including:

**·NDWI (B03 + B08)**

**·MNDWI (B03 + B11)**

**·SWI (B05 + B11)**

These indices are stacked to form a 2D feature array, which is then clustered using K-means. Binary water masks from thresholding NDWI/MNDWI are used for comparison, allowing us to evaluate how machine learning can match or improve upon traditional water detection methods.

The key steps include:

**·Loading Sentinel-2 bands**

**·Calculating NDWI/MNDWI**

**·Applying thresholds to generate binary masks**

**·Running K-means on the stacked array**

**·Visualizing and comparing classification outputs**

This integrated approach combines domain-specific index calculation with unsupervised learning, offering a flexible and scalable solution for surface water mapping.


## 11.Getting Started
This project, created using Google Colab, allows you to detect inland water bodies using machine learning (ML) on Sentinel-2 data. To get started, follow these simple steps:

**1.Download the project:**
Download the ML Detection of Inland Water Bodies.ipynb file from the repository to your local machine or Google Drive.

**2.Acquire datasets:**
Download the required Sentinel-2 .SAFE bands, and upload them to your Google Drive if using Google Colab.
If you're working with different datasets, make sure to modify the dataset paths accordingly in the notebook.

**3.Set up your environment:**
Ensure you are using Python 3.8+ and have the necessary libraries installed:
rasterio, scikit-learn, numpy, matplotlib, and codecarbon
Run the necessary cells in the notebook to load the datasets, calculate NDWI/MNDWI values, apply K-means clustering, and visualize the water body classification results.

**4.Run the code:**
Once your environment is set up, follow the notebook steps sequentially. The project will automatically guide you through water body detection, providing visual outputs like NDWI masks, K-means classifications, and comparison charts.
This approach combines the use of machine learning for water body detection with Sentinel-2 data, offering a powerful method for analyzing and monitoring surface water globally.

## 12.Datasets Used

The **Sentinel-2 L2A** images were downloaded from the **Copernicus Data Space** website. Only bands B03, B05, B08, and B11 were used. The images were downsampled for memory efficiency.


**· Normandy， France (April 2025,Flood season)**

**· Awbari，Libya （April 2025,Dry season）**

# Environmental Cost of the Project

This project emphasizes **sustainable AI practices** by using an energy-efficient, cloud-based workflow. The flood detection process was executed with minimal computational resources—without GPU acceleration or local infrastructure—using CPU-based operations on **Google Colab**, which leverages shared resources.

## 13。 Carbon Emissions Measured with codecarbon

The codecarbon package was used to estimate emissions during two key processing sessions:
1. **Normandy** – a flood-prone deltaic region  ：  0.000103 kg CO₂
2. **Awbari** – used as a dry season control region ：0.000921 kg CO₂

> **Environmental Impact Assessment**

The environmental footprint of this project is extremely low. For comparison, a typical two-hour car trip emits 0.5 kg of CO₂, while the entire computational process here produced only 0.001024 kg of CO₂ — less than 1/400th of a car journey.

No fuel-powered equipment or field surveys were needed. All analysis used freely available Sentinel-2 satellite imagery on a cloud-based platform, ensuring minimal energy consumption. This approach shows how remote sensing and data science can support sustainable research by maintaining scientific quality with minimal environmental impact.

---
The low emissions of this project are due to several key factors. First, no physical fieldwork was required, such as flights, car trips, or drone surveys. Second, publicly available satellite data, specifically free Sentinel-2 imagery provided by the European Space Agency, was used. Additionally, the project was run on the shared cloud infrastructure of Google Colab, utilizing shared GPUs and CPUs. The code was also optimized, with raster data files downsampled before processing, significantly reducing RAM and CPU load. Finally, the K-means clustering algorithm used is unsupervised and computationally light, eliminating the need for complex model training.

## 14.conclusion
This project showcases how low-carbon AI can be applied in environmental research, using open data and shared computing to significantly reduce carbon emissions.  By relying on free Sentinel-2 imagery and running the process on Google Colab’s shared GPUs/CPUs, we avoid the need for physical fieldwork, like flights or car trips, and minimize the use of high-power servers.  The code is optimized by downsampling raster data to save on memory and reduce computational load.  Additionally, K-means clustering, a lightweight, unsupervised algorithm, eliminates the need for resource-heavy model training.  Unlike traditional workflows that require extensive resources, this approach enables reproducibility with minimal environmental impact, making it scalable to other regions without added cost or emissions.  Ultimately, this demonstrates how cloud tools and efficient algorithms can reduce the environmental footprint of Earth observation, while promoting responsible AI practices in the geospatial domain.

# Contact

Chengcheng Zheng - [zcfbczh@ucl.ac.uk](mailto:fiona.mckee.23@ucl.ac.uk) 




<!-- ACKNOWLEDGMENTS -->
# Acknowledgments
This project was created for GEOL0069 at University College London, taught by Dr. Michel Tsamados and Weibin Chen.


## Reference
1.Zeng, F., Song, C., Cao, Z., Xue, K., Lu, S., Tan, C., & Liu, K. (2023). Monitoring inland water via Sentinel satellite constellation: A review and perspective. ISPRS Journal of Photogrammetry and Remote Sensing, 204, 340–361. https://doi.org/10.1016/j.isprsjprs.2023.09.011

2.McFeeters, S.K. (1996). NDWI for delineating open water. *IJRS*

3.Jiang, W., Ni, Y., Pang, Z., He, G., Fu, J., Lu, J., Yang, K., Long, T., & Lei, T. (2020). A NEW INDEX FOR IDENTIFYING WATER BODY FROM SENTINEL-2 SATELLITE REMOTE SENSING IMAGERY. ISPRS Annals of the Photogrammetry, Remote Sensing and Spatial Information Sciences, V-3–2020, 33–38. https://doi.org/10.5194/isprs-annals-v-3-2020-33-2020

4.Phiri, D., Simwanda, M., Salekin, S., Nyirenda, V. R., Murayama, Y., & Ranagalage, M. (2020). Sentinel-2 data for land cover/use mapping: A review. Remote sensing, 12(14), 2291.

5.Xu, H. (2006). Modification of normalised difference water index (NDWI) to enhance open water features in remotely sensed imagery. International Journal of Remote Sensing, 27(14), 3025–3033. https://doi.org/10.1080/01431160600589179

6.Lindsey, M. (2021, March 25). K-means clustering: Unveil hidden patterns in data. freeCodeCamp. Retrieved May 31, 2025, from https://www.freecodecamp.org/news/k-means-clustering-unveil-hidden-patterns-in-data/


6.Elspina. (n.d.). Sentinel Data Analysis 101. Retrieved May 31, 2025, from https://space.elspina.tech/sentinel-data-analysis-101-5f15bad35d35
