\# Kenya Maize Production \& Climate Data Analysis



\## Project Overview



This project analyzes maize production trends in Kenya from \*\*2000 to 2024\*\* and examines how climate variables may be associated with maize yield and production.



The analysis combines maize production data with climate data to identify historical trends, relationships, variations, and patterns that can support data-driven agricultural decision-making.



This is a \*\*data analytics project\*\* focused on descriptive analysis, trend analysis, correlation analysis, outlier assessment, production decomposition, and interactive visualization. It does not use predictive machine learning models.



\---



\## Objectives



The project aims to:



1\. Analyze trends in maize production, yield, and harvested area from 2000 to 2024.

2\. Examine historical variation in temperature and precipitation.

3\. Quantify linear relationships between climate variables and maize yield.

4\. Examine relationships between climate variables and maize production.

5\. Identify years with exceptionally high or low maize production and yield.

6\. Decompose maize production growth into area expansion, yield improvement, and their interaction.

7\. Present the findings through an interactive Power BI dashboard.



\---



\## Data Sources



The analysis uses data from:



\* \*\*FAOSTAT\*\* — maize production, yield, and harvested area.

\* \*\*World Bank Climate Change Knowledge Portal (CCKP)\*\* — climate variables including temperature and precipitation.



\### Analysis Period



\*\*2000–2024\*\*



\### Dataset



The final integrated dataset contains:



\* Year

\* Maize Production (tonnes)

\* Maize Yield (kg/ha)

\* Harvested Area (ha)

\* Temperature (°C)

\* Precipitation (mm)

\* Additional climate/seasonal variables used during the analysis



The final dataset contains \*\*25 annual observations\*\* with no missing values or duplicate rows.



\---



\## Tools Used



\* \*\*Python\*\*

\* \*\*Jupyter Notebook\*\*

\* \*\*Pandas\*\*

\* \*\*NumPy\*\*

\* \*\*Matplotlib\*\*

\* \*\*Power BI\*\*

\* \*\*Git\*\*

\* \*\*GitHub\*\*



\---



\## Project Structure



```text

Kenya\\\_Maize\\\_Climate\\\_Analysis/

│

├── data/

│   ├── raw/

│   │   ├── Crop production, yield, harvested area (Global, National - Annual) - FAOSTAT(1).csv

│   │   └── era5-x0.25\\\_timeseries\\\_tas,pr,gslstart\\\_timeseries\\\_annual\\\_1950-2025\\\_mean\\\_historical\\\_era5\\\_x0.25\\\_mean.xlsx

│   │

│   └── processed/

│       ├── kenya\\\_maize\\\_2000\\\_2024\\\_clean.csv

│       └── kenya\\\_maize\\\_climate\\\_2000\\\_2024.csv

│

├── notebooks/

│   └── 01\\\_data\\\_collection\\\_and\\\_exploration.ipynb

│

├── reports/

│   └── Kenya\\\_Maize\\\_Production\\\_Analysis\\\_Report\\\_v3.pdf

│

├── Kenya\\\_Maize\\\_Production\\\_Climate\\\_Analysis\\\_2000\\\_2004.pbix

│

└── .gitignore

```



\---



\## Methodology



The analysis followed these main stages:



\### 1. Data Collection



Maize production data was obtained from FAOSTAT, while climate data was obtained from the World Bank Climate Change Knowledge Portal.



\### 2. Data Cleaning



The datasets were inspected and prepared for analysis by:



\* Checking column names and data types

\* Selecting relevant variables

\* Aligning the datasets by year

\* Checking for missing values

\* Checking for duplicate records

\* Creating processed datasets for analysis and visualization



\### 3. Exploratory Data Analysis



Descriptive statistics were calculated for maize production, yield, harvested area, temperature, and precipitation.



Time-series visualizations were also created to identify historical trends and fluctuations.



\### 4. Correlation Analysis



Pearson correlation coefficients were calculated to measure linear associations between:



\* Climate variables and maize yield

\* Climate variables and maize production

\* Harvested area and maize production



Correlation values were interpreted as associations rather than evidence of causation.



\### 5. Outlier Analysis



The Interquartile Range (IQR) method was used to assess whether the major variables contained statistical outliers.



The analysis identified \*\*no statistical outliers\*\* under the applied IQR criterion.



\### 6. Production Decomposition



Maize production was analyzed using:



\*\*Production = Harvested Area × Yield\*\*



The change between 2000 and 2024 was decomposed into:



\* Area expansion effect

\* Yield improvement effect

\* Area × yield interaction effect



\---



\## Key Findings



\### Overall Production Growth



Maize production increased from approximately \*\*2.16 million tonnes in 2000\*\* to approximately \*\*4.023 million tonnes in 2024\*\*.



This represents an overall increase of approximately \*\*86.25%\*\*.



\### Harvested Area



Harvested area increased from approximately \*\*1.50 million hectares\*\* in 2000 to approximately \*\*2.41 million hectares\*\* in 2024.



This represents an increase of approximately \*\*60.97%\*\*.



\### Yield



Average maize yield increased from \*\*1,440.0 kg/ha\*\* in 2000 to \*\*1,666.2 kg/ha\*\* in 2024.



This represents an increase of approximately \*\*15.71%\*\*.



\### Production Decomposition



The increase in maize production between 2000 and 2024 was decomposed as follows:



| Component                | Contribution |

| ------------------------ | -----------: |

| Area expansion           |       70.68% |

| Yield improvement        |       18.21% |

| Area × Yield interaction |       11.10% |

| \*\*Total\*\*                |  \*\*100.00%\*\* |



