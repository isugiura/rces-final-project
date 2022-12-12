# rces-final-project

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/pangeo-data/pangeo-docker-images/2022.09.21?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252Fisugiura%252Frces-final-project%26urlpath%3Dlab%252Ftree%252Frces-final-project%252Ffinal_project.ipynb%26branch%3Dmain)

## Updated README
### Research Question:
What are the seasonality of the sea surface temperature (SST) and trends in its anomalies (with a special focus on ENSO indices' four Niño regions)?

### Goals
The goal of this project is to build tools to explore the SST seasonality and anomalies (recent variations). Using these tools, we will also compare the four Niño regions that are used in NOAA's ENSO indices (Niño 1.2, Niño 3, Niño 3.4, and Niño 4) to illustrate the differences in SST seasonality and anomalies in those areas.

### Dataset
The SST data will be obtained from NOAA NCEP-NCAR CDAS-1: Climate Data Assimilation System I NCEP-NCAR Reanalysis Project, accessible through the IRI/LDEO Climate Data Library, provides monthly data on the global SST from January 1949 to September 2022.

Link: https://iridl.ldeo.columbia.edu/SOURCES/.NOAA/.NCEP-NCAR/.CDAS-1/.MONTHLY/.Diagnostic/.surface/.temp/

### Summary of Analysis:
1. Compute mean annual SST to establish the norm of the 1949-2022 SST
    - Compare the original global mean annual SST and the detrended one to observe the effects of the recent warming
2. Compute seasonal mean using the "resample" function
3. Compute the seasonal climatology, anomalies, and detrended anomalies using the "groupby" and xrft's "detrend" function
4. Develop interactive visuals using the "ipywidgets"'s "interact" function and hvplot
    - Figure 1: global mean annual SST
    - Figure 2: global SST seasonalities and zonal mean
    - Figure 3: global SST anomalies
    - Figure 4: global vs. regional SST anomalies (with plots to show the magnitude of detrending in them)
5. Focus the analysis on ENSO indices' four Niño regions
    - Figure 5: SST seasonalities in the four Niño regions
    - Figure 6: SST anomalies in the four Niño regions (with plots to compare the number of grids with large anomalies)

-----
-----

## Original README

### Research question:
What are the seasonal variations/patterns of sea surface temperature in the Pacific Ocean?

The goal of this project is to understand the climatology of the Pacific Ocean based on sea surface temperature (SST). The SST data will be obtained from NOAA NCEP-NCAR CDAS-1: Climate Data Assimilation System I NCEP-NCAR Reanalysis Project, accessible through the IRI/LDEO Climate Data Library, provides monthly data on the global SST from January 1949 to September 2022.

### Summary of analysis plans:
1. Obtain the SST for the Pacific Ocean, (detrend the global warming trends if needed), and then partition that dataset into subbasins
2. Compute seasonal mean using the "resample" function
3. Compute the seasonal climatology of each subbasin of the Pacific Ocean using the "groupby" function and map them using the "cartopy" package
4. Develop an interactive visual using the "interact" function of the "ipywidgets" package to demonstrate the seasonal climatology of the Pacific Ocean (without the effect of global warming)
    - Button to choose season
    - Button to choose the temperature unit (C or F)
5. If detrended SST data will be used, then produce a similar interactive visual but using the original SST data to see how much global warming has influenced/altered seasonal SST patterns

### Link to the dataset:
https://iridl.ldeo.columbia.edu/SOURCES/.NOAA/.NCEP-NCAR/.CDAS-1/.MONTHLY/.Diagnostic/.surface/.temp/