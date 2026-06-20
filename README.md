# Sparse Machine Learning Approach for Biomarker Detection in Alzheimer's Disease

## Overview

Alzheimer's Disease (AD) is a progressive neurodegenerative disorder that affects memory, cognition, and daily functioning. Early diagnosis is essential for effective disease management and treatment planning.

This project presents a Temporal Group Sparse Additive Learning (TGSAL) framework for identifying significant neuroimaging biomarkers associated with Alzheimer's Disease using MRI data from the ADNI dataset. The proposed framework combines sparse feature selection, nonlinear modeling, and temporal progression analysis to improve diagnostic performance while maintaining model interpretability.

---

## Objectives

- Detect Alzheimer's Disease biomarkers from MRI-derived brain measurements.
- Reduce high-dimensional neuroimaging features using sparse learning.
- Capture nonlinear relationships between biomarkers and disease progression.
- Analyze longitudinal MRI data to identify temporal changes.
- Classify Alzheimer's Disease patients from non-AD subjects with high accuracy.

---

## Datasets

This study utilizes publicly available Alzheimer's Disease datasets containing neuroimaging and clinical information.

### 1. ADNI (Alzheimer's Disease Neuroimaging Initiative)
- Structural MRI
- Clinical assessments
- Demographic information
- Longitudinal follow-up data

### 2. OASIS (Open Access Series of Imaging Studies)
- Structural MRI scans
- Cognitive assessment scores
- Dementia status information

### 3. AIBL (Australian Imaging, Biomarkers and Lifestyle Study)
- MRI and PET imaging
- Clinical and demographic information
- Cognitive measurements

### 4. MIRIAD (Minimal Interval Resonance Imaging in Alzheimer's Disease)
- Longitudinal MRI scans
- Alzheimer's progression analysis

### 5. ICU-AD Dataset
- MRI measurements
- Clinical information
- Disease progression records

---

## Dataset Summary

| Dataset | Subjects | Classes | Data Type |
|----------|----------|----------|----------|
| ADNI | ~1000 | AD, CN, MCI | MRI + Clinical |
| OASIS | ~400 | AD, CN, MCI | MRI |
| AIBL | ~1000 | AD, CN | MRI + PET |
| MIRIAD | ~250 | AD, CN, MCI | MRI |
| ICU-AD | ~300 | AD, CN | MRI + Clinical |

Primary Dataset: ADNI

Additional datasets (OASIS, AIBL, MIRIAD, ICU-AD) are referenced for comparative research and future validation studies.


## Proposed TGSAL Framework

The proposed methodology consists of four stages:

### Stage 1: LASSO Feature Selection
- Removes irrelevant MRI features.
- Reduces dimensionality using L1 regularization.

### Stage 2: Group LASSO Anatomical Sparsity
- Groups MRI features based on anatomical brain regions.
- Preserves structurally relevant biomarkers.

### Stage 3: Sparse Additive Modeling
- Captures nonlinear relationships between MRI biomarkers and disease labels.
- Maintains sparsity and interpretability.

### Stage 4: Temporal Sparse Regression
- Models longitudinal brain changes.
- Identifies progression-related biomarkers.

### Classification
- XGBoost Classifier
- AD vs Rest (CN + MCI)

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib
- Jupyter Notebook

---

## Performance Results

| Metric | Value |
|----------|---------|
| Accuracy | 90.91% |
| Weighted F1 Score | 0.91 |
| ROC-AUC | 0.94 |
| Cross Validation Accuracy | 88.26% ± 0.025 |

---

## Key Biomarkers Identified

- Hippocampus
- Entorhinal Cortex
- Frontal Lobe
- Cingulate Cortex

These regions are strongly associated with Alzheimer's Disease progression.

---


## Installation

```bash
git clone https://github.com/yourusername/Sparse-Machine-Learning-Approach-for-Biomarker-Detection-in-Alzheimers-Disease.git

cd Sparse-Machine-Learning-Approach-for-Biomarker-Detection-in-Alzheimers-Disease

```

---

## Running the Project

```bash
jupyter notebook AD_TGSAL.ipynb
```

Execute all cells to reproduce the experimental results.

---

## Research Contribution

The proposed TGSAL framework:

- Reduces 341 MRI features to 27 discriminative biomarkers.
- Integrates sparse learning and temporal progression modeling.
- Improves interpretability compared to black-box approaches.
- Achieves robust Alzheimer's Disease classification performance.

---

## Author

**G. Vinay Kumar Gupta**  
MCA Final Year  
Anurag University

### Supervisor
Dr. Niteesha Sharma

---

## Citation

If you use this work, please cite:

**Sparse Machine Learning Approach for Biomarker Detection in Alzheimer's Disease**

---

## License

MIT License
