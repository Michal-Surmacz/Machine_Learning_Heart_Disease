# Machine_Learning_Heart_Disease

## **Introduction**

All project available on: XXX

### **Goal**

The goal of the project is to develop a predictive model that can accurately identify people with heart disease. Given the serious implications of misdiagnosis (missed patients, eligible for treatment), the main goal is to ensure that the model identifies all potential patients, making the sensitivity (recall) metric of the classifier for the positive class a key indicator for assessing its effectiveness.

### **Classification Problem**

Classification problem involves categorizing data into predefined classes or labels. This type of problem is often referred to as "supervised learning" because the algorithm learns from labeled data—data that comes with known categories.

## **Dataset**

### **Source**

The dataset is sourced from [**Kaggle - A Guide to any Classification Problem**](https://www.kaggle.com/code/durgancegaur/a-guide-to-any-classification-problem/input?select=heart.csv).

### **Data Description**

The dataset contains the following columns:
- **`Age`**: age of the patient [years]
- **`Sex`**: sex of the patient [M: Male, F: Female]
- **`ChestPainType`**: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
- **`RestingBP`**: resting blood pressure [mm Hg]
- **`Cholesterol`**: serum cholesterol [mm/dl]
- **`FastingBS`**: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
- **`RestingECG`**: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
- **`MaxHR`**: maximum heart rate achieved [Numeric value between 60 and 202]
- **`ExerciseAngina`**: exercise-induced angina [Y: Yes, N: No]
- **`Oldpeak`**: oldpeak = ST [Numeric value measured in depression, mm]
- **`ST_Slope`**: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
- **`HeartDisease`**: output class [1: heart disease, 0: Normal]

## **Result**

![Result](https://github.com/user-attachments/assets/4a5aba9b-a0f6-47a6-ac67-a4d5e0c0fc55)

### **Description**

This bar plot, titled "Comparison of Model Accuracy," compares the accuracy scores of different machine learning models. Here’s an analysis of the chart:
- `RandomTreeClassifier` and `LogisticRegression` have the highest accuracy, 0.89 and 0.88. This suggests these models are performing the best in terms of correctly classifying samples.
- `KNeighborsClassifier` follows closely with an accuracy of 0.86, showing strong performance.
- `Naive Bayes` also performs fairly well with an accuracy of 0.85.
- `SVM`has an accuracy of 0.84, which is decent but lower than the top performers.
- `DecisionTreeClassifier` and `MixedNB` have accuracies of 0.83, slightly below `SVM`.
- `CategoricalNB` shows the lowest accuracy at 0.82.


This bar plot, titled "Comparison of Model AUC," compares the Area Under the Curve (AUC) scores for different models. Here’s an analysis of the chart:
- `KNeighborsClassifier`, `RandomTreeClassifier` and `SVM` all achieved the highest AUC score of 0.94. This suggests these models are strong at distinguishing between classes.
- `Naive Bayes`, `CategoricalNB` and `LogisticRegression` each have an AUC of 0.92, showing consistent but slightly lower performance than the top group.
- `DecisionTreeClassifier` has a notably lower AUC score of 0.84, indicating it’s less effective in this metric compared to other models.


This bar plot titled "Comparison of Precision, Recall, and F1-score for Class 0" provides a detailed look at the performance of each model on Class 0 in terms of precision, recall, and F1-score. Here’s an analysis:
1. Precision:
   - `RandomTreeClassifier` has the highest precision for Class 0 at 0.85, indicating it’s the most accurate in predicting positive instances for this class.
   - Other models, like `LogisticRegression` and `KNeighborsClassifier`, have relatively high precision, around 0.81 to 0.83.
   - `CategoricalNB` and `MixedNB` have the lowest precision scores, at 0.74 and 0.76, respectively.
2. Recall:
    - `RandomTreeClassifier` stands out with the highest recall of 0.97 for Class 0, showing it captures almost all positive cases for this class.
    - Most other models have recall values between 0.86 and 0.88, which is strong performance.
    - `Naive Bayes` and `CategoricalNB` have lower recall values, around 0.78 to 0.80.
3. F1-score:
    - `RandomTreeClassifier` again leads with an F1-score of 0.86, balancing both high precision and recall.
    - `LogisticRegression` and `KNeighborsClassifier` also have respectable F1-scores, around 0.83 and 0.84, indicating decent balance between precision and recall.
    - `CategoricalNB` and `MixedNB` have the lowest F1-scores for Class 0, reflecting weaker performance.

### **Overall**:
`RandomTreeClassifier` is the best-performing model for Class 0, excelling in recall and achieving a balanced F1-score.
Models like `KNeighborsClassifier` and `LogisticRegression` show decent balance, while `Naive Bayes`, `CategoricalNB`, and `MixedNB` lag behind in precision and F1-scores.

This bar plot titled "Comparison of Precision, Recall, and F1-score for Class 1" provides a detailed look at the performance of each model on Class 1 in terms of precision, recall, and F1-score. Here's an analysis:
1. Precision:
    - Both `LogisticRegression` and `Naive Bayes` have the highest precision at 0.91 for Class 1.
    - Most other models maintain high precision around 0.89-0.90.
    - `SVM` has the lowest precision at 0.87, though still maintaining a strong performance overall.
2. Recall:
    - `RandomTreeClassifier` shows the highest recall at 0.89 for Class 1, demonstrating strong ability to capture positive cases.
    - `LogisticRegression` and `SVM` follow closely with recall values of 0.87 and 0.86 respectively.
    - `CategoricalNB` has the lowest recall at 0.78, showing it misses more positive cases than other models.
3. F1-score:
    - `RandomTreeClassifier` leads with the highest F1-score of 0.90, showing the best balance between precision and recall.
    - `LogisticRegression` follows closely with an F1-score of 0.89.
    - `CategoricalNB` has the lowest F1-score at 0.83, reflecting its lower recall despite decent precision.

Most models demonstrate strong overall performance with scores above 0.80 across all metrics, with `RandomTreeClassifier` and `LogisticRegression`consistently performing at the top across all three metrics.

### **Summary**

In summary, RandomTreeClassifier and LogisticRegression are the best models in this analysis, with RandomTreeClassifier excelling slightly in recall and F1-score for both classes. These models would be recommended for deployment in a classification task where both accuracy and the balance between precision and recall are essential.
