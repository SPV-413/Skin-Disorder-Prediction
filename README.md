# Skin Disorder Prediction
Potential reasons and contributing factors for skin disorders are Inflammatory Responses, Keratinization and Epidermal Abnormalities, Immune-Mediated and Autoimmune Factors & other factors. This project analyzes skin disorder data to identify key patterns and trends in skin disorder cases. A predictive model will be developed using various machine learning classifiers to classify patients accurately by type of skin disorder. Additionally, an in-depth analysis will be conducted to justify the choice of models, highlighting the most influential factors contributing to skin disorder. This study seeks to provide data-driven insights that can assist healthcare professionals in early diagnosis and effective intervention strategies.

## Dataset Overview
This dataset contains clinical and histopathological attributes related to six types of skin disorders. Each attribute represents specific characteristics observed in patients, with values indicating the severity or presence of the feature.
- Source: dermatology
- Rows: 366
- Columns: 35 (including the target variable)

### **Clinical Attributes (0–3 unless otherwise specified)**
- **Erythema**
- **Scaling**
- **Definite borders**
- **Itching**
- **Koebner phenomenon**
- **Polygonal papules**
- **Follicular papules**
- **Oral mucosal involvement**
- **Knee and elbow involvement**
- **Scalp involvement**
- **Family history (0 = No, 1 = Yes)**
- **Age**
### **Histopathological Attributes (0–3)**
- **Melanin incontinence**
- **Eosinophils in the infiltrate**
- **PNL infiltrate**
- **Fibrosis of the papillary dermis**
- **Exocytosis**
- **Acanthosis**
- **Hyperkeratosis**
- **Parakeratosis**
- **Clubbing of the rete ridges**
- **Elongation of the rete ridges**
- **Thinning of the suprapapillary epidermis**
- **Spongiform pustule**
- **Munro microabscess**
- **Focal hypergranulosis**
- **Disappearance of the granular layer**
- **Vacuolization and damage of basal layer**
- **Spongiosis**
- **Saw-tooth appearance of retes**
- **Follicular horn plug**
- **Perifollicular parakeratosis**
- **Inflammatory mononuclear infiltrate**
- **Band-like infiltrate**
### **Target Variable**
- **Class (1–6)**: Represents one of the six skin disorder types.
  - **Class 1** : Psoriasis
  - **Class 2** : Seboreic Dermatitis
  - **Class 3** : Lichen Planus
  - **Class 4** : Pityriasis Rosea
  - **Class 5** : Cronic Dermatitis
  - **Class 6** : Pityriasis Rubra Pilaris   
### **Feature Details**
- Family history is binary (0 = No, 1 = Yes) indicating whether any of the six skin disorders were observed in the patient’s family.
- Age is a continuous variable representing the patient’s age.
- Other attributes have values between 0 and 3, where:
  - 0 : Not present
  - 1, 2 : Intermediate levels
  - 3 : Maximum severity

## Project Workflow
### 1. **Exploratory Data Analysis (EDA)**
- Data loading
- Data visualization using **Matplotlib & Seaborn**
### 2. **Feature Engineering**
- **Checking missing values**
- **Checking duplicates**
- **Handling corrupted values**
- **Feature scaling (`StandardScaler`)**
- **Feature Balancing**
  - **SMOTE**
- **Feature Extraction**
  - **PCA method**
- **Splitting dataset into training & testing sets (`train_test_split`)**
  
### 3. **Machine Learning Models**
The project implements multiple machine learning algorithms & one deep learning algorithm for multi-class classification:
- **Logistic Regression**
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **Gradient Boosting Classifier**
- **K-Neighbors Classifier(KNN)**
- **Support Vector Classifier(SVC)**
- **Multi-layer Perceptron (MLP) Classifier**

### 4. **Model Evaluation**
- **Accuracy Score**
- **Confusion Matrix**
- **Classification Report**

## Installation & Usage

### Prerequisites
Ensure you have the following installed:
- Python 3.10 and above
- Jupyter Notebook
- Required libraries (`pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`)

### Running the Notebook
1. Clone the repository:
   git clone https://github.com/SPV-413/Skin-Disorder-Prediction.git
2. Navigate to the project folder:
   cd Skin-Disorder-Prediction
3. Open the Jupyter Notebook:
   jupyter notebook PRCP-1027-Skin Disorder.ipynb

## Results
- --> For this specific dataset and task, the 𝗗𝗲𝗰𝗶𝘀𝗶𝗼𝗻𝗧𝗿𝗲𝗲𝗖𝗹𝗮𝘀𝘀𝗶𝗳𝗶𝗲𝗿 is the most effective model. Its superior accuracy(99%) suggests it captures the underlying patterns in the data most accurately.
- --> Overall, the DecisionTreeClassifier has the ability to balance interpretability, robustness, and efficiency, making it a versatile and effective choice for many classification tasks.
- --> Even models such as LogisticRegression, MLPClassifier, RandomForestClassifier and SVC almost gives similar accuracy(98%) which works well with this classification problem.
- --> Assist healthcare professionals in early diagnosis and effective intervention strategies.

## Important to note
### 1) Justifications for Not Applying Outlier Handling:
- --> Since most features in the dataset are numerical and range between 0 to 3, applying the IQR method for outlier handling is not suitable. The IQR method typically identifies values beyond 1.5 times the interquartile range as outliers, which in this case incorrectly treats the value 3 as an outlier, leading to its removal and introducing NaNs.
- --> Given this limited feature range, the dataset inherently lacks extreme outliers, making outlier handling unnecessary.
### 2) Justifications for Not Applying Hyperparameter Tuning:
- --> Since test accuracy is consistently high (i.e., between 97-98%) across multiple algorithms.
- --> Confusion matrix shows minimal misclassification across all classes.
- --> Stable cross-validation scores across different models indicate No Overfitting present.

## Contact
For any inquiries, reach out via GitHub or email.
