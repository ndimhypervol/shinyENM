### **Module:** ***Draw Study Region***

**BACKGROUND**

For niche/distribution modeling approaches that compare the environments associated with species presence data with that of some comparison dataset (including Maxent; see Component **Model**), selection of a study region is critical. This decision defines the extent of grid cells for the comparison dataset (absences provided by the user, or pseudoabsence or background points sampled by the algorithm; Anderson 2013). Various, sometimes conflicting, principles for selecting a study region have been set forth in the literature (Peterson et al. 2011 chap. 7). Many researchers emphasize the geographic or environmental domain over which to build the model, whereas others suggest identification of areas where the species is likely to be at environmental equilibrium with the predictor variables (Vanderwal et al. 2009; Anderson and Raza 2010; Barve et al. 2011; Saupe et al. 2012; Franklin 2010 chap. 4; Anderson 2013; Merow et al. 2013). For example, one critical guiding principle (when estimates of suitability are desired, especially for use in other places and times) is that the study region should not include geographic areas that the species does not inhabit due to dispersal barriers. Inclusion of such areas will send a false negative signal, biasing the model's estimated response to the environment (Anderson 2015). Despide these theoretical suggestions, operational selection of the study region usually still depends on expert opinion and available natural history information (Acevedo et al. 2012; Gerstner et al. 2018).

**IMPLEMENTATION** 

This module relies on important functions from the R packages `sp` (for defining spatial objects) and `rgeos` (for buffering spatial objects).  

In this module, *Wallace* provides three simple ways to delimit a study region, by: 1) bounding box (rectangle with most the extreme coordinates in the four cardinal directions as vertices); 2) minimum convex polygon (a convex shape drawn around localities with minimized area), or 3) buffers around occurrence points. For each of these options, users can specify a buffer distance (in degrees; i.e. not meters). *Wallace* then masks the environmental grids by the resulting polygon. Users can download the masked grids as three raster grid formats (.asc, .grd, and .tif).

**REFERENCES**

Acevedo, P., Jiménez‐Valverde, A., Lobo, J. M Real, R. (2012). Delimiting the geographical background in species distribution modelling. *Journal of Biogeography*. 39: 1383-1390.

Anderson R.P., Raza A. (2010). The effect of the extent of the study region on GIS models of species geographic distributions and estimates of niche evolution: preliminary tests with montane rodents (genus *Nephelomys*) in Venezuela. *Journal of Biogeography*. 37: 1378-1393.

Anderson R.P. (2013). A framework for using niche models to estimate impacts of climate change on species distributions. *Annals of the New York Academy of Sciences*. 1297: 8-28.

Anderson, R. P. (2015). El modelado de nichos y distribuciones: no es simplemente "clic, clic, clic." [With English and French translations: Modeling niches and distributions: it's not just "click, click, click" and La modélisation de niche et de distributions: ce n'est pas juste "clic, clic, clic"]. *Biogeografía*. 8: 4-27.

Barve N., Barve V., Jiménez-Valverde A., Lira-Noriega A., Maher S.P., Peterson A.T., Soberón J., Villalobos F. (2011). The crucial role of the accessible area in ecological niche modeling and species distribution modeling. *Ecological Modelling*. 222: 1810-1819.

Franklin J. (2010). Mapping Species Distributions: Spatial Inference and Prediction. Data for species distribution models: the biological data. In: Mapping species distributions: spatial inference and prediction. Cambridge: Cambridge University Press.

Gerstner, B. E., Kass, J. M., Kays, R., Helgen, K. M., Anderson, R. P. (2018). Revised distributional estimates for the recently discovered olinguito (Bassaricyon neblina), with comments on natural and taxonomic history. *Journal of Mammalogy*. 99: 321-332.

Merow, C., Smith, M. J., & Silander, J. A. (2013). A practical guide to MaxEnt for modeling species' distributions: what it does, and why inputs and settings matter. *Ecography*. 36: 1058-1069.

Peterson A. T., Soberón J., Pearson R. G., Anderson R. P., Martinez-Meyer E., Nakamura M., Araújo M. B. (2011). Modeling Ecological Niches. In: *Ecological Niches and Geographic Distributions*. Princeton, New Jersey: Monographs in Population Biology, 49. Princeton University Press.

Saupe, E. E., Barve, V., Myers, C. E., Soberón, J., Barve, N., Hensz, C. M., ... & Lira-Noriega, A. (2012). Variation in niche and distribution model performance: the need for a priori assessment of key causal factors. *Ecological Modelling*. 237: 11-22.

VanDerWal, J., Shoo, L. P., Graham, C., & Williams, S. E. (2009). Selecting pseudo-absence data for presence-only distribution modeling: How far should you stray from what you know?. *Ecological Modelling*. 220: 589-594.
