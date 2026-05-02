# Hinga

## Overview
This folder contains a **localized dataset of lung sound recordings** collected within the Philippine clinical context. The dataset reflects real-world conditions, including variability in recording environments, patient demographics, and equipment used during acquisition.

The recordings are **unaltered and stored in their raw form**, preserving the natural characteristics of respiratory sounds such as background noise, device artifacts, and environmental factors. This makes the dataset particularly valuable for evaluating how models perform under realistic conditions rather than controlled settings.

---

## Dataset Characteristics

- **Localized Context**  
  All recordings were obtained within a Philippine setting, capturing region-specific clinical and environmental conditions.

- **Raw Audio Format**  
  No preprocessing, filtering, or normalization has been applied. The dataset retains:
  - Background noise  
  - Variations in recording quality  
  - Device-specific artifacts  

- **Clinical Variability**  
  Data was collected across different environments such as hospitals and clinics, introducing natural variability in:
  - Recording devices  
  - Ambient conditions  
  - Patient positioning and cooperation  

- **Label Scope**  
  The dataset includes two classes:
  - **Healthy**
  - **Asthma**

- **Real-World Distribution**  
  The dataset reflects actual patient availability during the collection period rather than a controlled or artificially balanced sampling process.

---

## Limitations

The dataset contains recordings for only two classes: **Healthy** and **Asthma**. This is a result of the conditions during data collection, where no other respiratory cases were successfully recorded despite efforts to gather a broader range of samples.

---

## Summary
The Hinga dataset is characterized by its **raw, real-world audio quality and localized clinical context**. While limited in class diversity, it provides a realistic representation of lung sound recordings as encountered in practice, making it useful for testing model robustness in non-ideal conditions.