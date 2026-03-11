# Airport Delay Prediction with Weather Integration

## Project Overview
[cite_start]This project aims to predict flight delays (defined as a delay of more than 15 minutes) using a combination of flight schedule data and local weather information[cite: 3]. [cite_start]It was developed as part of a machine learning study to understand how environmental factors, specifically precipitation, impact aviation logistics[cite: 1, 3, 5].

## Dataset Description
The project utilizes several datasets to build the predictive model:
* [cite_start]**flights.csv**: Contains historical flight records including airline, origin, and destination information[cite: 5].
* [cite_start]**rain.csv**: Contains daily precipitation data matched by date to the flight records[cite: 1].
* [cite_start]**airports.csv & airlines.csv**: Supplementary metadata for mapping airport codes and airline names[cite: 2, 4].

## Methodology
[cite_start]The core of the project is implemented in `Airport_delay_withrain.ipynb`[cite: 3]:
1. [cite_start]**Data Integration**: Merging flight schedules with weather data based on temporal features (Year, Month, Day)[cite: 3].
2. [cite_start]**Preprocessing**: Handling missing values (e.g., imputing missing rain data as 0) and feature encoding for categorical variables[cite: 3].
3. [cite_start]**Class Imbalance Handling**: Since delayed flights are minority events, **SMOTE** (Synthetic Minority Over-sampling Technique) was implemented to balance the training set[cite: 3].
4. [cite_start]**Modeling**: A **Random Forest Classifier** was trained to capture the non-linear interactions between scheduling and weather conditions[cite: 3].

## Requirements
To run this project, you need the following Python libraries:
* pandas
* scikit-learn
* imbalanced-learn
* matplotlib
* seaborn

## How to Run
1. [cite_start]Ensure all CSV files (`flights.csv`, `rain.csv`, etc.) are in the same directory as the notebook[cite: 1, 2, 3, 4, 5].
2. Open `Airport_delay_withrain.ipynb` in a Jupyter environment.
3. Run the cells sequentially to perform data cleaning, training, and evaluation.

## Results
[cite_start]The model achieves a balanced performance across both on-time and delayed flights, with a focus on optimizing the F1-score to handle the inherent class imbalance in aviation data[cite: 3].
