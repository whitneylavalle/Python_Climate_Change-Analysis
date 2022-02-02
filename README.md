# Python_Climate_Change-Analysis
This analysis uses a dataset from BP's annual energy review to show key changes and trends in energy consumption levels for about 99 entities globally. 

Tableau Link - https://public.tableau.com/app/profile/whitney.lavalle/viz/6_7ClimateChangeStorytelling/Story1?publish=yes
This storyboard explores key aspects of my analysis, but not all analysis. For example, the script Task 6.7 includes stationarizing data that is included in this storyboard. 

Data Source:
Percentage of Energy Consumption by Country
The dataset “percentage of energy consumption by country” is an external data source. I found this dataset on Kaggle. It is part of a larger group of datasets collected and scraped from the collected and scraped from the Organization of Economic Co-Operation and Development (OECD), BP Statistical Review of World Energy, International Renewable Energy Agency (IRENA), Berkeley Earth, ClimateWatch, Institute for Health Metrics and Evaluation (IMHE), Our World In Data, Corporate Knights, and the World Resource Institute. I rate this dataset as trustworthy due to the reputable nature of these organizations. 

Data Collection:
This specific dataset is pulled from bp’s Statistical Review of World Energy. This review provides a globally consistent data time series. It is the longest-running compilation of global energy statistics available.The review quantifies energy consumption based on country-specific energy statistics and production figures. These figures are gathered by the bp Review through the collaboration of many government and statistical agencies around the world (e.g. researchers at the Centre for Energy Economics Research and Policy, Heriot-Watt University) who measure and gather years of data on different countries’ annual energy consumption through coal, gas, nuclear energy, solar power, etc. This larger dataset created by the Review was simplified into an energy consumption by country view for eight key energy types. 

Context:
For the past few decades, there has been an increasing global spotlight on the crisis of climate change and its role as an existential threat. Climate change not only includes the change in global temperatures and emissions trends, but the subsequent climate disasters that have and will continue to run rampant globally. However, as an increasing number of countries pass climate-change focused policy, it will be crucial to ensure that the weight of responsibility for change is proportional to the weight of responsibility for current energy consumption. Certain countries in Sub-Saharan contribute a miniscule amount to global emissions and fossil fuel usage, but their citizens are already being displaced by ecosystem damage caused by global emissions leaders. While any country needs to balance imminent needs such as annual GDP stability and unemployment, long-term planning against the effects of climate change must consider country-specific and regional trends in energy consumption and investment in renewables. We cannot use a one-size-fits-all approach to climate-change action. 

Resources:
Kaggle Dataset: https://www.kaggle.com/seraphimstreets/environmentequity-starterpack/tasks
OECD: https://stats.oecd.org/
Our World in Data: https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions, https://ourworldindata.org/energy https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions
ClimateWatch: https://www.climatewatchdata.org/
Corporate Knights: https://www.corporateknights.com/reports/2020-global-100/2020-global-100-ranking-15795648/
IRENA: https://www.irena.org/Statistics/View-Data-by-Topic/Costs/Global-Trends
Institute for Health Metrics and Evaluation: http://www.healthdata.org/
BP Statistical Review of World Energy: https://www.bp.com/en/global/corporate/energy-economics/statistical-review-of-world-energy.html
World Resource Institute: https://www.wri.org/
Country Polygons JSON https://datahub.io/core/geo-countries#resource-countries


Why I chose this data:
I chose this data because I wanted to find a dataset focused on climate change, as sustainability is a passion of mine as an Environmental Studies/Geography graduate. The vast majority of datasets were interesting but had too little data or were from less reliable sources. I found one focused on the daily temperature for major cities across time, but I thought that I could create a more compelling view of climate change responsibility and main contributors through a view of energy consumption. This view and dataset would show not only a vast increase in energy consumption globally, but show which countries are the main contributors to fossil fuel depletion, the highest investors in renewables, etc. 


Data Profile:
This dataset has 5191 rows (including header row) and 11 columns. 
Columns: entity, code, year, Coal Consumption - EJ, Gas Consumption - EJ, Geo Biomass Other - TWh, Hydro Generation - TWh, Nuclear Generation - TWh, Solar Generation - TWh, Wind Generation -TWh, Oil Consumption - EJ. 

Unit meanings in columns:
*EJ=exajoule
*TWh=terawatt-hour
These are units of energy consumption. 

Data wrangling and consistency checks:
I looked at the mean, std, min, quartiles, and max for each field and none are suspicious
I dropped the column “Code’” as there was not a code for each entity/country and it does not add to this analysis
I checked the data types of each column and changed entity (country name) to string type
Checked for mixed type data, there was none
Checked for missing values, there were 20 rows with no values under the entity “Other CIS” which I deleted for this analysis
Checked for duplicates, there were none
Checked the shape of the dataframe before and after wrangling
Exported clean df as df_clean to project folder


Limitations and considerations:
In terms of data limitations, this dataset only represents 99 entities, some of which (e.g. South Africa and Africa) overlap with each other and should not be considered all separate and independent entities. It will be crucial to clarify this throughout the analysis and be careful when using the data for visualizations. 
Ethically, this dataset is provided by bp, who themselves have a role in past and present emissions and even ecosystem disasters such as their infamous oil spill of 2010. While bp’s Statistical Review of World Energy is a reputable source aligned with several well-respected organizations and universities, it is important to keep in mind that bp could have a vested interest in downplaying any alarming trends in fossil fuel usage- particularly oil. 
