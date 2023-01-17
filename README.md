Medical Cost Multivariate Linear Regression
-----------------------

Linear Regression and Polynomial models to predict the medical insurance cost of customers from a customer dataset. The dataset contains customer information and region, along with their medical cost. Dataset is [here](https://www.kaggle.com/datasets/mirichoi0218/insurance?datasetId=13720&sortBy=voteCount&utm=). You can see the data processing, model, code, and full explanations in the MedicalCostRegression.ipynb notebook above.

Quick Overview
----------------------

The data is of 13k customers with their features and charge. The BMI feature stands for body mass index, a value derived from the mass and height of a person.

<p align="center">
<br />
Data
<br />
<br />
<img src="https://github.com/ET-777/Medical-Cost-Regression/blob/master/images/data.jpg"/>
<br />
<br />
<br />
</p>

<p align="center">
<br />
Graphs
<br />
<br />
<img src="https://github.com/ET-777/Medical-Cost-Regression/blob/master/images/graphs.jpg"/>
<br />
<br />
<br />
</p>

Plotting the data, we find:

- From the first two graphs plotting age and BMI, we can see there is a clear distinction between smokers and non smokers. The smoking group clearly has higher charges for their medical bill, further confirmed by the smoker graph.

- Age also seems to increase chargres, but for BMI, charge only increases along if the customer is a smoker.

- The region of the customer does not seem to have an effect on charges.

- The more children a customer has, charges seem to decrease. Customers with 3 children still reached high charges, however this could be outlier cases.

- As with region, sex does not seem to have an impact on charges.

Smoking has the highest correlation with charges, unsurprsingly. Sex and region the least, so these last two are dropped.

Results
----------------------

Using Linear regresion, the model is fitted and trained, getting the following results.

Model score: 0.7300423756673933
Model test score: 0.7894429387120754
Model mean squared error: 33577421.938634135

<p align="center">
<br />
Graphs
<br />
<br />
<img src="https://github.com/ET-777/Medical-Cost-Regression/blob/master/images/linear_graph.jpg"/>
<br />
<br />
<br />
</p>

Using polynomial regreesion, 6 models with different degreees. The model with 2 degrees proved best out of all the model and best at generalizing with the following results.

Degree: 2
Model score: 0.8266610379551892
Model test score: 0.8750334947519957
Model mean squared error: 19928341.748514995

<p align="center">
<br />
Graphs
<br />
<br />
<img src="https://github.com/ET-777/Medical-Cost-Regression/blob/master/images/pol_graph.jpg"/>
<br />
<br />
<br />
</p>

Installation
----------------------

### Download the data

* Clone this repo to your computer.
* Create a `Data` folder in the project directory
* Download the data files from Kaggle into the `Data` folder.  
    * You can find the data [here](https://www.kaggle.com/datasets/mirichoi0218/insurance?datasetId=13720&sortBy=voteCount&utm=).
    * You'll need to register with Kaggle to download the data.
* Extract the `.zip` file.

### Install the requirements
 
* Install the requirements with `anaconda` or with pip using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

Usage
-----------------------

* Open `MedicalCostRegression.ipynb` with `Jupyter Notebook`.
* Run the notebook
