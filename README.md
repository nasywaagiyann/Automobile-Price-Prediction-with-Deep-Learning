# Deep Learning Regression - Automobile Price Prediction

## 📄 Project Description

This project aims to build a regression model using an Artificial Neural Network (ANN) to predict car prices based on various features such as technical specifications and vehicle characteristics. The model is developed using TensorFlow and Keras.

## 🧰 Tools & Libraries

* Python
* Pandas, NumPy, Matplotlib, Seaborn, Missingno
* Scikit-learn (for preprocessing and train-test split)
* TensorFlow & Keras

## 📚 Workflow

1. **Import Libraries**
   Standard libraries are used for data handling, visualization, preprocessing, and deep learning.

2. **Load Dataset**
   The *Automobile\_data.csv* dataset is loaded and its structure is examined.

3. **Exploratory Data Analysis (EDA)**

   * Analyzing data structure and descriptive statistics
   * Handling missing values:

     * Mean imputation for numerical data with < 75% missing values
     * Mode imputation for categorical data
     * Dropping columns with > 75% missing values (not applicable in this case)

4. **Feature Engineering**

   * Label Encoding for categorical features
   * StandardScaler for normalizing numerical features
   * Splitting the dataset into training and testing sets (80:20 split)

5. **Modeling**

   * ANN architecture with multiple Dense layers, Batch Normalization, and Dropout
   * Optimizer: Adam with a learning rate of 0.001
   * Loss function: Mean Squared Error (MSE)
   * Model training monitored using EarlyStopping and ModelCheckpoint

6. **Model Evaluation**

   * Evaluated on the test set
   * Metrics used: Loss (MSE) and Mean Absolute Error (MAE)

7. **Inference (New Data Prediction)**

   * Encoding and scaling applied to new input before prediction
   * Produces predicted car price as output

## 📊 Results

* **Test Loss (MSE):** \~2529.8472
* **Test MAE:** \~32.6620
* The model demonstrates reasonably good performance with an average error of ±33 units of price.
