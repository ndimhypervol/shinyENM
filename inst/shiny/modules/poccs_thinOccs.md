### **Module:** ***Spatial Thin***

**BACKGROUND**

In addition to the possibility of errors regarding identification and georeferencing, datasets of occurrence records typically suffer from the effects of uneven (i.e., biased) sampling across geographic space. An example would be higher sampling effort near roads and established research centers. Geographically biased sampling also often results in biases in environmental space, which distorts estimates of the species' niche (Kadmon et al. 2004). Furthermore, this can falsely inflate estimates of model performance (Veloz 2009). Although these problems are well recognized, the field has not yet reached consensus regarding best practices (either conceptually or operationally). Nevertheless, some ways of dealing with this problem include: 1) quantifying heterogeneity in sampling effort across geography by, for example, sampling for a "target group" of species detected with the same techniques (Anderson 2003) and correcting for such spatial sampling patterns during model building (Phillips et al. 2009) not currently implemented in *Wallace*; or 2) reducing the effects of biased sampling by thinning records based on geographic distance (implemented here) or environmental distances (Varela et al. 2014).

**IMPLEMENTATION**

This module implements the R package `spThin`, which removes localities less than a specified geographic distance from other localities (Aiello-Lammens et al. 2015). 

If run with sufficient (independent) repetitions, `spThin` will produce at least one dataset that retains the maximal number of localities possible while satisfying the constraint of the minimum distance between them. This distance is user-specified and typically decided by expert opinion. Alternatively, it could be determined empirically for a given dataset through experiments that apply various filtering distances and select the one that performs best in independent evaluations (Boria et al. 2014). As implemented here, `spThin` is run for 100 repetitions and returns one thinned dataset with the maximum retained number of localities. Users are also able to reset the occurrence dataset back to its original localities to compare different filtering distances. Finally, users can download a .csv file of the thinned localities.

**REFERENCES**

Aiello-Lammens M.E., Boria R.A., Radosavljevic A., Vilela B., Anderson R.P. (2015). spThin: an R package for spatial thinning of species occurrence records for use in ecological niche models. *Ecography*. 38: 541-545.

Anderson R.P. (2003). Real vs. artefactual absences in species distributions: tests for *Oryzomys albigularis* (Rodentia: *Muridae*) in Venezuela. *Journal of Biogeography*. 30: 591-605.

Boria R.A., Olson L.E., Goodman S.M., Anderson R.P. (2014). Spatial filtering to reduce sampling bias can improve the performance of ecological niche models. *Ecological Modelling*. 275: 73-77.

Kadmon R., Farber O., Danin A. (2004). Effect of roadside bias on the accuracy of predictive maps produced by bioclimatic models. *Ecological Applications*. 14:401-413.

Phillips S.J., Dudík M., Elith J., Graham C.H., Lehmann A., Leathwick J., Ferrier S. (2009). Sample selection bias and presence-only distribution models: implications for background and pseudo-absence data. *Ecological Applications*. 19:181-197.

Varela S., Anderson R.P., García-Valdés R., Fernández-González F. (2014). Environmental filters reduce the effects of sampling bias and improve predictions of ecological niche models. *Ecography*. 37: 1084-1091.

Veloz S.D. (2009). Spatially autocorrelated sampling falsely inflates measures of accuracy for presence-only niche models. *Journal of Biogeography*. 36: 2290-2299.
