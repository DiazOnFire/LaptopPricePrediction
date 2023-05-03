**How to run this notebook on your system?**

You can download the notebook along with the dataset directly from the repo itself and run it on your system.

***OR***

1. Open Google Collab or Kaggle or any other cloud based notebook.

2. Download the dataset from repository itself.

3. Create a new notebook and go to **File->Upload Notebook->GitHub and paste this [link](https://github.com/DiazOnFire/LaptopPricePrediction/blob/main/LaptopPricePrediction/LaptopPricePredictorUsing_LocallyWeightedLR.ipynb) 

4. Run the code and in the first cellbox itself,a prompt to upload file shows up, Upload the dataset you downloaded there and the notebook now can run on your system.












# LaptopPricePrediction
Exploratory Data Analysis, extensive data preprocessing and prediction of Laptop Price based on various components using RandomForestRegressor, Locally Weighted Linear Regression and also using Artificial Neural Network implemented via PyTorch.


The dataset I worked on is LaptopData.csv which has the following columns.I have uploaded the dataset along with the jupyter notebook.

#Columns of the dataset
1. Company
2. TypeName
3. Inches
4. ScreenResolution
5. Cpu
6. Ram
7. Memory
8. Gpu
9. OpSys
10. Weight
11. Price

**The dependant variable is Price column, we attempt to predict Price column using the other columns/variables.**

- I started off with Exploratory Data Analysis and started comparing each independent variable with *Price*. With the help of ***corr()*** function, Seaborn, Matplotlib, Numpy and Pandas, I figured out relations between **Price** and other variables.

- After doing decent amount of EDA, I started off with Data Preprocessing. I have explained reasons and methods to make the data ready for a ML model. At some places, I made my own functions as well to feature extract and engineer.

- Using ***train_test_split*** function which is imported from sklearn.preprocessing, I split the data into *Training* and *Testing* data. Using OneHotEncoder and Pipeline, the RandomForestRegressor was fit onto the ready data. Using performance metrics like mse and r2_score, I evaluated the efficiency of the model.

- Similarly, I used ***get_dummies()*** to convert categorical data. After making functions for Locally Weighted LR, it was fit onto the data. Using plots, it's metrics was represented. Right after this, using PyTorch, an Artificial Neural Network was implemented with 1 input, 1 hidden and 1 output layer. It's accuracy has been measured using Root Mean Square Error. Even though it is quite high as the layers and various parameters involved in creating the neural network have not been properly configured, the plot shows decent results.


