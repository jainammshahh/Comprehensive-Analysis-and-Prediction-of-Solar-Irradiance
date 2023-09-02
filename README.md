# Project Overview 

Solar Radiation is the predominant source of energy on earth and plays a vital role in the process of environmental cycles taking place on earth including hydrological cycles, vegetation photosynthesis and climate change. Precise analysis and accurate prediction of solar radiation is very important in conserving energy and preventing climate change all over the planet. Prediction also helps to ameliorate organization and coordination of solar systems and further helps in diminishing electricity bills and prove to be economically efficient for households. In this project, statistical methods and machine learning techniques have been employed to predict solar irradiance. The methods include building prediction model with random forest regressor and applying cross-validation which prove to be effective in providing accurate prediction whereas rest of the methods fail due to inability of scaling big data and defining long-term dependency. Results indicate that meteorological factors like temperature, time of day and year were important for predictive analytics. The dataset used in this project includes information from HI-SEAS habitat from Hawaii and multiple sources which tracked the formation of solar irradiance. Extreme surface temperature and the extend of solar radiation shows importance of solar irradiance in different places through trend analysis. How much energy is stored in solar panels and the amount of solar energy is required for daily consumption level for mission in HI-SEAS and the factors affecting it have been tracked. Final insights of this project indicate that cross-validation method and Random Forest Regressor performed better than the rest of the methods to predict solar irradiance.

# Data Preparation & Integration

Gathering Data is the initial and most crucial step to provide comprehensive understanding of a concept. For predicting solar irradiance in this project, multiple datasets are combined from meteorological data available from HI-SEAS program from NASA through period of four months (September - December 2016) over two missions. The project’s aim is to help crew monitor energy levels coming from photovoltaic systems and different parameters affecting it.

**Data Overview & Preprocessing**

The following organization has been followed for data preprocessing on HI-SEAS Hawaii data.

**Data preprocessing path**  

<img width="468" alt="image" src="https://github.com/jainammshahh/Comprehensive-Analysis-and-Prediction-of-Solar-Irradiance/assets/114266749/3190372d-ddd1-4ced-989f-153dbcb6a05e">


**Data Source -** https://2017.spaceappschallenge.org/challenges/earth-and-us/you-are-my-sunshine/details

The following parameters are included in each dataset and based on that the datasets are merged.

1.	Row number (1-n) for sorting
2.	UNIX time_t date (secoonds) for sorting
3.	Date in yyyy-mm-dd format
4.	Local time in 24-hour format
5.	Numeric data
6.	Text Data

Numeric data and Text data are unique based on parameters as mentioned below. The merged data frame includes following columns and have been sorted based on UNIXTIME column available in each dataset:

1.	UNIXTime – in seconds
2.	Date – in yyyy-mm-dd format
3.	Time – in 24-hour format
4.	Radiation – in watts per meter2
5.	Temperature – in degrees fahrenheit
6.	Pressure – in Hg (mercury)
7.	Humidity - percent
8.	WindDirection (Degrees) – in degrees
9.	Speed – in miles per hour
10.	TimeSunRise - Hawaii Time
11.	TimeSunSet - Hawaii Time

**Dataset Overview**
<img width="468" alt="image" src="https://github.com/jainammshahh/Comprehensive-Analysis-and-Prediction-of-Solar-Irradiance/assets/114266749/0cbfe3d2-467e-4a3d-812e-8f3a981fdc99">


Originally “Time” column was available in reverse order. It has been modified and correctly arranged in the data frame by resetting by sorting.

**Dataset Info**
<img width="283" alt="image" src="https://github.com/jainammshahh/Comprehensive-Analysis-and-Prediction-of-Solar-Irradiance/assets/114266749/72699027-cfdf-4a9d-9914-65f478f5a1f9">


**Dataset Statistics**

<img width="412" alt="image" src="https://github.com/jainammshahh/Comprehensive-Analysis-and-Prediction-of-Solar-Irradiance/assets/114266749/10abe8e8-1f8a-4555-95e4-0b858fde9ed0">

# Inplementation Appraoch

**Step 1: Data Gathering**

-   Gathered multiple datasets related to solar irradiance from the HI-SEAS program by NASA, spanning four months (September - December 2016) across two missions.

**Step 2: Data Preprocessing**

-   Combined and organized the datasets.
-   Cleaned and preprocessed the data.
-   Transformed date and time variables into a trackable format.
-   Added new parameters for analysis, modeling, and visualization.

**Step 3: Feature Engineering**

-   Used datetime functions and libraries to correlate data with Hawaii time zone.
-   Created new columns for various time-related features like Month of the Year, Day of the Year, etc.
-   Calculated Day Length.

**Step 4: Feature Visualization**

-   Visualized data parameters using bar plots, focusing on hourly and monthly means.
-   Gained insights such as the strong correlation between temperature and solar irradiance.

**Step 5: Correlation Analysis**

-   Utilized Pearson Correlation Heatmap to understand relationships between variables.
-   Observed that temperature had a stronger correlation with solar irradiance compared to other factors.

**Step 6: Model Creation**

<img width="395" alt="image" src="https://github.com/jainammshahh/Comprehensive-Analysis-and-Prediction-of-Solar-Irradiance/assets/114266749/0988185c-e49e-4339-847f-1f85eeaf799a">

-   Split the dataset into independent and dependent variables, where solar irradiance is the dependent variable.
-   Employed decision tree-based regression algorithms, specifically Random Forest Regressor, for model creation.
-   Performed backward elimination to remove less important parameters.
-   Achieved an r2 score of approximately 0.93 with key features: Temperature, Time of Day, and Day of the Year.

**Step 7: Cross-Validation**

-   Conducted cross-validation with 10 folds to assess the model's performance.
-   Verified that the model was not overfit.

**Step 8: Predictive Modeling**

-   Applied the trained model to predict solar irradiance on a test dataset.
-   Obtained variance, r2, and mean squared error as metrics to assess accuracy.

**Step 9: Analytical Results**

-   Summarized key findings from feature visualization, correlation analysis, and model creation.
-   Highlighted the importance of temperature, time of day, and day of the year in predicting solar irradiance.

This step-by-step implementation provides an overview of the project's process from data gathering to obtaining analytical results for predicting solar irradiance.


