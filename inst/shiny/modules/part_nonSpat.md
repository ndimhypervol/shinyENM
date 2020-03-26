### **Module:** ***Non-spatial Partition***

**BACKGROUND**

Non-spatial partitions are useful when no sampling bias exists and when the model will not be used for transfer across space or time (or when too few localities exist to implement spatial partitions).

**IMPLEMENTATION**

This module implements functionalities from the R package `ENMeval` to partition the occurrence localities into training and testing datasets. 

These non-spatial partitions are either via a: 1) jackknife procedure where each occurrence record is put into a unique group (*k* equals the number of localities; technically an n - 1 jackknife), which is appropriate for small sample sizes (Pearson et al. 2007, Shcheglovitova and Anderson, 2013); or 2) random *k*-fold, where localities are randomly assigned to a group (the number of groups, *k*,  is user-defined), an approach suggested for larger sample sizes. For more details about these partitioning methods, see Muscarella et al. (2014). Users can download a .csv that includes all the localities retained thus far with an extra column for partition group, plus all the background points sampled in Component **Process Environmental Data** (partition value = 0).

**REFERENCES**

Muscarella R., Galante P.J., Soley-Guardia M., Boria R.A., Kass J.M., Uriarte M., Anderson R.P. (2014). ENMeval: An R package for conducting spatially independent evaluations and estimating optimal model complexity for Maxent ecological niche models. *Methods in Ecology and Evolution*. 5: 1198-1205.

Pearson, R. G., Raxworthy, C. J., Nakamura, M., & Townsend Peterson, A. (2007). Predicting species distributions from small numbers of occurrence records: a test case using cryptic geckos in Madagascar. *Journal of Biogeography*. 34: 102-117.

Shcheglovitova, M. and R. P. Anderson. (2013). Estimating optimal complexity for ecological niche models: a jackknife approach for species with small sample sizes. *Ecological Modelling*. 269: 9-17.