The results indicate that \*\*expansion of harvested area was the largest contributor to the increase in national maize production\*\* during the period.



\---



\## Climate and Yield Relationships



The Pearson correlation analysis produced the following key relationships:



| Variables                   | Pearson Correlation |

| --------------------------- | ------------------: |

| Yield – Precipitation       |            \*\*0.61\*\* |

| Yield – Temperature         |           \*\*-0.22\*\* |

| Production – Precipitation  |            \*\*0.58\*\* |

| Production – Temperature    |            \*\*0.41\*\* |

| Production – Harvested Area |            \*\*0.86\*\* |

| Yield – Production          |            \*\*0.49\*\* |

| Yield – Harvested Area      |           \*\*-0.01\*\* |

| Temperature – Precipitation |           \*\*-0.15\*\* |



\### Interpretation



\* \*\*Precipitation and yield (r = 0.61):\*\* A moderate positive linear association was observed. Years with higher annual precipitation tended to be associated with higher maize yields.

\* \*\*Temperature and yield (r = -0.22):\*\* A weak negative association was observed.

\* \*\*Harvested area and production (r = 0.86):\*\* A strong positive relationship was observed, supporting the finding that area expansion played a major role in production growth.

\* \*\*Precipitation and production (r = 0.58):\*\* A moderate positive association was observed.



These relationships should be interpreted as \*\*statistical associations, not proof that one variable directly caused changes in another\*\*.



\---



\## Notable Years



\### Highest Production



The highest recorded production in the analyzed dataset occurred in \*\*2023\*\*, at approximately:



\* Production: \*\*4,285,206 tonnes\*\*

\* Yield: approximately \*\*1,763.4 kg/ha\*\*

\* Temperature: approximately \*\*25.66°C\*\*

\* Precipitation: approximately \*\*707.85 mm\*\*



\### Lowest Production



The lowest recorded production occurred in \*\*2000\*\*:



\* Production: \*\*2,160,000 tonnes\*\*

\* Yield: \*\*1,440.0 kg/ha\*\*

\* Temperature: \*\*25.16°C\*\*

\* Precipitation: \*\*477.52 mm\*\*



\---



\## Power BI Dashboard



An interactive Power BI dashboard was developed to communicate the major findings of the analysis.



The dashboard provides visual analysis of:



\* Maize production trends

\* Yield trends

\* Harvested area trends

\* Temperature trends

\* Precipitation trends

\* Climate-production relationships

\* Key performance indicators

\* Historical variations and notable years



The dashboard complements the Python exploratory analysis by providing an interactive interface for exploring the results.



\---



\## Data Quality



The final integrated dataset contains:



\* \*\*25 annual observations\*\*

\* \*\*2000–2024 coverage\*\*

\* \*\*Zero missing values\*\*

\* \*\*Zero duplicate rows\*\*



Data validation and exploratory checks were performed before analysis and visualization.



\---



\## Limitations



The analysis has several limitations:



1\. The data is aggregated at the \*\*national level\*\*, so county-level differences are not captured.

2\. Annual climate measurements may hide important seasonal effects such as short dry spells or rainfall timing.

3\. Pearson correlation measures linear association and does not establish causation.

4\. Other important agricultural factors such as fertilizer use, soil conditions, pests, diseases, irrigation, farming practices, and economic conditions were not fully incorporated.

5\. The analysis focuses on historical descriptive relationships rather than predictive modeling.



\---



\## Recommendations



Based on the findings, the following areas deserve attention:



\### 1. Sustainable Intensification



Increasing productivity through improved agricultural practices may reduce the need to rely heavily on further expansion of cultivated land.



\### 2. Water Management



Improved water management and irrigation can help reduce vulnerability to rainfall variability.



\### 3. Climate-Smart Agriculture



Farmers and agricultural planners can consider climate-resilient farming practices to manage changing temperature and precipitation conditions.



\### 4. Improved Data Collection



Future analysis could incorporate county-level production and climate data to identify regional differences within Kenya.



\### 5. Expanded Analytics



Future versions of the project could incorporate variables such as:



\* Soil characteristics

\* Fertilizer application

\* NDVI/vegetation indices

\* Irrigation

\* Pest and disease occurrence

\* County-level climate data



These additional variables could support more advanced agricultural analytics and, where appropriate, future predictive modeling.



\---



\## Conclusion



The analysis shows that Kenya's maize production increased substantially between 2000 and 2024.



The largest contributor to this growth was \*\*expansion of harvested area\*\*, accounting for approximately \*\*70.68%\*\* of the decomposed production increase, while yield improvement contributed approximately \*\*18.21%\*\*.



Precipitation showed a moderate positive association with maize yield (\*\*r = 0.61\*\*), while temperature showed a weak negative association (\*\*r = -0.22\*\*).



Overall, the findings demonstrate the value of combining agricultural and climate data to understand historical maize production patterns and support evidence-based agricultural planning.



\---



\## References



\* Food and Agriculture Organization of the United Nations (FAOSTAT)

\* World Bank Climate Change Knowledge Portal (CCKP)

\* Intergovernmental Panel on Climate Change (IPCC)

\* Kenya National Bureau of Statistics (KNBS)

\* Lobell, D. B., \& Field, C. B. (2007). Global scale climate–crop yield relationships and the impacts of recent climate trends.



\---



\## Project Status



\*\*Status:\*\* Completed



\*\*Analysis Period:\*\* 2000–2024



\*\*Project Type:\*\* Data Analytics



\*\*Main Technologies:\*\* Python, Jupyter Notebook, Power BI, Git, GitHub

