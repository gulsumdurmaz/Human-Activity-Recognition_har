Human Activity Recognition (HAR) using Hybrid CNN-LSTM and Classical ML
This repository features a comprehensive comparative study between Classical Machine Learning models and a Hybrid Deep Learning architecture for Human Activity Recognition (HAR) using the UCI HAR Dataset.

📌 Project Overview
The core objective is to classify six distinct human activities (Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying) using two different data processing approaches:
1.	Feature-Engineered Approach: 561-feature vector utilized for Classical ML.
2.	Raw Signal Approach: 3D raw inertial signals utilized for the Hybrid Deep Learning model.

🛠️ Model Architectures
1. Hybrid CNN-LSTM Model
Designed for automatic feature extraction and temporal dependency modeling:
•	CNN Layers: Capture local spatial patterns and motifs from raw accelerometer and gyroscope signals.
•	LSTM Layers: Model long-term temporal dependencies within the movement sequences.
•	Optimization: Trained using GPU acceleration on Google Colab to handle high-dimensional time-series data.
2. Optimized Classical ML Models
Trained on the 561-feature engineered dataset with RandomizedSearchCV for hyperparameter tuning:
•	Logistic Regression: Baseline linear classifier.
•	K-Nearest Neighbors (KNN): Optimized at $K=15$ via cross-validation.
•	SVM (RBF Kernel): High-dimensional boundary optimization.
•	Random Forest: Utilized for Feature Importance analysis to identify key biomechanical indicators.

📊 Evaluation & Visualization
Performance metrics are visualized using a Semi-Bold Pastel color palette for clarity and professional aesthetics:
•	Micro-Average ROC Curve: Comparative performance analysis across all models.
•	Confusion Matrix: Detailed misclassification analysis for the Hybrid model.
•	Feature Importance Ranking: Top 10 features identified by the Random Forest model.
•	Elbow Analysis: Optimal $K$-value determination for the KNN algorithm.

🚀 Technical Implementation
•	Environment: Google Colab (T4 GPU Haccelerator)
•	Preprocessing: Robust scaling and standardization were applied to ensure distance-based models (KNN, SVM) perform optimally.
•	Library Stack: TensorFlow/Keras, Scikit-learn, Seaborn, Matplotlib.

📈 Key Findings
•	The Hybrid CNN-LSTM model demonstrates superior capability in capturing complex patterns directly from raw data without manual feature engineering.
•	Gravity acceleration features remain the most significant predictors in classical models for distinguishing static vs. dynamic activities.
