### **Module:** ***WorldClim***

**BACKGROUND**

The WorldClim project provides bioclimatic variables for the Earth's land surfaces for all continents except Antarctica. Monthly data from weather stations were spatially extrapolated using elevation as a covariate and subsequently 19 bioclimatic variables were derived, reflecting various aspects of temperature and precipitation (Hijmans et al. 2005). The descriptions of each variable are listed below, taken from the WorldClim <a href="http://www.worldclim.org" target="_blank">website</a>, where more details can be found.

BIO1 = Annual Mean Temperature  
BIO2 = Mean Diurnal Range (Mean of monthly (max temp - min temp))  
BIO3 = Isothermality (BIO2/BIO7) (* 100)  
BIO4 = Temperature Seasonality (standard deviation *100)  
BIO5 = Max Temperature of Warmest Month  
BIO6 = Min Temperature of Coldest Month  
BIO7 = Temperature Annual Range (BIO5-BIO6)  
BIO8 = Mean Temperature of Wettest Quarter  
BIO9 = Mean Temperature of Driest Quarter  
BIO10 = Mean Temperature of Warmest Quarter  
BIO11 = Mean Temperature of Coldest Quarter  
BIO12 = Annual Precipitation  
BIO13 = Precipitation of Wettest Month  
BIO14 = Precipitation of Driest Month  
BIO15 = Precipitation Seasonality (Coefficient of Variation)  
BIO16 = Precipitation of Wettest Quarter  
BIO17 = Precipitation of Driest Quarter  
BIO18 = Precipitation of Warmest Quarter  
BIO19 = Precipitation of Coldest Quarter  

**IMPLEMENTATION**

This module relies on the R package `raster` to download bioclimatic variables from the WorldClim server. 

*Wallace* makes all four resolutions of the data available (10 arcmin &asymp; 20 km, 5 arcmin &asymp; 10 km, 2.5 arcmin &asymp; 5 km, and 30 arcsec &asymp; 1 km). The finest grain WorldClim dataset (30 arcsec) can only be downloaded by 30 x 30 degree tiles in the current implementation of `dismo` (1.1-1), and so *Wallace* uses the current center of the map display as the tile reference. This means that analyses with 30 arcsec climatic data using the current version of *Wallace* are restricted to the extent of a single tile. When running locally, the dataset is downloaded to the *Wallace* folder (which can take substantial time), but *Wallace* will use the downloaded data for later runs when the same resolution is selected.

**REFERENCES**

Hijmans, R. J., Cameron, S. E., Parra, J. L., Jones, P. G., Jarvis, A. 2005. Very high resolution interpolated climate surfaces for global land areas. *International Journal of Climatology*. 25: 1965-1978.
