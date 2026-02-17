# Preprocessing Steps

## Overview
This document outlines the preprocessing pipeline for the respiratory sound analysis project using the ICBHI dataset. The preprocessing involves audio normalization, metadata processing, and stratified patient-level data splitting.

## 1. Audio Loading and Normalization
- **Input**: Raw audio files from the ICBHI Respiratory Sound Database
- **Sample Rate**: 4,000 Hz
- **Processing**:
  - Load audio using librosa
  - Convert to float32
  - RMS normalization to standardize volume levels
  - Clip values to [-1, 1] range to prevent clipping artifacts

## 2. Metadata Processing
- **Patient Diagnosis Data**: Read `patient_diagnosis.csv` containing patient IDs and disease classifications
- **Annotation Data**: Process all `.txt` annotation files containing:
  - Breath cycle start/end times
  - Crackle and wheeze annotations
  - Patient IDs extracted from filenames
- **Data Integration**: Merge annotations with patient diagnoses

## 3. Data Quality Control
- **Rare Class Filtering**: Remove disease classes with ≤3 unique patients to ensure statistical reliability
- **Patient-Level Deduplication**: Ensure no patient appears in multiple data splits

## 4. Stratified Patient-Level Splitting
- **Strategy**: Patient-level splits to prevent data leakage (same patient in train/test/val)
- **Distribution**:
  - At least one patient per disease class in each split (train/test/val)
  - Remaining patients split 80/10/10 (train/test/validation)
  - Maintain disease class balance across splits
- **Output**: Separate DataFrames for training, testing, and validation sets

## Configuration Parameters
- `SEG_LEN`: 3 seconds (segment length for analysis)
- `SR`: 4,000 Hz (target sample rate)
- `TARGET_COUNT`: 500 samples per class (for data augmentation)
- Random seed: 42 (for reproducible splits)

