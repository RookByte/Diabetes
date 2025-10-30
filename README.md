# Diabetes
# Diabetes Prediction with KNN 🤖

This project focuses on predicting whether a person has diabetes based on their medical measurements using the **K-Nearest Neighbors (KNN)** algorithm.

## Dataset 📊
- **File:** `diabetes.csv`
- **Rows:** 768
- **Features:** 8 numeric features + 1 target column (`Outcome`)
- **Target:** `Outcome` → 0 = non-diabetic, 1 = diabetic

## Workflow 🛠️

### 1. Data Cleaning 🧹
- Checked for **missing or zero values** in the dataset.
- Replaced invalid zeros with the **mean or median** of the respective column.

### 2. Shuffling & Splitting 🔀
- Shuffled the dataset to remove any inherent order.
- Split the data into **training set (80%)** and **test set (20%)**.

### 3. Feature Scaling ⚖️
- Standardized features to have **mean = 0** and **standard deviation = 1** using `StandardScaler`.
- Scaling helps KNN perform better, since **distances are sensitive to feature magnitudes**.

### 4. KNN Implementation ⚡

#### a) Manual KNN (Without scikit-learn) 💡
- Calculated **Euclidean distances** between test samples and training samples.
- Selected the **k = 5 nearest neighbors**.
- Predicted the class by **majority vote** of the neighbors.

#### b) KNN with scikit-learn 🛠️
- Used `KNeighborsClassifier` for comparison.
- Applied standardization with `StandardScaler`.
- Verified that the scikit-learn model gives similar results to the manual implementation.

### 5. Evaluation 📈
- Compared predictions to actual labels on the test set.
- Calculated **accuracy** and **F1-score**.
- Checked **precision** and **recall** for each class to see how well the model identifies diabetic vs non-diabetic cases.

## Results 🏆
- **Manual KNN Accuracy:** ~72%
- **scikit-learn KNN Accuracy:** ~76%
- Manual implementation helped in understanding the inner workings of KNN and the effect of **scaling** and **distance calculation**.
