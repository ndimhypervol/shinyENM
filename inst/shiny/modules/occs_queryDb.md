### **Module:** ***Query Database*** 

**BACKGROUND**  

Over the past two decades, the worldwide biodiversity informatics community has achieved remarkable progress, with many millions of species occurrence records now available online through various databases--including a substantial subset of records with assigned georeferences (e.g., latitude/longitude coordinates; Gaiji et al. 2013; Peterson et al. 2015; Walters and Scholes 2017). These data document the presence of a species at particular points in space and time, along with other useful metadata fields when available (e.g., institution, specimen/observation number, elevation, etc.). The origin of much of this information is specimens in research collections at natural history museums and herbaria, although newer data sources such as citizen-science initiatives are growing contributors as well (Sullivan et al. 2009).

**IMPLEMENTATION** 

This module relies on the R package `spocc`, which provides streamlined access to many species occurrence databases, some of which aggregate data from myriad providers. Users can choose between three of the largest databases: <a href="http://www.gbif.org" target="_blank">GBIF</a>, <a href="http://www.vertnet.org" target="_blank">VertNet</a>, and <a href="https://bison.usgs.gov" target="_blank">BISON</a>. Note that currently users must choose only one of these databases, and any later download overwrites previous ones. 

Records used in downstream analyses in *Wallace* are filtered to remove those without georeferences (latitude/longitude coordinates) and those that have exact duplicate coordinates of other records (including number of decimal places). The "Occs Tbl" tab displays all the filtered records with several key fields: name, longitude, latitude, year, institutionCode, country, stateProvince, locality, elevation, and basisOfRecord (standard field names from GBIF). The records available for download as a .csv file have all original fields and include records without georeferences.

**REFERENCES**

Gaiji, S., Chavan, V., Ariño, A. H., Otegui, J., Hobern, D., Sood, R., & Robles, E. (2013). Content assessment of the primary biodiversity data published through GBIF network: status, challenges and potentials. *Biodiversity Informatics*. 8: 94-172.

Peterson, A. T., Soberón, J., & Krishtalka, L. (2015). A global perspective on decadal challenges and priorities in biodiversity informatics. *BMC Ecology*. 15: 15.

Sullivan, B. L., Wood, C. L., Iliff, M. J., Bonney, R. E., Fink, D., & Kelling, S. (2009). eBird: A citizen-based bird observation network in the biological sciences. *Biological Conservation*. 142: 2282-2292.

Walters, M., and Scholes, R. J., (Eds.). (2017). The GEO Handbook on Biodiversity Observation Networks. Springer International Publishing. Link: http://link.springer.com/book/10.1007/978-3-319-27288-7
