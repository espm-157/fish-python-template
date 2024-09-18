---
jupytext:
  formats: md:myst,ipynb
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.4
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# Unit I: Climate Change Module

## Opening Tutorial: Examining CO2 trends in python

- Example from <http://climate.nasa.gov/vital-signs/carbon-dioxide/>
- Raw data from <https://gml.noaa.gov/webdata/ccgg/trends/co2/co2_mm_mlo.txt>

```{code-cell} ipython3
import pandas as pd
import seaborn.objects as so
```

```{code-cell} ipython3
columns = ['year', 'month', 'decimal_date', 'average', 'smooth', 'std_days', 'uncertainty', 'empty']
df = pd.read_csv("https://gml.noaa.gov/webdata/ccgg/trends/co2/co2_mm_mlo.txt", sep="\s+", comment="#", names= columns)
df
```

```{code-cell} ipython3
(
    so.Plot(df, x="decimal_date", y="average")
    .add(so.Line())
)
```

Which months are the CO2 values at the maximum? Minimum?  Why is this?

What rolling average is used in computing the "trend" line?  How does the trend depend on the rolling average?

------------------------

+++

:::{tip} Exercise 1

# Temperature Data

Each of the last years has consecutively set new records on global climate.  In this section we will analyze global mean temperature data.

Data from: <http://climate.nasa.gov/vital-signs/global-temperature>

## Question 1:

Describe the data set to the best of your ability given the documentation provided.  Describe what kind of column each data contains and what units it is measured in.  Then address our three key questions in understanding this data:

- How are the measurements made? What is the associated measurement uncertainty?
- What is the resolution of the data?
- Are their missing values? How should they be handled?

+++

## Question 2:

Construct the necessary python code to import and prepare for manipulation the following data set: <http://climate.nasa.gov/system/internal_resources/details/original/647_Global_Temperature_Data_File.txt>

```{code-cell} ipython3

```

## Question 3:

Plot the trend in global mean temperatures over time.  Describe what you see in the plot and how you interpret the patterns you observe.

```{code-cell} ipython3

```

# Exercise II: Melting Ice Sheets?

- Data description: <http://climate.nasa.gov/vital-signs/land-ice/>
- Raw data file: <http://climate.nasa.gov/system/internal_resources/details/original/499_GRN_ANT_mass_changes.csv>

## Question 1:

- Describe the data set: what are the columns and units? Where do the numbers come from? 
- What is the uncertainty in measurment? Resolution of the data? Interpretation of missing values?

```{code-cell} ipython3

```

## Question 2:

Construct the necessary code to import this data set.

```{code-cell} ipython3

```

## Question 3:

Plot the data and describe the trends you observe.

```{code-cell} ipython3

```

# Exercise III: Rising Sea Levels?

- Data description: <http://climate.nasa.gov/vital-signs/sea-level/>
- Raw data file: <http://climate.nasa.gov/system/internal_resources/details/original/121_Global_Sea_Level_Data_File.txt>


## Question 1:

- Describe the data set: what are the columns and units? 
- Where do these data come from? 
- What is the uncertainty in measurment? Resolution of the data? Interpretation of missing values?

```{code-cell} ipython3

```

## Question 2:

Construct the necessary R code to import this data set as a tidy `Table` object.

```{code-cell} ipython3

```

## Question 3:

Plot the data and describe the trends you observe.

```{code-cell} ipython3

```

# Exercise IV: Arctic Sea Ice?

- <http://nsidc.org/data/G02135>
- <https://noaadata.apps.nsidc.org/NOAA/G02135/north/monthly/data/>

## Question 1:

- Describe the data set: what are the columns and units? 
- Where do these data come from? 
- What is the uncertainty in measurement? Resolution of the data? Interpretation of missing values?

+++

## Question 2:

Construct the necessary code to import this data set

```{code-cell} ipython3

```

## Question 3:

Plot the data and describe the trends you observe.

```{code-cell} ipython3

```

# Exercise V: Longer term trends in CO2 Records


The data we analyzed in the unit introduction included CO2 records dating back only as far as the measurements at the Manua Loa observatory.  To put these values into geological perspective requires looking back much farther than humans have been monitoring atmosopheric CO2 levels.  To do this, we need another approach.


[Ice core data](http://cdiac.ornl.gov/trends/co2/ice_core_co2.html):

Vostok Core, back to 400,000 yrs before present day 

- Description of data set: <http://cdiac.esd.ornl.gov/trends/co2/vostok.html>
- Data source: <http://cdiac.ornl.gov/ftp/trends/co2/vostok.icecore.co2>

## Questions / Tasks:

- Describe the data set: what are the columns and units? Where do the numbers come from? 
- What is the uncertainty in measurment? Resolution of the data? Interpretation of missing values?
- Read in and prepare data for analysis.
- Reverse the ordering to create a chronological record.  
- Plot data
- Consider various smoothing windowed averages of the data. 
- Join this series to Mauna Loa data
- Plot joined data
- Describe your conclusions

```{code-cell} ipython3

```
