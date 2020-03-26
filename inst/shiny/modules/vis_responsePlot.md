### **Module:** ***Plot Response Curves*** 
	
**BACKGROUND**  

In addition to model performance, researchers often are interested in the relationship between the modeled response (suitability) and the predictor variables. Presence-background models are usually some variation of an additive model. For example, the estimated suitability in a Maxent model represents the sum of contributions of various features (e.g. environmental variables or functions thereof; Phillips et al. 2006). Hence, the relationship between suitability and the values of individual environmental variables (taking into account the availability of environments in the study region) can be expressed as plots commonly termed "response curves" (Elith and Graham 2009). *Wallace* implements marginal response curves using the `dismo` package that plot the modeled response (suitability) on the y-axis and the range of a predictor variable (when all other variables are held at their medians) on the x-axis. 

*Wallace* does not provide response curves for presence-only models (like BIOCLIM) that do not incorporate consideration of background values into the modeling process. As the available background is not considered by such models, their output is biased by any heterogeneity in the frequency of different environments in the study region. Hence, although an entity analogous to a "response curve" can be calculated from the geographic prediction of BIOCLIM, in reality it represents a histogram (biased by environmental frequency), rather than a true response curve indicating relative use of available environments (suitability).

**IMPLEMENTATION** 

This module relies on plotting functionality from R package `dismo`.

Users must first select a model. Depending on the `ENMeval` settings selected in Component **Model**, there may be multiple choices for Maxent. Users must then choose a predictor variable to view its response curve. The predictor variables available for selection in the dropdown menu are the variables with non-zero coefficients in the model (i.e., non-zero lambda values). Users can download the currently displayed response curve plot as an image file (.png).

**REFERENCES**

Elith, J., & Graham, C. H. (2009). Do they? How do they? WHY do they differ? On finding reasons for differing performances of species distribution models. *Ecography*. 32: 66-77.

