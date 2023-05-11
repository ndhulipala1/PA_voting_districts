# Pennsylvania Voting District Analysis

This codebase is where analysis was done to compare the output of the [BDistricting algorithm](https://bdistricting.com/about.html), a political redistricting algorithm, and the 2020 Congressional Districts of Pennsylvania (PA). This analysis was performed for our paper, "Algorithms for Political Redistricting and Assessing Fairness," a final project for the course CS331 Advanced Algorithms at Wellesley College. This README will explain what the various aspects of the repository are, what they do, and how to operate them.

## About This Repository

The repository consists of a `data` directory, which contains all the data necessary for the analysis, and three Jupyter notebooks: `BDistricting_Output_EG_Analysis.ipynb`, `BDistricting_Output_Racial_Analysis.ipynb`, and `PA_Current_Districts.ipynb`. 

The `data` directory contains all the data necessary for the analysis in the three notebooks. Within that directory, there are three subdirectories:
- `PA_pop`: this directory contains the shapefile consisting of Pennsylvania's voting districts. These were sourced from the [MGGG Redistricting Lab's official Github repository for Pennsylvania's shapefile](https://github.com/mggg-states/PA-shapefiles/).
- `US_con_dists`: this directory contains the shapefile for all US Congressional Districts. Of this shapefile, we only use the Congressional Districts in Pennsylvania (state 42) for analysis.
- `PA_Congress.csv`: this file contains the output of the BDistricting algorithm for Pennsylvania, containing the data for 17 Congressional Districts the algorithm produced. This is sourced from the [BDistricting website](https://bdistricting.com/2020/PA_Congress/).

The BDistricting Analysis notebooks, namely `BDistricting_Output_EG_Analysis.ipynb` and `BDistricting_Output_Racial_Analysis.ipynb`, conduct analysis on the BDistricting output. Each notebook merges the geospatial data of Pennsylvania's voting districts and the BDistricting output. The first notebook calculates the Efficiency Gap (EG) of all districts, and the second notebook conducts analysis to compute the number of Minority Opportunity Districts (MODs).

Finally, the `PA_Current_Districts.ipynb` notebook merges the voting district data with the current Congressional District geospatial data and conducts both EG and racial analysis on all the current PA Congressional Districts.

## Usage

To use this paper, you will need a current version of Python (version 3.8 or later) and you will need to either install the following libraries or use a virtual environment containing the following libraries (in parentheses, I included the current version of the library on my machine):
- NumPy (1.20.2)
- Pandas (1.2.4)
- GeoPandas (0.12.2)

To reproduce the analysis from our paper, you may run each of the notebooks after those libraries are installed. Make sure you run the notebooks on a Jupyter notebook pointing either to your Python version or your virtual environment (whichever module contains the libraries you installed). Alternatively, you may also upload these Jupyter notebooks onto Google Colab and upload the files in the data directory to the file management system so that Colab can access this data.