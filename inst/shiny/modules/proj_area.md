### **Module:** ***Project to New Extent***

**BACKGROUND**  

In simple terms, applying or "projecting" a niche/distributional model to a region or time period different from the ones used to make the model involves making a prediction based on the model and the new values of the predictor variables, as long as these values are available for the original region and time period. In reality, however, researchers should be cognizant of many possible pitfalls, including non-analog conditions (e.g., requiring extrapolation in environmental space; see component **Model**) and heterogeneity in the effects of species interactions (Fitzpatrick and Hargrove 2009; Anderson 2013).

**IMPLEMENTATION** 

This module relies on functionality for model prediction grids from the R package `dismo`.

Users must first select a model. Depending on the `ENMeval` settings selected in Component **Model**, there may be multiple choices for Maxent. Users then draw a polygon on the map to delineate the area desired for the new prediction. Once the polygon has been drawn, "Select" chooses this extent for all projection operations. "Project" calculates the modeled response for the predictor variable values for each cell of the selected extent and plots the prediction on the map. Users can download the prediction as either raster grid types for analysis (.asc, .grd and .tif), or as an image file (.png).

Users may choose a thresholding rule to convert the continuous prediction to a binary one (0s and 1s), which can be interpreted as presence/absence or suitable/unsuitable. Please see guidance text for **Component: Model** for more details on thresholding rules. After the model and threshold selections are made, the prediction can be plotted on the map. Users can download the prediction as either raster grid types for analysis (.grd and .asc), or as an image file (.png).

*NOTE*: However, with the maxent.jar option, model predictions are currently always 'clamped' for grid cells with environmental values more extreme than those of the training dataset (background sample plus occurrence records). This is because, due to a bug in the `predict()` function in `dismo`, the "clamping" option is always on for model predictions (i.e., clamping cannot be turned off using dismo, to allow an unconstrained extrapolation beyond the environmental condtions of the training dataset). 

**REFERENCES**

Anderson R.P. (2013). A framework for using niche models to estimate impacts of climate change on species distributions. *Annals of the New York Academy of Sciences*. 1297: 8-28.

Fitzpatrick, M. C., & Hargrove, W. W. (2009). The projection of species distribution models and the problem of non-analog climate. *Biodiversity and Conservation* 18: 2255-2261.

