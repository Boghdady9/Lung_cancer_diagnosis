# Lung Cancer Diagnosis: Small Lung Nodule Dataset  
[![Kaggle Dataset](https://img.shields.io/badge/Kaggle-Dataset-blue)](https://www.kaggle.com/datasets/yasserhessein/small-lung-nodule-lung-cancer-dataset)  

This project builds upon the **Small Lung Nodule Lung Cancer Dataset** to classify small lung nodules, aiming to enhance early diagnosis of lung cancer. Our approach outperforms the baseline performance outlined in the referenced manuscript in several aspects, offering a robust decision-support tool for radiologists.  

---

## Dataset Overview  
This dataset accompanies the manuscript:  
*"Radiomics-Based Decision Support Tool Assists Radiologists in Small Lung Nodule Classification and Improves Lung Cancer Early Diagnosis."*  

- **Dataset Link**: [Small Lung Nodule Dataset](https://www.kaggle.com/datasets/yasserhessein/small-lung-nodule-lung-cancer-dataset)  

The dataset includes **990 nodules from 810 patients**, annotated with features extracted from multi-region CT segmentations using **TexLab2.0**. It introduces a predictive radiomics model, **Small Nodule Radiomics Predictive Vector (SN-RPV)**, developed through LASSO regression for nodule classification.  

---

## Objectives  
- **Enhance Radiologist Evaluation**: Support radiologists in lung nodule classification and improve early cancer detection.  
- **Risk Stratification**: Categorize lung nodules into **Low Risk**, **Intermediate Risk**, and **High Risk** groups.  
- **Quantifiable Improvements**: Offer significant enhancements in missed or delayed cancer diagnoses compared to radiologists.  

---

## Workflow  
### Radiologist Evaluation  
1. **Initial Assessment**: Radiologists evaluate lung nodules using CT scans.  
2. **Risk Categorization**: Nodules are stratified into three categories based on SN-RPV:  
   - **Low Risk**: Unlikely to be cancerous.  
   - **Intermediate Risk**: Moderate likelihood of malignancy.  
   - **High Risk**: High probability of cancer.  

### Management Decisions  
- **Low Risk**:  
  - SN-RPV High → Place patient in a "Safety Net" with no further follow-up.  
- **Intermediate Risk**:  
  - SN-RPV High → Early surveillance CT to monitor growth and enable early diagnosis.  
- **High Risk**:  
  - Aggressive investigation, including biopsy or advanced imaging.  

![Radiologist Workflow](https://media.springernature.com/m312/springer-static/image/art%3A10.1038%2Fs41416-023-02480-y/MediaObjects/41416_2023_2480_Fig2_HTML.png)  

---

## Results and Improvements  
### Quantifiable Improvements  
Our approach outperforms the referenced manuscript in several key metrics:  
- Improved **AUC** for malignancy prediction across multiple methods and models.  
- Enhanced accuracy and sensitivity for detecting small lung nodules.  
- Achieved **73% accuracy** and a **66.67% improvement** in missed or delayed cancer diagnoses compared to the average radiologist.  

### Model Performance  
| Feature Selection Method | Model             | Accuracy | Sensitivity | Specificity | AUC    |
|---------------------------|-------------------|----------|-------------|-------------|--------|
| Boruta                   | SVC               | **0.7323**   | **0.8056**      | 0.6364      | **0.7775** |
| Boruta                   | Neural Network    | 0.6850   | 0.6944      | 0.6727      | 0.7636 |
| Mutual Information       | Neural Network    | 0.7244   | 0.7639      | 0.6727      | 0.7662 |
| XGBoost                  | Neural Network    | 0.7323   | 0.8056      | 0.6364      | 0.7619 |

### Comparison with Radiologists  
The test set's **73% accuracy** surpassed the average performance of six thoracic radiologists, offering earlier and more reliable cancer detection.  

---

## Future Directions  
- **Expand Validation**: Incorporate external datasets for broader evaluation.  
- **Deep Learning**: Explore CNNs for feature extraction and classification.  
- **Personalized Decision Tools**: Enhance decision-support tools for tailored patient management.  

