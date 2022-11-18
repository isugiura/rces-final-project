# rces-final-project

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/pangeo-data/pangeo-docker-images/2022.09.21?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252Fisugiura%252Frces-final-project%26urlpath%3Dlab%252Ftree%252Frces-final-project%252Ffinal_project.ipynb%26branch%3Dmain)

Research question:
What are the seasonal variations/patterns of sea surface temperature in the Pacific Ocean?

The goal of this project is to understand the climatology of the Pacific Ocean based on sea surface temperature (SST). The SST data will be obtained from NOAA NCEP-NCAR CDAS-1: Climate Data Assimilation System I NCEP-NCAR Reanalysis Project, accessible through the IRI/LDEO Climate Data Library, provides monthly data on the global SST from January 1949 to September 2022.

Summary of analysis plans:
1. Obtain the SST for the Pacific Ocean, (detrend the global warming trends if needed), and then partition that dataset into subbasins
2. Compute seasonal mean using the "resample" function
3. Compute the seasonal climatology of each subbasin of the Pacific Ocean using the "groupby" function and map them using the "cartopy" package
4. Develop an interactive visual using the "interact" function of the "ipywidgets" package to demonstrate the seasonal climatology of the Pacific Ocean (without the effect of global warming)
    - Button to choose season
    - Button to choose the temperature unit (C or F)
5. If detrended SST data will be used, then produce a similar interactive visual but using the original SST data to see how much global warming has influenced/altered seasonal SST patterns



Link to the dataset:
https://iridl.ldeo.columbia.edu/SOURCES/.NOAA/.NCEP-NCAR/.CDAS-1/.MONTHLY/.Diagnostic/.surface/.temp/