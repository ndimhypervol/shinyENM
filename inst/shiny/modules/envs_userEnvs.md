### **Module:** ***User-specified Environmental Data***

**BACKGROUND**

Users may want to use environmental data that they have compiled themselves for use in the *Wallace* analysis.

**IMPLEMENTATION**

Users may upload one or more raster files, which must be in single-file format (e.g. .tif, .asc) and not multi-file (e.g. .grd + .gri, .bil + .hdr). Additionally, all rasters must have the same extent and resolution (cell size).

**NOTES**

If the input rasters have no coordinate reference system (CRS) defined (listed as NA), users will be unable to map the rasters in later components. Users will be notified of this in **Module:** ***Map Prediction*** in **Component: Visualize Model Results**, and the mapping functionality will not work. To remedy this problem, users can define the CRS for each raster and save the new version in R with the following code:

```{r}
library(raster)
r <- raster(path_to_raster_file)
# an example for the common CRS called WGS84 (a latitude / longitude projection)
# the text format for these CRS's is called proj4
crs(r) <- crs("+proj=longlat +ellps=WGS84 +datum=WGS84 +no_defs")
# save the raster with defined CRS to file
writeRaster(r, path_to_new_projected_raster_file)
```

Users will need to know what the original CRS of their rasters is, then look up (i.e., Google search) its proj4 format. After saving, upload the new projected rasters and continue with your analysis. 

**NOTE**: A reminder that some file types like .asc cannot embed CRS information in the file, so please avoid these types -- instead use types such as .tif that retain the CRS.
