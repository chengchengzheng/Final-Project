# Final-Project
## Inland Water Body Detection with ML
### Normandy(flooded) vs Awbari(dray)
![S2B_MSIL2A_20250429T104619_N0511_R051_T31UET_20250429T130440-ql](https://github.com/user-attachments/assets/5c59e03f-83dd-4e65-a46a-10b090cfcc4f)
![S2A_MSIL2A_20250525T094051_N0511_R036_T33RUN_20250525T120714-ql](https://github.com/user-attachments/assets/e0843433-956b-4e61-ac41-ac8b0eeb2f8b)
## Inland Water Detection in Flood-Prone Areas using Sentinel-2 and Unsupervised ML

“A study on NDWI + K-means classification of satellite imagery in Khulna and Mandalay.”
## About the Project 
This project was developed as part of the GEOL0069 AI4EO module at University College London. It focuses on applying machine learning to satellite imagery to detect and classify inland water bodies in both flood-prone and dry regions.The study uses freely available Sentinel-2 imagery and explores the performance of three key techniques in different hydrological settings.
### Techniques Applied 
·NDWI (Normalized Difference Water Index)

·MNDWI (Modified NDWI using Green & SWIR bands)

·K-means clustering (unsupervised learning algorithm)
### 🌍 Study Areas
·Normandy Estuary, France

A coastal deltaic zone located in western Normandy, characterized by dense river networks, tidal inlets, and dynamic hydrology. This region is prone to seasonal flooding due to both river overflow and tidal influence, making it an ideal candidate for assessing flood detection techniques.

·Awbari Region, Libya

A hyper-arid inland area near the town of Awbari in the Libyan Sahara. This region experiences extremely low annual rainfall, sparse vegetation, and minimal surface water presence, making it suitable as a non-flooded baseline. 

-This project uses open-access Sentinel-2 data to compare the performance of NDWI, MNDWI, and K-means clustering for detecting water bodies in both flooded and dry regions. By testing different band combinations and algorithm outputs, it evaluates the accuracy and adaptability of each method under varying environmental conditions.

Additionally, the project uses the CodeCarbon tool to estimate emissions from computation, highlighting the environmental efficiency of the approach.
## Background

Inland water bodies, such as lakes, rivers, and reservoirs, are vital to ecosystems, agriculture, and human livelihoods. However, they are increasingly impacted by climate change and human activities, making accurate and timely monitoring essential (Zeng et al., 2023).

Remote sensing provides an efficient, scalable, and cost-effective approach for surface water detection. This project builds on existing research by applying Sentinel-2 satellite data and machine learning techniques to enhance the identification of inland water bodies.

## Description of the Problem
Problem Overview

Flooding is one of the most widespread and destructive natural hazards, posing significant threats to human lives, infrastructure, and economies. Rapid and accurate flood detection is crucial for disaster response, risk management, and long-term resilience planning.

Conventional flood mapping methods—such as field surveys or drone-based inspections—can be time-consuming, expensive, and spatially limited. In contrast, satellite-based remote sensing offers a scalable, timely, and cost-effective solution for monitoring large areas and detecting water bodies with minimal delay.

This project investigates how to effectively identify inland water in both flood-prone and dry environments using freely available Sentinel-2 imagery and basic unsupervised machine learning techniques. Specifically, it explores:

The effectiveness of NDWI and MNDWI in detecting water bodies across various land types
Whether K-means clustering can enhance or complement traditional water indices
How different spectral band combinations perform under complex conditions such as urban shading or high sediment levels
By combining visual interpretation with quantitative evaluation, the project proposes a lightweight and adaptable framework for flood mapping, particularly suited for regions with limited data or infrastructure.

##  The SENTINEL-2 Satellite

## Reference
1.Zeng, F., Song, C., Cao, Z., Xue, K., Lu, S., Tan, C., & Liu, K. (2023). Monitoring inland water via Sentinel satellite constellation: A review and perspective. ISPRS Journal of Photogrammetry and Remote Sensing, 204, 340–361. https://doi.org/10.1016/j.isprsjprs.2023.09.011

