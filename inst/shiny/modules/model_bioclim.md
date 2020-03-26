### **Module:** ***BIOCLIM***

**BACKGROUND**

BIOCLIM is one of the simplest techniques for estimating a species' niche and distribution. It characterizes the species' observed environments (upper and lower limits of the training localities) for each axis independently, thereby delimiting its environmental envelope (or *n*-dimensional hypervolume of Hutchinson; Booth et al. 2014). To do so and indicate conditions that are successively more commonly inhabited (inferred higher suitability), BIOCLIM generates a percentile distribution for each environmental predictor variable, considering the values associated with all occurrence localities. It then evaluates the ranking of environmental values for occurrence localities and other grid cells in the study region based on where they fall on these distributions (Hijmans and Graham 2006). The closer to the median percentile value, the more suitable an environmental value is considered, with both tails of the distribution interpreted identically. The minimum percentile score (full range of observed conditions) for *any* predictor variable is displayed on the map in Module ***Map Prediction*** in Component **Visualize Model Results** (see below). 

**IMPLEMENTATION**

This model uses the R package `dismo` to build BIOCLIM models, and evaluates them with custom code modified from the R package `ENMeval` (Muscarella et al. 2014). 

*Wallace* offers the BIOCLIM implementation available in `dismo`. BIOCLIM models are built and evaluated using the partitions assigned in Component **Partition Occurrence Data**. The rows in the results table correspond to evaluation statistics calculated, and the "Bin" columns refer to the different partitions. Users can download a .csv file of the evaluation statistics table. Further, the model results can be viewed graphically in Component **Visualize Model Results** with Module ***BIOCLIM Envelope Plots***.

**REFERENCES** 

Booth T.H., Nix H.A., Busby J.R., Hutchinson M.F. (2014). BIOCLIM: The first species distribution modelling package, its early applications and relevance to most current MaxEnt studies. *Diversity and Distributions*. 20: 1-9.

Hijmans, R. J., & Graham, C. H. (2006). The ability of climate envelope models to predict the effect of climate change on species distributions. *Global Change Biology*. 12: 2272-2281.

Muscarella R., Galante P.J., Soley-Guardia M., Boria R.A., Kass J.M., Uriarte M., Anderson R.P. (2014). ENMeval: An R package for conducting spatially independent evaluations and estimating optimal model complexity for Maxent ecological niche models. *Methods in Ecology and Evolution*. 5: 1198-1205.
