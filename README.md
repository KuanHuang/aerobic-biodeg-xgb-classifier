# Aerobic biodegradation prediction with XGBoost Classifier

A machine learning model for the aerobic biodegradation prediction (classification) based on XGBoost as the major ML algorithm and MACCS fingerprint as the chemical representation. The repository contains all the related datasets, codes, and model files.

An online predictor was published on [**Aropha AI**](https://www.ai.aropha.com/) at https://www.ai.aropha.com/aerobic-biodegradation/classification/about.html


## Basic information
### Dataset:
The classification model was based on more than 3,000 data points with SMILES strings as the inputs and the class (0 or 1) as the output. Only ready biodegradation data with time of 28 and principles of closed bottle test, closed respirometer, and CO2 evolution were considered.

### ML algorithms:
A total of 14 ML algorithms were examined to find the best one, including K nearest neighbors, Linear support vector machine (SVM), Radial basis function SVM (RBF SVM), Gaussian process, Neural net multi-layer perceptron classifier, Decision tree, Random forest, Bagging, Adaptive boosting, Gradient boosting, XGBoost, Extra tree, Gaussian Naive Bayes, Quadratic discriminant analysis.

XGBoost was found to be the best one.

### Chemical representation:
MACCS fingerprints

### Other notes:
Data balancing was performance as the two classes were not well balanced. Bayesian optimization was conducted for tuning the model hyperparameters. Chemical similarity calculation was performed using the fingerprint similarity based on Tanimoto index to determine the model applicability domain.

## Use the online predictor on Aropha AI
<img src="/doc/presentation_pysirc.gif?raw=true" align="center">

## Download files to run locally
In addition to using the online predictor, we also encourage you to try the model files locally with your data to have command-line controls over the prediction.
### Dependencies
<ul>
<li><b>RDkit:</b> Draw molecules and convert smiles to fingerprints.</li>
<li><b>Numpy:</b> Create matrices and mathematical operations.</li>
<li><b>Pandas:</b> Data manipulation.</li>
<li><b>Scikit-learn:</b> Framework to perform ML models.</li>
<li><b>XGBoost:</b> Perform a XGBoost model.</li>
<li><b>Pickle:</b> Load the model files.</li>
</ul>

### Install the dependencies
#### RDKit
The installation of RDKit using `pip` had been challenging. However, the recent update made it super simple with the following command:
```
pip install rdkit-pypi
```
or traditionally, using `conda`: 
```
conda install -c conda-forge rdkit
```
#### Others
```
pip install numpy
pip install pandas
pip install -U scikit-learn
pip install xgboost
pip install pickle-mixin
```

### Download the model file and follow the JupyterNotebook
You can simply download the model file in the `Model` and follow the JupyterNotebook in the `Example` folder to run the models for your predictions. 
