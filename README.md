# project_m3

## Name
"Diamond price estimator"


## Status
Alpha version


## One-liner
This project uses machine learning techniques in order to determine the prices of diamonds based on its given characteristics.


## Technology stack
Python, sklearn, Pandas, lightgbm.


## Configuration
The project requires Python 3.x and several libraries, which can be installed using the requirements.txt file included in the repository.


## Usage
There are two main notebooks used in this project, the "009_classify" is used to calculate the price variations of the color, cut and clarity features, generating and scaling a labeling table that is used in the train and test dataframes. In the second notebook "009_proj_m3", is where the data is processed. We have the a couple of functions to scale the data in general and to bin the carat values and then the process go like this:
- The train and the test tables are merged to be scaled together.
- After the scaling we drop the test data.
- The already scaled labels for cut, color and clarity are included in the dataframe and the original cut, color and clarity columns are dropped.
- We also drop unwanted columns like, x, y, z and city.
- We use the lightgbm model and train it using the final result of the dataset.
- We load the test dataframe and apply the same process described above to it.
- We predict the diamond prices in the test dataframe.
- We save the prediction.

The Folder structure is as follows:


```
Folder structure
├── .git
├── data
│ └──predictions
│ └──scales
├── notebooks
│ └── other
│ └── 009_classify.ipynb
│ └── 009_proj_m3.ipynb
├── .gitignore
└──README.md
```


## ToDo
Implement new tests in order to improve the model.


## Contact info
If you have any questions or feedback, please contact me at magnofz@gmail.com.