# Heart Disease Prediction Model

## Overview
A machine learning model developed to predict 
cardiovascular disease risk using patient clinical 
data. Built using Python and scikit-learn, achieving 
83.61% classification accuracy on the UCI Heart 
Disease Dataset.

---

## Dataset
- **Source:** UCI Machine Learning Repository
- **Size:** 303 patients, 13 clinical features
- **Target:** Binary classification 
  - 1 = Heart disease present
  - 0 = Heart disease absent

---

## Clinical Features

| Feature | Description | Measurement |
|---------|-------------|-------------|
| Age | Patient age | Years |
| Sex | Biological sex | 1=Male, 0=Female |
| Chest Pain Type | Pain classification | 0=Typical Angina, 1=Atypical, 2=Non-Anginal, 3=Asymptomatic |
| Resting BP | Blood pressure at rest | mmHg |
| Cholesterol | Serum cholesterol | mg/dl |
| Fasting Blood Sugar | Post-fast glucose | 1=>120mg/dl, 0=Normal |
| Resting ECG | Electrocardiogram at rest | 0=Normal, 1=ST-T Abnormality, 2=LV Hypertrophy |
| Max Heart Rate | Peak exercise heart rate | bpm |
| Exercise Angina | Chest pain during exercise | 1=Yes, 0=No |
| ST Depression | ECG change during exercise | Continuous 0-6.2 |
| ST Slope | ST segment direction | 0=Upsloping, 1=Flat, 2=Downsloping |
| Major Vessels | Visible vessels on scan | 0-3 |
| Thalassemia | Blood oxygen disorder | 1=Normal, 2=Fixed Defect, 3=Reversible Defect |

---

## Methodology

### Algorithm
Random Forest Classifier
- 100 decision trees
- Majority voting system
- Handles mixed data types well

### Data Split
- 80% Training (242 patients)
- 20% Testing (61 patients)

---

## Results

### Accuracy: 83.61%

### Confusion Matrix
| | Predicted Negative | Predicted Positive |
|--|------------------|------------------|
| **Actually Negative** | 24 ✅ | 5 ❌ |
| **Actually Positive** | 5 ❌ | 27 ✅ |

### Key Finding - Top Predictors
| Rank | Feature | Significance |
|------|---------|-------------|
| 1 | ST Depression | Strongest predictor |
| 2 | Maximum Heart Rate | Very significant |
| 3 | Major Vessels | Very significant |
| 4 | Chest Pain Type | Significant |
| 5 | Thalassemia | Significant |

---

## Key Insights

### Clinical
- ST Depression was the strongest single predictor
- Asymptomatic patients can carry a significant hidden risk
- Model confidence varied (62-74%), reflecting 
  real clinical complexity
- False negatives remain a critical concern 
  in clinical application

### Technical
- Importance of train/test splitting for unbiased evaluation
- Model uncertainty quantification is as important 
  as overall accuracy
- Data preprocessing significantly impacts model performance

### Limitations
- Small dataset (303 patients)
- Binary classification oversimplifies clinical reality
- Requires validation on larger, diverse datasets
- Not suitable for clinical use without further development

---

## Libraries
- Python 3
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

---

## Future Development
- Expand dataset size
- Compare multiple algorithms
- Implement cross-validation
- Develop web interface
- Explore deep learning approaches

---

## References
UCI Machine Learning Repository
Heart Disease Dataset
Collected by:
- Cleveland Clinic Foundation
- Hungarian Institute of Cardiology  
- University Hospital Zurich
- VA Medical Centre Long Beach
