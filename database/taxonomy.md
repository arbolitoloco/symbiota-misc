# Taxonomy in Symbiota

Taxonomic information is stored in a few different tables in Symbiota. In the **occurrence** table can be stored the accepted determination information and remarks can be. The **determinations** table keeps track of the determination history of occurrences. Finally, there are tables that keep track of the taxonomic names, authorship, references and hierarchy.

## Occurrence table

| column_type      | dwc_definition                                                                       | symbiota_def                                 |
| ---------------- | ------------------------------------------------------------------------------------ | -------------------------------------------- |
| varchar(255)     | [family](https://dwc.tdwg.org/terms/#dwc:family)                                     |                                              |
| varchar(255)     | [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName)                     |                                              |
| varchar(255)     | [sciname]()                                                                          | full scientific name, with or without author |
| int(10) unsigned | [tidinterpreted]()                                                                   | internal id for accepted taxon               |
| varchar(255)     | [genus](https://dwc.tdwg.org/terms/#dwc:genus)                                       |                                              |
| varchar(255)     | [specificEpithet](https://dwc.tdwg.org/terms/#dwc:specificEpithet)                   |                                              |
| varchar(32)      | [taxonRank](https://dwc.tdwg.org/terms/#dwc:taxonRank)                               |                                              |
| varchar(255)     | [infraspecificEpithet](https://dwc.tdwg.org/terms/#dwc:infraspecificEpithet)         |                                              |
| varchar(255)     | [scientificNameAuthorship](https://dwc.tdwg.org/terms/#dwc:scientificNameAuthorship) |                                              |
| text             | [taxonRemarks](https://dwc.tdwg.org/terms/#dwc:taxonRemarks)                         |                                              |
| varchar(255)     | [identifiedBy](https://dwc.tdwg.org/terms/#dwc:identifiedBy)                         |                                              |
| varchar(45)      | [dateIdentified](https://dwc.tdwg.org/terms/#dwc:dateIdentified)                     |                                              |
| text             | [identificationReferences](https://dwc.tdwg.org/terms/#dwc:identificationReferences) |                                              |
| text             | [identificationRemarks](https://dwc.tdwg.org/terms/#dwc:identificationRemarks)       |                                              |
| varchar(255)     | [identificationQualifier](https://dwc.tdwg.org/terms/#dwc:identificationQualifier)   |                                              |

## Determinations table

## Taxon table

## Published Darwin Core Archive and search results

The DwCA packages published for each collection, as well as the dataset available for download when performing a search, contain the taxonomic information and determination history, when available, for each occurrence listed.
