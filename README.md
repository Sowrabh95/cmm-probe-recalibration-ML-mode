# CMM Probe Recalibration Classification Model
Link to the publication https://www.sciencedirect.com/science/article/pii/S2212827124001665
The detail description of the model is provided in the research article published in Procedia CIRP.


**Project Overview**

This project aims to develop a machine learning-based predictive model for determining the optimal time to recalibrate a Coordinate Measuring Machine (CMM) probe. The objective is to minimize unnecessary calibrations while ensuring accurate measurements, thereby improving efficiency, reducing downtime, and enhancing sustainability in manufacturing processes.

**1. Data Collection**

Sources:

CMM Probe Usage Data: Sensor-based logs from touch-trigger probes.

Calibration Records: Historical data from previous probe calibrations.

Environmental Conditions: Temperature, humidity, vibration levels during measurement.

Workpiece Characteristics: Material hardness, surface properties.

Operator Decisions: Human-appraiser-based calibration records.

**2. Data Preprocessing**

Steps:

Handling Missing Values: Imputation techniques for incomplete records.

Feature Scaling: Normalization and standardization applied to numerical values.

Categorical Encoding: One-hot encoding for categorical features like material type.

Data Splitting: Divided into training (70%), validation (15%), and testing (15%) datasets.

**3. Model Selection & Training**

Algorithm: Random Forest Classifier: Chosen for its robustness in handling mixed data types and its interpretability.

Hyperparameter Tuning: Max Depth & Number of Trees: Optimized using Grid Search Cross Validation.

Feature Importance Analysis: Identified key contributors to calibration necessity.

Data Augmentation: SMOTE (Synthetic Minority Over-Sampling Technique): Addressed class imbalance by generating synthetic samples for underrepresented cases.

**4. Model Evaluation & Fine-Tuning
**
Metrics Used:

Confusion Matrix: Visualized prediction performance.

F1-score, Precision, Recall: Evaluated model accuracy and reliability.


![Test accuracy](https://github.com/user-attachments/assets/e8e96417-b83a-4f79-b320-45e64d849e51)


Cross-Validation: Ensured robustness across different data subsets.

Improvements Post-Tuning:

Increased model recall for minority class predictions.

Reduced false positives and false negatives in calibration decisions.

**5. Deployment & Integration**

Deployment Strategy:

API-Based Model: Exposed via a lightweight API for real-time predictions.

Integration with CMM Systems: Enabled automated decision support for calibration.

User Interaction:

Input parameters include probe usage metrics, environmental factors, and historical calibration data.

Output: Binary classification (1 = Recalibration Required, 2 = No Recalibration Needed).

**6. Results & Impact**

Optimized Calibration Frequency: Reduced unnecessary calibrations while maintaining quality.

Time & Cost Savings: Improved efficiency of the measurement process.

Sustainability: Lower energy consumption by reducing excessive probe qualifications.
Test accuracy

