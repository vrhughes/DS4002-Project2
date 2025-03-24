# DS4002-Project2
DS 4002 Project 2 for Vivienne Hughes (leader), Avery Donmoyer and Dana Pham.

## Goal
We will employ a regression model to correlate five specific social and economic variables (GDP per capita, women’s education attainment in years, life expectancy in year, child/infant mortality rate per 100 live births, and homicide rate per 100,000 people) with fertility rates. Our goal is to answer the question: Which social factor has the most predictive power on a country’s population? We plan to predict future fertility rates with our data and compare our predictions to the UN's predictions to see how well our model(s) work. Lastly, we will calculate the error between our model and the UN predictions with RMSE and MAE.

## Software/Platform
We are using Jupter Notebooks for this program that run on Python 3 (prefferably 3.10+). Our code can be run on Google Colab by importing our notebooks. All files will need a Python environment with some or all of the following packages: Pandas, Numpy, Matplotlib, Seaborn, re, statsmodels, and linearmodels. All files will need support for Jupyter Notebooks and can be run on Windows, Linux, or Mac.

## Documentation
The files and folders are broken down into this structure

```
- root
  -- DATA
    -- GDP-Per-Capita-Current-USD.csv
    -- Homicides-Per-100000.csv
    -- attainment_and_fertility.csv
    -- children-born-per-woman.csv
    -- fertility-rate-with-projections.csv
    -- infant_mortality.csv
    -- life-expectancy.csv
  -- SCRIPTS
    -- script files for data analysis
  -- OUTPUT
    -- generated data files
    -- charts and tables (png files)
  -- README.md
  -- License.md
```

The DATA folder contains the datasets which we used in our project (references below coordinate to where each is from). The SCRIPTS folder contains multiple Jupyter Notebooks that have been used to clean and analyse the data, run ARIMAX and TWFE, create graphs, and do error analysis. The OUTPUT folder contains generated datasets from SCRIPTS as well as important outputed graphs and tables in png files. 

## Steps to Reproduce
To reproduce the results of the project first yo umust close the repository with the following command: ``` git clone https://github.com/vrhughes/DS4002-Project2 ```
Then, you can take the gdp data and run the GDP_csv_organizing script which will give you your first cleaned output of the gdp file (also available in the OUTPUTS folder if you want to skip the first script). Then, using the cleaned gdp file and the other 5 data sets (not including the projections by the UN) run the Data_Consolidation to get the complete dataset. Next, run the third script which verifies that the educational attainment data can be linearly interpolating. Now, run the ARIMA_data_cleaning file which fixes the missing values created in the combined data set due due to the fact that the educational attainment information was only collected every five years. From there you can run either TWFE or full_ARIMA, the order does not matter.

1. GDP_csv_organizing.ipynb
2. Data_Consolidation.ipynb
3. edu_attainment_linear_reg_analysis.ipynb
4. ARIMA_data_cleaning.ipynb
5. TWFE.ipynb
6. full_ARIMAX.jpynb

## References
1. Data compiled from multiple sources by World Bank (2025) – with minor processing by Our World in Data. “GDP per capita – World Bank – In constant international-$” [dataset]. Data compiled from multiple sources by World Bank, “World Development Indicators” [original data]. Retrieved March 5, 2025 from https://ourworldindata.org/grapher/gdp-per-capita-worldbank 
2. IHME, Global Burden of Disease (2024) – with minor processing by Our World in Data. “Homicide rate” [dataset]. IHME, Global Burden of Disease, “Global Burden of Disease - Deaths and DALYs” [original data]. Retrieved March 5, 2025 from https://ourworldindata.org/grapher/homicide-rate 
3. Barro and Lee (2015); Lee and Lee (2016) – with major processing by Our World in Data. “Average years of schooling (women aged 15–64)” [dataset]. Barro and Lee, “Projections of Educational Attainment”; Lee and Lee, “Human Capital in the Long Run” [original data].
4. UN, World Population Prospects (2024) – processed by Our World in Data. “Fertility rate, total – UN WPP” [dataset]. United Nations, “World Population Prospects” [original data].
5. UN, World Population Prospects (2024) – processed by Our World in Data. “Fertility rate, medium projection – UN WPP” [dataset]. United Nations, “World Population Prospects” [original data]. 
6. United Nations Inter-agency Group for Child Mortality Estimation (2024) – with major processing by Our World in Data. “Infant mortality rate” [dataset]. United Nations Inter-agency Group for Child Mortality Estimation, “United Nations Inter-agency Group for Child Mortality Estimation”; Various sources, “Population” [original data]. Retrieved March 5, 2025 from https://ourworldindata.org/grapher/infant-mortality
7. UN WPP (2024); HMD (2024); Zijdeman et al. (2015); Riley (2005) – with minor processing by Our World in Data. “Life expectancy at birth – Various sources – period tables” [dataset]. Human Mortality Database, “Human Mortality Database”; United Nations, “World Population Prospects”; Zijdeman et al., “Life Expectancy at birth 2”; James C. Riley, “Estimates of Regional and Global Life Expectancy, 1800-2001” [original data]. Retrieved March 5, 2025 from https://ourworldindata.org/grapher/life-expectancy  
