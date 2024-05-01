# Predictive Modeling for Patient Eligibility to Specific Drug

## Problem Statement
The project addresses the need for a predictive model to determine patient eligibility for a specific drug based on their medical history. This involves analyzing sequential patient data to identify patterns leading to drug eligibility or discontinuation.

## Methodology
1. **Data Preprocessing**: Patient medical records were extracted and processed to create features such as time-based gaps between events and frequency-based occurrence of events.
2. **Feature Engineering**: Time-based features were engineered to capture intervals between consecutive events, while frequency-based features were created using TF-IDF vectorization to quantify event occurrence.
3. **Model Architecture**: A multi-input neural network architecture was implemented, consisting of LSTM layers for sequential data analysis and dense layers for feature integration.
4. **Custom Callbacks**: Custom callbacks were incorporated to monitor model performance during training, including F1-score calculation and early stopping.
5. **Training and Evaluation**: Standard techniques like early stopping and model checkpointing were utilized to optimize model training and evaluation.

## Architecture
- **Input Layers**: Three input layers were used to accommodate different types of features: LSTM for sequential data, time-based features, and frequency-based features.
- **LSTM Layer**: Sequential patient data was analyzed using LSTM layers to capture temporal dependencies.
- **Feature Integration**: LSTM output was concatenated with engineered time-based and frequency-based features for further analysis.
- **Dense Layers**: Dense layers were added for additional feature integration and classification.
- **Custom Callbacks**: Custom callbacks were integrated into the model for monitoring performance and optimizing training.

## Conclusion
The developed model effectively leveraged sequential patient data and engineered features to predict patient eligibility for a specific drug. By incorporating custom callbacks and utilizing a multi-input neural network architecture, the model achieved a significant increase in F1-score, demonstrating its efficacy in patient eligibility prediction.
