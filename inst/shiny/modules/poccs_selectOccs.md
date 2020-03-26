### **Module:** ***Select Occurrences On Map***

**BACKGROUND**  

Despite their great utility, aggregated biodiversity occurrence datasets typically contain errors both in identification and in georeferencing. Many, but certainly not all, such errors can be spotted by simple visual inspection of the localities plotted on a map (Gaiji et al. 2013). For example, if a species is known only from high elevation forest, and a few localities from an online database are in a lowland grassland, this suspicious pattern may lead users to exclude these records from the analysis. This module can also be used to narrow the analysis on a regional subset of available records.

**IMPLEMENTATION**

The R package `leaflet.extras` provides a drawing tool plugin to the `leaflet` map for this module, which allows users to draw a polygon to specify which occurrences to retain in the analysis. 

Occurrences that fall within (i.e. overlap with) the polygon are retained, and all others are removed from the analysis. Users can then draw other polygons to select other groups of localities. This process can be repeated until all the desired localities are selected. Users are also able to reset the occurrence dataset back to the original localities. Finally, users can download a .csv file of the edited localities.

**REFERENCES**

Gaiji, S., Chavan, V., Ariño, A. H., Otegui, J., Hobern, D., Sood, R., Robles, E. (2013). Content assessment of the primary biodiversity data published through GBIF network: status, challenges and potentials. *Biodiversity Informatics*. 8: 94-172.
