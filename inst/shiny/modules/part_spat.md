### **Module:** ***Spatial Partition***

**BACKGROUND**

Spatial partitions have important advantages over non-spatial ones when sampling bias is known or suspected, and when the application will require transfer across space and/or time. For such transfers, researchers may desire a spatial-partitioning scheme that mimics the likely degree of environmental extrapolation that will be necessary for the final use of the model (e.g., across regions for invasive species or across time for climate-change studies).

**IMPLEMENTATION**

This module implements functionalities from the R package `ENMeval` to partition the occurrence localities into training and testing datasets. 

The user can choose one of three means of spatial partitioning: the 1) "block", 2) "checkerboard 1", or 3) "checkerboard 2" options. Depending on the strenth of the aggregation factors chosen for 2) and 3), these three means of partitioning will vary in the degree of spatial independence of points among partitions (and likely also in the need for environmental extrapolation to make predictions to regions corresponding to withheld points). The "block" method draws a latitudinal and then a longitudinal line to create four groups of localities corresponding to spatial rectangles (*k* = 4). These rectangles hold similar numbers of localities but typically differ in area. The "checkerboard 1" method breaks the extent into a checkerboard pattern and attributes localities to one of two groups depending on which square they fall in (*k* = 2). The "checkerboard 2" method is similar, but adds another level of hierarchy to the spatial grouping, resulting in *k* = 4 groups. Specifically, a coarser checkerboard is placed on top of "checkerboard 1" with grid size equal to a user-specified "aggregation factor" that is multiplied by the length of the finer grid. Later versions of *Wallace* may include other varieties, such as more sophisticated nearest neighbor approaches to partitioning. For more details about these partitioning methods, see Muscarella et al. (2014). Users can download a .csv that includes all the localities retained thus far with an extra column for partition group, plus all the background points sampled in Component **Process Environmental Data**.

**REFERENCES**

Muscarella R., Galante P.J., Soley-Guardia M., Boria R.A., Kass J.M., Uriarte M., Anderson R.P. (2014). ENMeval: An R package for conducting spatially independent evaluations and estimating optimal model complexity for Maxent ecological niche models. *Methods in Ecology and Evolution*. 5: 1198-1205.
