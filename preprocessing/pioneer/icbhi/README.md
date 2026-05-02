# ICBHI 2017 Respiratory Sound Database

## Overview
This folder contains the **ICBHI 2017 Respiratory Sound Database**, a widely used public dataset for research in respiratory sound analysis and classification.

The dataset was introduced as part of the **International Conference on Biomedical and Health Informatics (ICBHI) 2017 Challenge**, and serves as a benchmark for developing and evaluating machine learning models on lung sound data.

---

## Dataset Characteristics

- **Public Benchmark Dataset**  
  The ICBHI 2017 dataset is a standard reference in the field, commonly used to compare model performance across studies.

- **Diverse Respiratory Conditions**  
  Recordings include multiple respiratory states and diseases, such as:
  - Healthy  
  - Asthma  
  - Chronic Obstructive Pulmonary Disease (COPD)  
  - Pneumonia  
  - Bronchiectasis  

- **Annotated Audio Recordings**  
  Each audio file is accompanied by annotations that may include:
  - Respiratory cycle segmentation  
  - Presence of adventitious sounds (e.g., crackles, wheezes)  
  - Diagnostic labels  

- **Controlled Yet Variable Recording Conditions**  
  While collected across multiple subjects and settings, the dataset follows a more structured acquisition protocol compared to purely localized datasets. However, it still contains:
  - Variations in recording devices  
  - Differences in patient conditions  
  - Background noise and artifacts  

- **Pre-segmented and Structured Metadata**  
  The dataset includes predefined splits and structured metadata, making it easier to use for:
  - Supervised learning  
  - Benchmark evaluation  
  - Reproducible experiments  

---

## Notes

- The data is provided in its **original format** as released for the ICBHI 2017 Challenge.  
- No additional preprocessing or modification has been applied in this repository.  
- Users are expected to handle preprocessing, feature extraction, and labeling strategies in downstream pipelines.

---

## Summary
The ICBHI 2017 dataset provides a **diverse and well-annotated collection of respiratory sounds**, making it a reliable benchmark for model development and evaluation. Its combination of structured metadata and real-world variability makes it a strong complement to localized datasets.