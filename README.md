Machine Learning Prediction of Perineural Invasion in Hepatobiliary Cancers
===========================================================================

Overview
--------

This repository contains the code and resources for a research project aimed at predicting **perineural invasion (PNI)** and **lymphovascular invasion (LVI)** in **hepatobiliary cancers** using machine learning (ML) techniques. The project leverages various ML models, including Logistic Regression, Random Forest, Gradient Boosting, and Neural Networks, to predict tumor invasiveness based on demographic, clinicopathological, and genomic features.
Methodology
-----------

### Data Preprocessing

The dataset includes 433 samples of hepatobiliary cancers. The preprocessing steps include:

-   **Binary Encoding**: Converting categorical "Yes/No" columns to binary (0/1) values.

-   **One-Hot Encoding**: Encoding categorical variables such as tumor stage, sample type, and primary tumor site.

-   **Scaling Continuous Variables**: Standardizing continuous features like BMI, fraction genome altered, and tumor mutational burden (TMB).

### Feature Selection

The following features were used for model training:

-   **Demographic**: Age, sex, BMI.

-   **Clinicopathological**: Tumor stage, lymphovascular invasion, perineural invasion, resection margin, etc.

-   **Genomic**: Fraction genome altered, microsatellite instability (MSI), TMB, and mutation status of genes like BAP1, IDH1, KRAS, TP53, and SMAD4.

### Model Development

Ten machine learning models were developed using Python libraries such as `scikit-learn` and `TensorFlow`. The models include:

-   **K-Nearest Neighbors (KNN)**

-   **Multilayer Perceptron (MLP)**

-   **Support Vector Machine (SVM)**

-   **Logistic Regression**

-   **Decision Tree**

-   **Random Forest**

-   **Gradient Boosting**

-   **AdaBoost**

-   **Gaussian Naive Bayes**

### Hyperparameter Tuning

GridSearchCV was used for hyperparameter optimization. The best parameters for each model were selected based on the area under the curve (AUC) score.

### Model Evaluation

Model performance was evaluated using metrics such as:

-   **Accuracy**

-   **Precision**

-   **Recall**

-   **F1 Score**

-   **ROC AUC**

-   **Confusion Matrix**

SHapley Additive exPlanations (SHAP) analysis was applied to interpret feature contributions.

### Neural Network Implementation

A TensorFlow-based Multilayer Perceptron (MLP) was also implemented for both PNI and LVI prediction. The architecture includes multiple dense layers with dropout and batch normalization for regularization.

Dependencies
------------

The project requires the following Python libraries:

-   `scikit-learn`

-   `TensorFlow`

-   `pandas`

-   `numpy`

-   `matplotlib`

-   `seaborn`

-   `SHAP`

You can install all dependencies using the [`requirements.txt`](requirements.txt) file:
```bash
pip install -r requirements.txt
```
Contributing
------------

Contributions to this project are welcome! If you would like to contribute, please follow these steps:

1.  Fork the repository.

2.  Create a new branch for your feature or bugfix.

3.  Commit your changes.

4.  Submit a pull request.

License
-------

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Acknowledgments
---------------

-   **Dataset**: Memorial Sloan Kettering Cancer Center 2024 HCC dataset.

-   **Libraries**: `scikit-learn`, `TensorFlow`, `SHAP`, and other open-source tools.

-   **Research Team**: Jehad A. Yasin, Abd-alrahman Obeid, Lujia Chen, Mohammad-Amer A. Tamimi, Fares A. Qtaishat, Osama M. Younis, Ahmad E. Saeed, Yousef A. Atehwi, Ramez M. Odat, Mohammad M. Alghaniem, Nada Al-Awamleh, Azhar Saeed, Anwaar Saeed.

Contact
-------

For questions or feedback, please contact:

- **Jehad A. Yasin**, University of Jordan, [jehadamerjehadyasin@gmail.com](mailto:jehadamerjehadyasin@gmail.com)  
- **Abdalrahman Obeid**, World Islamic Sciences and Education University, [abdalrahmanobaid44@gmail.com](mailto:abdalrahmanobaid44@gmail.com)
