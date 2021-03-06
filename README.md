# Coronavirus (Covid-19) Data in Nigeria
[ [Confirmed cases](https://github.com/6ones/covid-19-data.ng/blob/master/confirmed.csv) ([raw CSV](https://raw.githubusercontent.com/6ones/covid-19-data.ng/master/confirmed.csv)) | [Discharged cases](https://github.com/6ones/covid-19-data.ng/blob/master/discharged.csv) ([raw CSV](https://raw.githubusercontent.com/6ones/covid-19-data.ng/master/discharged.csv)) | [Deaths](https://github.com/6ones/covid-19-data.ng/blob/master/deaths.csv) ([raw CSV](https://raw.githubusercontent.com/6ones/covid-19-data.ng/master/deaths.csv)) ]

The NCDC is doing a really good job collecting data and [reporting it](https://ncdc.gov.ng/diseases/sitreps/?cat=14&name=An%20update%20of%20COVID-19%20outbreak%20in%20Nigeria) (and also sending text messages), but it's not in a format useful for analysis. It is released daily in a pdf file (some days are missing as well). To use this data for anything you would need to do some **hocus pocus**.

Luckily, I am doing that for you.

The first confirmed case of the coronavirus pandemic was announced in Nigeria on the 27th February 2020, however this data starts from the 29th February, you however will not lose any useful information as that stayed at one case for the next one week, till a second case was recorded on the 9th of March.

## Nigeria Data

This is not the first curation of the data on the coronavirus pandemic in Nigeria, you can see something similar [here](https://github.com/CSSEGISandData/COVID-19), provided by the John Hopkins University.

However, this is the first data on coronavirus in Nigeria curated at a geographical level: **States**.

I have compiled this time series at a state level (starting from the 29th February 2020), meaning every state is represented in these files, including those without any known coronavirus case (Cross River & Kogi).

> Below is a screenshot of what is in the confirmed.csv file, showing cases from the 10th of April up to the 29th

![confirmed cases](https://github.com/6ones/covid-19-data.ng/blob/master/images/screenshot%20confirmed%20cases.png)

The data can be found in three files

- confirmed.csv - contains confirmed cases
- discharged.csv - contains discharged cases
- deaths.csv - contains deaths recorded

Each row of data reports cumulative counts based on the NCDC up to the moment an update is published. I do my best to revise earlier entries in the data when I receive new information.

## Reading Data

To get the data, you either clone the repository using git:

`git clone https://github.com/6ones/covid-19-data.ng.git`

Or download the raw files as indicated above.

To read the data into a dataframe, you can do the following:
```python
import pandas as pd

confirmed = pd.read_csv('confirmed.csv', index_col='date')
discharged = pd.read_csv('discharged.csv', index_col='date')
deaths = pd.read_csv('deaths.csv', index_col='date')
```

## Contact Me

If you have any questions or observation regarding the data or licensing condtion, please contact me at:

[promise.bones@gmail.com](mailto:promise.bones@gmail.com)
