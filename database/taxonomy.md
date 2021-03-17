# Taxonomy in Symbiota database

Taxonomic information is stored in a few different tables in Symbiota. In the **occurrence** table both the accepted determination information and taxonomic remarks can be stored. The **determinations** table keeps track of the determination history of occurrences. Finally, there are tables that keep track of the taxonomic names, authorship, references and hierarchy. The fields below are only partial descriptions of each table, limited to those referring to taxonomic information.

## Occurrence table

| column_name              | column_type      | dwc_definition                                                                       | symbiota_def                                 |
| ------------------------ | ---------------- | ------------------------------------------------------------------------------------ | -------------------------------------------- |
| family                   | varchar(255)     | [family](https://dwc.tdwg.org/terms/#dwc:family)                                     |                                              |
| scientificName           | varchar(255)     | [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName)                     |                                              |
| sciname                  | varchar(255)     |                                                                                      | full scientific name, with or without author |
| tidinterpreted           | int(10) unsigned |                                                                                      | internal id for accepted taxon               |
| genus                    | varchar(255)     | [genus](https://dwc.tdwg.org/terms/#dwc:genus)                                       |                                              |
| specificEpithet          | varchar(255)     | [specificEpithet](https://dwc.tdwg.org/terms/#dwc:specificEpithet)                   |                                              |
| taxonRank                | varchar(32)      | [taxonRank](https://dwc.tdwg.org/terms/#dwc:taxonRank)                               |                                              |
| infraspecificEpithet     | varchar(255)     | [infraspecificEpithet](https://dwc.tdwg.org/terms/#dwc:infraspecificEpithet)         |                                              |
| scientificNameAuthorship | varchar(255)     | [scientificNameAuthorship](https://dwc.tdwg.org/terms/#dwc:scientificNameAuthorship) |                                              |
| taxonRemarks             | text             | [taxonRemarks](https://dwc.tdwg.org/terms/#dwc:taxonRemarks)                         |                                              |
| identifiedBy             | varchar(255)     | [identifiedBy](https://dwc.tdwg.org/terms/#dwc:identifiedBy)                         |                                              |
| dateIdentified           | varchar(45)      | [dateIdentified](https://dwc.tdwg.org/terms/#dwc:dateIdentified)                     |                                              |
| identificationReferences | text             | [identificationReferences](https://dwc.tdwg.org/terms/#dwc:identificationReferences) |                                              |
| identificationRemarks    | text             | [identificationRemarks](https://dwc.tdwg.org/terms/#dwc:identificationRemarks)       |                                              |
| identificationQualifier  | varchar(255)     | [identificationQualifier](https://dwc.tdwg.org/terms/#dwc:identificationQualifier)   |                                              |

## Determinations table

| column_name               | column_type      | dwc_definition                                                                       | symbiota_def                                 |
| ------------------------- | ---------------- | ------------------------------------------------------------------------------------ | -------------------------------------------- |
| detid                     | int(10) unsigned |                                                                                      | internal id for determinator                 |
| occid                     | int(10) unsigned |                                                                                      | internal id for occurrence                   |
| identifiedBy              | varchar(60)      | [identifiedBy](https://dwc.tdwg.org/terms/#dwc:identifiedBy)                         |                                              |
| idbyid                    | int(10) unsigned |                                                                                      | internal id                                  |
| dateIdentified            | varchar(45)      | [dateIdentified](https://dwc.tdwg.org/terms/#dwc:dateIdentified)                     |                                              |
| dateIdentifiedInterpreted | date             |                                                                                      | internal usage                               |
| sciname                   | varchar(100)     |                                                                                      | full scientific name, with or without author |
| tidinterpreted            | int(10) unsigned | [tidinterpreted](https://dwc.tdwg.org/terms/#dwc:tidinterpreted)                     | internal id for accepted taxon               |
| scientificNameAuthorship  | varchar(100)     | [scientificNameAuthorship](https://dwc.tdwg.org/terms/#dwc:scientificNameAuthorship) |                                              |
| identificationQualifier   | varchar(45)      | [identificationQualifier](https://dwc.tdwg.org/terms/#dwc:identificationQualifier)   |                                              |
| iscurrent                 | int(2)           |                                                                                      | defines if determination is current          |
| printqueue                | int(2)           |                                                                                      | internal usage                               |
| appliedStatus             | int(2)           |                                                                                      | internal usage                               |
| detType                   | varchar(45)      |                                                                                      | internal usage                               |
| identificationReferences  | varchar(255)     | [identificationReferences](https://dwc.tdwg.org/terms/#dwc:identificationReferences) |                                              |
| identificationRemarks     | varchar(500)     | [identificationRemarks](https://dwc.tdwg.org/terms/#dwc:identificationRemarks)       |                                              |
| sourceIdentifier          | varchar(45)      |                                                                                      | identifier for reference                     |
| sortsequence              | int(10) unsigned |                                                                                      | internal usage                               |

## Taxon table

| column_name       | column_type          | dwc_definition                                                                       | symbiota_def                                                                              |
| ----------------- | -------------------- | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| TID               | int(10) unsigned     |                                                                                      | internal id for taxon                                                                     |
| kingdomName       | varchar(45)          | [kingdom](https://dwc.tdwg.org/terms/#dwc:kingdom)                                   |                                                                                           |
| RankId            | smallint(5) unsigned |                                                                                      | internal id for taxon rank                                                                |
| SciName           | varchar(250)         |                                                                                      | full scientific name, with or without author                                              |
| UnitInd1          | varchar(1)           |                                                                                      | partial scientific name, normally for complex taxa (hybrids, varieties)                   |
| UnitName1         | varchar(50)          |                                                                                      | partial scientific rank, normally for complex taxa (hybrids, varieties)                   |
| UnitInd2          | varchar(1)           |                                                                                      | partial scientific name, normally for complex taxa (hybrids, varieties)                   |
| UnitName2         | varchar(50)          |                                                                                      | partial scientific rank, normally for complex taxa (hybrids, varieties)                   |
| UnitInd3          | varchar(7)           |                                                                                      | partial scientific name, normally for complex taxa (hybrids, varieties)                   |
| UnitName3         | varchar(35)          |                                                                                      | partial scientific rank, normally for complex taxa (hybrids, varieties)                   |
| Author            | varchar(100)         | [scientificNameAuthorship](https://dwc.tdwg.org/terms/#dwc:scientificNameAuthorship) |                                                                                           |
| PhyloSortSequence | tinyint(3) unsigned  |                                                                                      | internal usage                                                                            |
| Status            | varchar(50)          | [taxonomicStatus](https://dwc.tdwg.org/terms/#dwc:taxonomicStatus)                   |                                                                                           |
| Source            | varchar(500)         | [identificationReferences](https://dwc.tdwg.org/terms/#dwc:identificationReferences) |                                                                                           |
| Notes             | varchar(250)         | [identificationRemarks](https://dwc.tdwg.org/terms/#dwc:identificationRemarks)       |                                                                                           |
| Hybrid            | varchar(50)          |                                                                                      | internal usage                                                                            |
| SecurityStatus    | int(10) unsigned     |                                                                                      | internal usage, indicates whether taxon is protected and should not be displayed publicly |

## Published Darwin Core Archive and search results

The DwCA packages published for each collection, as well as the dataset available for download when performing a search, contain the taxonomic information and determination history, when available, for each occurrence listed.
