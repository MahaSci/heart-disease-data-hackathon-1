#  ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Heart Disease Data Analytics Project 🫀



**Cardiovascular diseases remain the leading cause of death worldwide each year.**

> According to the World Heart Federation, **"an estimated 80% of cardiovascular diseases... are preventable."** 

This highlights the critical need for preventative strategies in reducing the number of global deaths. In order to address this issue, we must first examine the prevalent risk factors associated with heart disease.

## Project Goal
This goal of this project is to analyse health data to understand the relationship and trends of various risk factors such as _diabetes_, _cholesterol_ and _BMI_ in relation to heart disease. 

## Dataset Content

The dataset consists of 21 columns.
| **Attributes**            |     **Attributes**        |     **Attributes**        |
|---------------------------|---------------------------|---------------------------|
| **Age**                       | **Diabetes** (Yes/No)                  | **Sleep Hours** (Hours)              |
| **Gender** (Male, Female, Other)                   | **BMI** (kg/m^2)                       | **Sugar Consumption** (Low, Medium, High)         |
| **Blood Pressure** (mmHg)            | **High Blood Pressure** (Yes/No)       | **Triglyceride Level** (mg/dL)        |
| **Cholesterol Level** (mg/dL)       | **Low HDL Cholesterol** (Yes/No)       | **Fasting Blood Sugar** (mg/dL)       |
| **Exercise Habits** (Low, Medium, High)          | **High LDL Cholesterol** (Yes/No)      | **CRP Level** (mg/L)                 |
| **Smoking** (Yes/No)                  | **Alcohol Consumption** (Low, Medium, high)       | **Homocysteine Level** (µmol/L)        |
| **Family Heart Disease** (Yes/No)      | **Stress Level** (Low, Medium, High)              | **Heart Disease Status** (Yes/No)      |

<br>

> BMI: Body Mass Index
  
> HDL Cholesterol: A "good" cholesterol that removes "bad" cholesterol from your blood

> LDL Cholesterol: "Bad" cholesterol that increases risk of heart disease

> Triglycerides: Type of fat in blood that increases risk of heart disease

> CRP Level: Protein in the blood that indicates inflammation that can contribute to heart disease



## Business Requirements
### Objectives
#### Primary Goal
This goal of this project is to analyse health data to understand the relationship and trends of various risk factors such as _diabetes_, _cholesterol_ and _stress_ in relation to heart disease. 
#### Intended Outcomes
The intended outcome of this project is for healthcare providers to have a set of actionable insights, regarding risk factors for cardiovascular diseases, that they can then utilise to inform prevention strategies and programmes for patients.

### Target Audience
The target audience of this project includes:
* Medical professionals
* Government healthcare departments
* Patients

### Questions
* Which risk factor is most strongly associated with heart disease?
* What demographic groups are most at risk? (Age, BMI)


## Hypotheses and how to validate?
### Hypothesis 1: Individuals with diabetes are more likely to develop heart disease
#### Visualisation
A donut chart was used to visualise distribution of individuals with or without diabetes who have heart disease. Since there are only 2 categories, a donut chart will show whether there is a noticeable difference between the 2 groups.



### Hypothesis 2: Higher cholesterol levels have a positive correlation with heart disease diagnosis
#### Visualisation
A violin plot was used to show the distribution of the continuous type cholesterol level in individuals with and without heart disease.



### Hypothesis 3: Smokers are more likely to develop heart disease compared to non-smokers
#### Visualisation

A donut chart was used to visualise distribution of individuals smokers or non-smokers who have heart disease. Since there are only 2 categories, a donut chart will show whether there is a noticeable difference between the 2 groups.


### Hypothesis 4: Individuals with a family history of heart disease are more likely to develop heart disease themselves
#### Visualisation

A donut chart was used to visualise distribution of individuals with or without a family history of heart disease who have heart disease. Since there are only 2 categories, a donut chart will show whether there is a noticeable difference between the 2 groups.


### Hypothesis 5: Individuals with a higher BMI are more likely to develop heart disease
#### Visualisation
Hex bin visual was used to visualise the density of individuals with a higher BMI and positive diagnosis for heart disease.

## Project Plan
* Outline the high-level steps taken for the analysis.
- Phase 1: Data Collection and ETL
    Extraction:
        Data sourced from Kaggle and saved as a csv
    Transformation:
        Rows with missing and duplicate data was removed
    Feature Engineering:
        Categorical value of heart disease status was mapped into a numerical value/
    Load:
        Data was then loaded into a truncated csv file.

- Phase 2: Exploratory Analysis
    Summary statistics were calculated
    Distribution of the data was assessed using visualisation
    Outliers were identified using visualisation

- Phase 3: Visualisation
    Histograms, Box plots, violin plots, correlation heatmaps.
    Aim: understand distribution of the data, show the spread of the data and identify if there were any relationships between risk factors of heart disease.

## Analysis techniques used
* Statistical Testing
* Multivariable visualisations

How did you use generative AI tools to help with ideation, design thinking and code optimisation?
* ChatGPT was used to find the best visualisation types based on the type of data i.e categorical, numerical. I also used ChatGPT to help me debug during section 2.3.

## Ethical considerations
* All data was anonymised with identifying information removed and index numbers to identify each row.

## Development Roadmap
### What challenges did you face, and what strategies were used to overcome these challenges?
#### 1. Iteration error with plotting
In [section 1.2.4 Identifying outlier values] I struggled with attempting to iterate through the list of columns and plot on multiple axes.

<img src="BoxPlotError.png" alt="boxploterror" width="500"/>

    * I got around this by simply plotting each box plot seperately. 

#### 2. Sample error
In [section 1.2.4 Identifying outlier values] during the count plot analysis for outliers, it was made apparent that 100% of the data selected had 'No' for heart disease diagnosis 

<img src="CountPlotSampleError.png" alt="countplotsampleerror" width="400"/>

     * Therefore, I resampled the data using a random state argument to ensure a more representative sample was analysed.

#### 3. Mapping Error
In [section 2.3] during the mapping process I made the error of not stripping white space from my heart disease status column which lead the mapping to fill the dataframe with NaN values. After searching through documentation I used the str.strip() function to do so and successfully map numeric values to my categorical ones


## What new skills or tools do you plan to learn next based on your project experience? 
In my next project I would love to learn more statistical tests that can help me to assess the validity of my findings with numerical measures.


## Main Data Analysis Libraries
* Pandas: data manipulation and analysis
* Numpy: numerical operations
* Seaborn: data visualisations
* matplotlib : static visualisations
* plotly: for interactive visualisations
* Scipy: for statistical tests (chi-squared)

## Credits 

Chi Squared Statistical Test Method: https://campus.datacamp.com/courses/analyzing-survey-data-in-python/statistical-modeling?ex=8


Pandas Documentation: https://pandas.pydata.org/docs/reference/api/pandas.Series.str.strip.html


## Acknowledgements 
* I would like to express my gratitude to my facilitator, Vasi Pavaloi, for his valuable feedback and support throughout this project.