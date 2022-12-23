# 202212-32-Food-Recalls
## Visualization and Analysis of Food Recalls
### EECS E6893: Big Data Analytics Fall 2022
Group 32\
Nathan Ma

## Project Introduction
This project aims to extract meaningful text features from food recall report webpages listed by the US FDA and FSIS, to augment existing tabular data. This data can be used to identify trends in food recalls, allowing users to textually query then visualize distributions or patterns in recalls. This ultimately allows users to make more informed decisions about the food they purchase, which can prevent some of the millions of cases of people getting sick or dying from foodborne illnesses each year.

Available to the user is an interactive tool in `Analysis_Visualization.ipynb` to query recalls and see the results visualized.

[Data Collected and Used (Requires LionMail)](https://drive.google.com/drive/folders/1Oc26bdlAPJln8gnjE_aZNBsIk-ORqANk?usp=sharing)

![State Recalls](overall_state_choropleth.jpeg)

## To Run Code
### Dependencies
The following packages need to be installed to run the code. They can be installed with `pip install`. Some may already be installed (especially if using Google Colab environment)
* numpy
* matplotlib
* pandas
* google-colab
* reqeusts
* bs4
* plotly
* kaleido

### Notebooks
The data preparation and gathering is done in `Data_Preparation.ipynb`. This process can be recreated in the notebook. By executing the cells to make all the http requests, the user can reproduce the gathering of all the raw html data (not recommended due to long runtime). The cells to process the html data into extracted text data features can also be used to reproduce this process of formatting then parsing the text data (also not recommended due to long runtime). These cells are commented as only to be run once. Alternatively, the user can simply use the pre-saved data files to view the html and text data already processed.

### Visualizations
The analysis and visualization done in `Analysis_Visualization.ipynb` can be reproduced by running the notebook cells (preferable in Google Colab environment). The functions to create visualizations are available for individual use, or the user can jump to the bottom and use the interactive tool. This interactive tool allows the user to query recalls and have the results visualized. Users can specify analysis/visualization type, year of recalls, impacted states (50 US states + DC), recalled product, and recall reason. The visualization is displayed.
