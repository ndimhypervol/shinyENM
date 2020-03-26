### **Module:** ***Calculate Environmental Similarity***

**BACKGROUND**  

When projecting a niche/distributional model to new conditions, the new region/time period frequently contains environmental values and combinations different than those where it was made (termed "non-analog conditions"). Realistic use of such projections requires detecting any non-analog conditions and assessing the degree to which extrapolation in environmental space affects the prediction (Williams and Jackson 2007, Fitzpatrick and Hargrove 2009, Anderson 2013). Multivariate environmental similarity surfaces (MESS) constitute one way to address these issues (Elith et al. 2010). High positive values (cooler colors on the map) indicate increasing similarity with the conditions used to train the model, and low negative values (warmer colors on the map) indicate increasing difference.

**IMPLEMENTATION** 

This module relies on the `mess()` function from the R package `dismo`, which calculates a multidimensional similarity surface (Elith et al. 2010).

Users must first select a model. Depending on the `ENMeval` settings selected in Component **Model**, there may be multiple choices for Maxent. Users then draw a polygon on the map to delineate the area for performing the MESS calculations. Once the polygon has been drawn, "Select" chooses this extent, and "Calculate" runs the MESS analysis for the selected extent. Users can download the MESS map as either raster grid types for analysis (.asc, .grd and .tif), or as an image file (.png).

**REFERENCES**

Anderson R.P. (2013). A framework for using niche models to estimate impacts of climate change on species distributions. *Annals of the New York Academy of Sciences*. 1297: 8-28.

Elith, J., Kearney, M., & Phillips, S. (2010). The art of modelling range-shifting species. *Methods in Ecology and Evolution*. 1: 330-342.

Fitzpatrick, M. C., & Hargrove, W. W. (2009). The projection of species distribution models and the problem of non-analog climate. *Biodiversity and Conservation*. 18: 2255-2261.

Williams, J. W., & Jackson, S. T. (2007). Novel climates, no-analog communities, and ecological surprises. *Frontiers in Ecology and the Environment*. 5: 475-482.

