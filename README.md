# Motor-Imagery-based-Daily-Activities-interface

1.	Data preparation (training and testing sets) and preprocessing used:
- Data Preparation:
  - Training and Testing Sets: The data was divided into training and testing sets using an 80/20 split. Specifically, 230 samples were used for training and 58 samples for testing.
- Preprocessing Steps:
  - Channel Selection: EOG channels were removed from the raw data.
  - Filtering: Applied bandpass filter between 14-30 Hz and notch filter at 50 Hz.
  - Epoch Creation: Created epochs from the raw data based on events.
  - Normalization: Normalized the features between 0 and 1.

2.	Feature Extraction methods used.:
- Common Spatial Patterns (CSP):
  - CSP was used to extract discriminative features from the EEG data. This method helps in enhancing the signal-to-noise ratio by emphasizing the variance between different classes of motor imagery.

3.	Classifier used and its parameters:
- Multiple classifiers tested to determine the best performing model:
- Support Vector Machine (SVM):
  - Kernel: Linear
  - Parameters: Tuned C and gamma using GridSearchCV

- Support Vector Machine (SVM):
  - Kernel: RBF
  - Best Parameters: C=100 

- Random Forest Classifier:
  - Parameters: n_estimators=100, max_depth=6

- Logistic Regression:
  - Parameters: C=4

- XGBoost Classifier:
  - Parameters: gamma=0.001, n_estimators=150
