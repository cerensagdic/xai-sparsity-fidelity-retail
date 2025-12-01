# xai-sparsity-fidelity-retail
This repository contains the code and analysis for evaluating SHAP and LIME explanations in perishable demand forecasting using MoRF and LeRF curves. The project investigates sparsity, fidelity, and model interpretability in XGBoost and LSTM forecasting models.
The provided notebook automatically downloads the FreshRetailNet-50K dataset from the Hugging Face platform and concatenates the train and evaluation splits into a unified dataset. Due to the differing preprocessing requirements of the XGBoost and LSTM models, the notebook is not intended to be run sequentially in a single pass. Each model requires its own feature engineering pipeline, so the data must be re-downloaded and independently preprocessed before training the second model. The computational environments used for each model are summarised in Table X (see below), highlighting the differences in framework dependencies (e.g., XGBoost vs. TensorFlow/Keras) and explainability libraries (SHAP vs. LIME).
| Package Category           | Seasonal Naive Env. | XGBoost Env. | LSTM Env. |
|---------------------------|----------------------|---------------|-----------|
| **Core & Data Handling**  |                      |               |           |
| Python                    | 3.12.12              | 3.12.12       | 3.12.12   |
| NumPy                     | 2.0.2                | 2.0.2         | 2.0.2     |
| Pandas                    | 2.2.2                | 2.2.2         | 2.2.2     |
| Scikit-learn              | 1.6.1                | 1.6.1         | 1.6.1     |
| SciPy                     | 1.16.3               | 1.16.3        | 1.16.3    |
| Hugging Face Datasets     | 4.0.0                | 4.0.0         | 4.0.0     |
| **Statistics & Viz**      |                      |               |           |
| Statsmodels               | 0.14.5               | 0.14.5        | 0.14.5    |
| Matplotlib                | 3.10.0               | 3.10.0        | 3.10.0    |
| Seaborn                   | 0.13.2               | 0.13.2        | 0.13.2    |
| **ML Frameworks**         |                      |               |           |
| XGBoost                   | —                    | 3.1.1         | —         |
| TensorFlow/Keras          | —                    | —             | 2.19.0    |
| **Optimization & XAI**    |                      |               |           |
| Optuna                    | —                    | 4.6.0         | 4.6.0     |
| Optuna-Integration        | —                    | 4.6.0         | 4.6.0     |
| SHAP                      | —                    | 0.50.0        | —         |
| LIME                      | —                    | 0.2.0.1       | —         |
