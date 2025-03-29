## **Overview**  

This project focuses on the top seven African music industries—Nigeria, South Africa, Ghana, Kenya, Tanzania, DR Congo, and Benin Republic—selected based on market size, cultural influence, and global reach.
By narrowing the scope to these key markets, the machine learning model can better predict song popularity while minimizing noise from less influential regions. 
The analysis includes songs from top artists, verified through Google searches, with all **Forbes’ 20 Biggest African Artists of 2022** originating from these selected countries.

It utilizes various classification models, including Random Forest (RF), Logistic Regression (LR), and XGBoost, to determine whether a song will be popular based on key audio and metadata features.

The dataset includes various musical attributes such as genre, key, loudness, duration, danceability. The goal is to identify patterns that distinguish popular songs from less popular ones and to build models that provide accurate predictions.

## **Key Objectives**  
- **Feature Analysis:** Identifying key attributes that influence song popularity.  
- **Model Comparison:** Evaluating RF, LR, and XGBoost for classification accuracy.  
- **Performance Metrics:** Measuring accuracy, precision, recall, and F1-score.  
- **Insights & Findings:** Understanding why certain models perform better than others.  

---

## **1. Data Analysis & Preprocessing**  
We cleaned and prepared the dataset by handling missing values, normalizing numerical features, and encoding categorical variables.

- **Feature Engineering:** Created derived metrics to enhance model performance.
- **Data Splitting:** Divided data into training and test sets to evaluate generalizability.
- **Class Imbalance Handling:** Addressed imbalance using techniques like SMOTE.

### **Findings:**  
- Certain audio features like genre and danceanility are strong predictors of song popularity.
- Data imbalance (fewer popular songs) affected classification accuracy in some models.
- Feature selection improved model performance by reducing noise.

---

## **2. Model Evaluation**  
We trained three machine learning models—Random Forest, Logistic Regression, and XGBoost—and compared their performance on classifying song popularity.

### **Random Forest (RF)**  
- **Correctly classified:** 1088 (82.24%)  
- **Misclassified:** 235 (17.76%)  
- **Popular songs correctly classified:** 63 (63.00%)  
- **Popular songs misclassified as unpopular:** 37 (37.00%)  
- **Unpopular songs correctly classified:** 1025 (83.81%)  
- **Unpopular songs misclassified as popular:** 198 (16.19%)  

### **Logistic Regression (LR)**  
- **Correctly classified:** 695 (52.53%)  
- **Misclassified:** 628 (47.47%)  
- **Popular songs correctly classified:** 97 (97.00%)  
- **Popular songs misclassified as unpopular:** 3 (3.00%)  
- **Unpopular songs correctly classified:** 598 (48.90%)  
- **Unpopular songs misclassified as popular:** 625 (51.10%)  

### **XGBoost**  
- **Correctly classified:** 984 (74.38%)  
- **Misclassified:** 339 (25.62%)  
- **Popular songs correctly classified:** 78 (78.00%)  
- **Popular songs misclassified as unpopular:** 22 (22.00%)  
- **Unpopular songs correctly classified:** 906 (74.08%)  
- **Unpopular songs misclassified as popular:** 317 (25.92%)  

### **Findings:**  
- **Random Forest performed best overall**, with high classification accuracy for both classes but misclassify  a lot of popular songs compare with LR and XGBoost.
- **Logistic Regression struggled with unpopular songs**, misclassifying more than half.
- **XGBoost balanced between RF and LR**, achieving better results for popular songs but slightly lower accuracy for unpopular songs.

---

## **3. Technical Implementation**  
- **Data Preprocessing:** Cleaning, normalizing, and encoding categorical variables.  
- **Feature Engineering:** We split the genre column using regex to separate multiple genres, then created individual columns where each genre was marked as 1 if present in a song.
- **Model Training & Tuning:** Hyperparameter optimization for RF and XGBoost.  
- **Evaluation Metrics:** Using confusion matrices, precision, recall, and F1-score.  

---

## **4. Next Steps**  
- **Expand the dataset** Include more songs from countries beyond the seven largest music markets to enhance prediction accuracy across a broader range of African markets.
- **Try deep learning models** like neural networks to improve performance.  

---

## **Usage Instructions**  
To run the project, follow these steps:

1. **Clone the repository**  
   ```bash
   git clone https://github.com/peterobarotu/African_Hit_Song_Prediction.git
   ```  
2. **Navigate to the project directory**  
   ```bash
   cd notebooks
   ```  
3. **Run the model training notebook**  
   ```bash
   african_music_prediction.ipynb
   ```  

---

## **License**  
This project is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0) License**. You are free to share and adapt the material as long as proper credit is given.  

For full details, see the [LICENSE.txt](./LICENSE.txt) file.  

