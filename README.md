# EQ-77(thesis)
# Earthquake Magnitude Prediction Using Machine Learning and Deep Learning Models

This project involves predicting earthquake magnitudes (`mag`) using various machine learning and deep learning models. The models were trained on seismic and geospatial data and evaluated using key performance metrics such as **Mean Squared Error (MSE)** and **R² Score**.

---

## Project Workflow

### 1. Data Preprocessing
- **Loaded the dataset**: Earthquake data with features such as latitude, longitude, depth, number of reporting stations (`nst`), gap, minimum distance (`dmin`), and root-mean-square error (`rms`).
- **Created a new column**: `danger` (1 if magnitude > 3.5, else 0) for reference.
- **Selected relevant features**: Latitude, longitude, depth, nst, gap, dmin, and rms.
- **Set the target value**: `mag` (Earthquake Magnitude) for regression models.

---

### 2. Splitting the Data
- **Split the dataset** into **training and testing sets** using an 80-20 split to ensure fair model evaluation.

---

### 3. Models Implemented
We implemented several machine learning and deep learning models to predict the earthquake magnitude (`mag`):

#### 3.1. Machine Learning Models
1. **Linear Regression**  
   - A simple linear model to predict earthquake magnitude.
   
2. **Ridge Regression**  
   - Linear model with L2 regularization to prevent overfitting.
   
3. **Lasso Regression**  
   - Linear model with L1 regularization for feature selection.
   
4. **Random Forest Regressor**  
   - An ensemble method using multiple decision trees.

5. **Support Vector Regressor (SVR)**  
   - A regression model based on support vectors.

#### 3.2. Deep Learning Model
6. **Convolutional Neural Network (CNN)**  
   - A deep learning model designed to capture complex patterns in the data.
   - CNN model structure:
     - 1D Convolution Layer with 64 filters
     - MaxPooling Layer
     - Dropout for regularization
     - Dense Layer with ReLU activation
     - Output Layer for regression (no activation function)

---

### 4. Model Evaluation
We evaluated the models using:
- **Mean Squared Error (MSE)**: Measures average squared difference between actual and predicted values.
- **R² Score**: Coefficient of determination; how well the model captures variance in the data.

---

### 5. Results Comparison

| **Model**               | **MSE**   | **R² Score** |
|-------------------------|-----------|--------------|
| Ridge Regression        | 0.016150  | 0.907748     |
| Linear Regression       | 0.031570  | 0.819666     |
| SVR                     | 0.028825  | 0.835344     |
| CNN                     | 0.062044  | 0.645585     |
| Random Forest Regressor | 0.042775  | 0.755660     |

---

### 6. Key Observations
- **Ridge Regression** performed the best with **MSE = 0.016150** and **R² Score = 0.907748**.
- **CNN** struggled with the **highest MSE (0.062044)** and the **lowest R² Score (0.645585)**, indicating difficulty in capturing the underlying patterns.
- **SVR and Random Forest Regressor** offered decent performance, making them useful alternatives to linear models.

---
### 7. Video


https://github.com/user-attachments/assets/87c19438-18fb-484f-a1ed-f644643893cf



---
### 8. How to Run the Project

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/earthquake-magnitude-prediction.git
   cd earthquake-magnitude-prediction

