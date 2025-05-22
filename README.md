# Hate-Crime-Tristate-Data
Hate crimes recorded by the FBI across the tri-state region from 2020 to 2023

For this project, I have created a data pipeline using the FBI's hate crime dataset. On the CDE website, they stated that the most up-to-date data included records up to 2023.
Preferably, I was also looking forward to working with 2024 data, but based on when data is updated, I would have had to wait until September of this year (2025) to access 2024 records.
Furthermore, the website did not provide me with a data dictionary, so I had to make my own.
Regardless, given what I have, I will be giving my first attempt at building a proper data pipeline.


This project has 6 main components, which are as follows:
- Data sourcing
- Defining the business requirements
- Defining the functional requirements
- Creating an information architecture
- Creating a data architecture
- Dimensional modeling

The uploaded PDF explains my data and where I sourced it. It also defines my business and functional requirements and displays my architecture models with brief descriptions for each.
I also uploaded my star schema model as a DBS file and a separate PDF file titled "dimension_model," which lists the facts and dimensions.

## Business Requirements
Thousands of hate crime incidents occur across the tri-state region each year. My goal is to
collect and store data from 2020-2023, enabling year-over-year comparisons to show us
- Shifts in incident frequency
- Commonly targeted groups within the Tri-state region
  
## Functional Requirements
This system will allow users to do the following:
- Filter hate crime based on location, date, and types of offenses
- Create year-over-year comparison reports
- Display interactive charts that compare trends by year or location
- Download query results in different formats for external analysis

## Data Requirements
The data I am working with is a structured CSV file that contains historic records of hate crimes committed in the US.
My data has an unstructured part, which is my reference data. This part explains the values in my data.

## Tools
For this project, I have decided to use:
- Google Cloud Storage - Temporary storage
- Google Colab - Python environment for ETL
- Snowflake - [Data Warehouse](https://app.snowflake.com/east-us-2.azure/zqa66309/w5E5MoeZbp0T#query)
- Tableau - Visualization tool

## Pipeline Process
1) Download data from the [source](https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/downloads)
2) Upload data and dictionary into Google Cloud Storage (GCS)
3) Perform ETL in Google Colab and convert clean data to CSV
4) Load cleaned data into GCS and Snowflake
5) Perform visualizing data with Tableau

## Visuals and Findings
1) [Tableau Dashboard and Heat Map](https://public.tableau.com/views/Tri-StateHateCrimeInformation/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
2) [Findings](https://docs.google.com/document/d/1JI1c791Uc9pVhnyeMdfkCzGew7WcTbrX5Sn_XRVI4V4/edit?usp=sharing)

## Moving Forward
While doing my visualization, I noticed certain values, such as offense type and location name, had zero records. The fact that they are there as an option opens the door for questions such as what state has the most common reporting of those incidents, or what year did those incident reports peak. You are welcome to take your approach to this project with a different business requirement or functional requirement that better suits your research.
