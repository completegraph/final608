# ![Cary](https://www.townofcary.org/Home/ShowPublishedImage/26839/637414707996500000)

# The Distribution of Income and Crime By Residential Subdivision in Cary, North Carolina

## Introduction

This application visualizes residential subdivisions in the Town of
Cary, North Carolina, using publicly available data sources on crime and household income.

The motivation to create this application was my limited understanding of the central
role played by residential subdivisions in defining community standards and housing markets.
__Residential subdivisions__ (there are over 700 in this Town) seem to exhibit substantial dispersion in levels of socioeconomic variables like income and crime rates.

Getting detailed quantitative data about residential subdivisions is difficult.

This application has been built as part of the CUNY SPS Data Science Data Visualization course.  

## Technologies Used

This application was written in Python as a Jupyter notebook.

Data cleaning and processing used the `pandas` library.

Geospatial analysis was done using `geopandas`.

Maps were constructed using `folium`.

`Voilà` turns `Jupyter` notebooks into standalone web applications.

I deployed the notebook thorugh **MyBinder.org**  the hosting service for this application.

The code and data are publicly available on the github repository at `completegraph/final608`.

## Data Sources

  1.  Town of Cary boundary in GEOJSON format is provided by the Town of Cary technology support team.   Thanks to them.

  2.  Police Incident data is provided on the Town of Cary Open Data Portal.

  3.  Residential Subdivision data is provided on the Town of Cary Open Data Portal.  There are over 700 subdivisions -- 4 of these lack geospatial data and are omitted as present.

  4.  Household Median Income data is provided from the US Census through the Censusreporter.org at the census tract level.

### Application

The application is hosted at the link below:

#[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/completegraph/final608/master?filepath=voila%2Frender%2Fcary_v3.ipynb)


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/completegraph/final608/master?urlpath=voila%2Frender%2Fcary_v3.ipynb)
[https://mybinder.org/v2/gh/completegraph/final608/master?urlpath=voila%2Frender%2Fcary_v3.ipynb]


### Calculation Methodology

The color coding of the crime heat map and cluster data uses a crime density measure.  That measure is tabulated for all residential subdivisions and the color assigned to a subdivision uses its percentile ranking of crime density vs. all included subdivisions in Cary.   For example, a red rank does not mean the subdivision is unsafe on an absolute basis -- but less safe relative to other subdivisions in Cary.   The measure uses total crime incidents per square kilometer of area of the subdivision.

The color coding of the median household income is based on the census tract containing each residential subdivision.   In a small number of cases, two census tracts divide up a residential subdivision.  I assigned a weighted average household income to that residential subdivision.


## License

We use a shared copyright model that enables all contributors to maintain the
copyright on their contributions.

This software is licensed under the BSD-3-Clause license. See the
[LICENSE](LICENSE) file for details.
