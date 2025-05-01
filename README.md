# GenSafe: Machine Learning & Generative AI for Construction Accident Severity Prediction

A hybrid AI system that leverages Machine Learning and Generative AI to predict the severity of construction site accidents and generate automatic safety reports. Developed as part of CNST 6308 – Data Analysis in Construction Management at the University of Houston.

## 📌 Project Overview

Construction sites are high-risk environments where accurate prediction of accident severity is crucial for proactive safety management. This project introduces **GenSafe**, a dual-layered solution:

- **Machine Learning Layer**: Classifies accidents as **fatal** or **non-fatal** based on features such as environment, human behavior, and task type.
- **Generative AI Layer**: Uses OpenAI's GPT-3.5 Turbo to convert structured prediction results into narrative safety reports with actionable recommendations.

## 🧠 Core Technologies

- **Python** (data processing & modeling)
- **Scikit-learn**, **XGBoost**, **LightGBM**, **CatBoost** (classification)
- **OpenAI GPT-3.5 Turbo** (generative text synthesis)
- **SHAP**, **Permutation Importance** (feature interpretability)
- **Pandas**, **Matplotlib**, **Seaborn** (EDA & visualization)

## 📊 Dataset

- **Source**: Construction accident records
- **Size**: ~4,800 records, 25 features
- **Target Variable**: `Degree of Injury` (0 = Non-fatal, 1 = Fatal)
- **Features**: Event Type, Fall Height, Task Assigned, Human Factor, Environmental Factor, Project Cost, Year, etc.

## 🔍 Key Features

- Robust preprocessing including:
  - Handling missing values
  - One-hot and frequency encoding
  - Feature scaling and outlier detection
- Multiple ML models with hyperparameter tuning:
  - Logistic Regression, Random Forest, Decision Tree, SVM, KNN, Naive Bayes, XGBoost, LightGBM, CatBoost
- **Top Accuracy**:
  - CatBoost / XGBoost / LightGBM: **92%**
- Automated textual reporting using **OpenAI GPT**:
  - Custom safety narratives
  - Risk-specific suggestions

## 📈 Results

| Model        | Accuracy | F1-Score (Fatal) | F1-Score (Non-Fatal) |
|--------------|----------|------------------|----------------------|
| CatBoost     | 92%      | 0.89             | 0.93                 |
| XGBoost      | 92%      | 0.89             | 0.93                 |
| LightGBM     | 92%      | 0.89             | 0.93                 |
| RandomForest | 90%      | 0.88             | 0.92                 |
| SVM          | 89%      | 0.87             | 0.91                 |

## 💡 Generative AI Component

After ML-based classification, the top features are passed as prompts to OpenAI's GPT-3.5 Turbo to generate accident summaries. These reports assist safety officers in understanding risk factors and planning proactive safety measures.

**Example Output**:
> _“The accident involved a fall from 5 meters during roofing work under rainy conditions. Human factor identified: Inattention. This scenario is predicted to result in a fatal injury. Recommended actions: increase supervision, use rainproof gear, and reinforce awareness training.”_

## 📚 Future Work

- Integrate real-time IoT sensor data
- Expand to multilingual support for safety reports
- Use generative AI to create safety training materials
- Enable web dashboard with live monitoring and risk updates

**Faculty Guide**: Dr. Lu Gao, University of Houston

## 🏫 Course Info

**Course**: CNST 6308 – Data Analysis in Construction Management  
**Institution**: University of Houston  
**Semester**: Spring 2025

## 📄 License

This project is for academic and demonstration purposes. Contact contributors for usage inquiries.

---

