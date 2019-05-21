# Kaggle-Santander-Customer-Transaction-Prediction

*A collection of work related to the [Santander Customer Transaction Prediction](https://www.kaggle.com/c/santander-customer-transaction-prediction) on [Kaggle](https://www.kaggle.com/).*

*Language:* Python

Currently, the repository contains the following files:

1. README.md -- this file.

2. Santander_EDA_1_Simple_Modeling.ipynb -- a Jupyter notebook containing introductory level exploratory data analysis of the data and some baseline modeling. The list of models: 
    * Logistic Regession 
    * Elastic Net 
    * Gaussian Naive Bayes
    * Linear Discriminant Analysis (LDA)
    * Quandratic Discriminant Analysis (QDA).
Please note that **the table of content links do not work on Github**  -- you need to download the notebook and view it locally to be able to use the links.

3. logistic-regression-with-new-features-feather.ipynb -- a Jupyter notebook introducing some additional numerical feature variables with Logistic Regression model. The notebook also illustrates the usage of the `feather` file format for saving and loading data. The notebook is [publically available](https://www.kaggle.com/graf10a/logistic-regression-with-new-features-feather) on the Kaggle website.

4. data_serialization.py -- a Python script that assigns data types to the columns of the testing and training data
      * Assigns data types to the columns of the training and testing data sets to reduce memory usage (50% reduction).
      * Separates the *target* and *ID_code* columns from the training and testing data.
      * Serializes the data saving them into the feather file format. Reading feather files from the disk happens much faster than reading CSV files, so we can use the output of this script every time when we need to read the data instead of reading the CSV's.
      * For convenience, the column names of test and train are saved as pickle files.
      
5. Eli5.ipynb -- a Jupyter notebook computing ELI5 weights for LightGBM model trained on the competition data. The notebook is [publically available](https://www.kaggle.com/graf10a/santander-eli5-weights-for-lightgbm) on the Kaggle website. The Kaggle version is a bit better because it shows the color coding for the weights (green: helpful, white: neutral, red: detrimental).

6. umap.png -- the UMAP image of the raw data.

7. T_SNE.png -- the T-SNE image of the raw data.
