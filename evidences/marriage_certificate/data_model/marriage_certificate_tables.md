# Disclaimer

This page relates to [version (v0.14)](marriage_certificate_diagram_v0.14.png) of the model.

---

# Marriage Evidence

## Entities

### Marriage Evidence
**Definition**: Official document or data proving the Marriage of two Persons.

**Source**:  [Public documents forms](https://beta.e-justice.europa.eu/35981/EN/public_documents_forms) 

|     attribute            |     expected type          |     definition                                                                                        |     cardinality    | code list | 
|--------------------------|----------------------------|-------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier           |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)             |     An unambiguous reference to the Marriage Evidence.                                                |     [0..1]         | N/A       | 
|     issuing date         |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)                   |     The date on which the Marriage Evidence was issued.                                               |     [1..1]         | N/A       | 
|     certifies marriage            |     [Marriage](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#marriage)               |     Attesting in a formal way that the Marriage is true.                                              |     [1..1]         | N/A       | 
|     issuing authority    |     [Public Organisation](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#public-organisation)    |     A Public Organisation with official authority in charge of issuing the Marriage Evidence.         |     [1..1]         | N/A       | 
|     issuing place        |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#location)               |     The Location where the Marriage Evidence was issued.                                              |     [0..1]         | N/A       | 

### Marriage
**Definition**: A legally accepted relationship between two Persons in which they live together.

**Source**:  [Public documents forms](https://beta.e-justice.europa.eu/35981/EN/public_documents_forms) 

|     attribute          |     expected type |     definition                                            |     cardinality    | code list |
|------------------------|-------------------|-----------------------------------------------------------|--------------------|-----------|
|     marriage date      |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)          |     The date on which the Marriage took place.            |     [1..1]         | N/A       | 
|     place of marriage  |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#location)      |     The Location where the Marriage took place.           |     [0..1]         | N/A       | 
|     spouse             |     [Married Person](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#married-person)        |     The Person who was married.                          |     [2..2]         | N/A       | 


### Married Person
**Definition**: A Person who has entered into a Marriage.

**Source**:  [Public documents forms](https://beta.e-justice.europa.eu/35981/EN/public_documents_forms) 

**Subclass of**: Person

|     attribute                            |     expected type     |  definition                                                                                     |     cardinality     | code list                                                                                        | 
|------------------------------------------|-----------------------|-------------------------------------------------------------------------------------------------|---------------------|--------------------------------------------------------------------------------------------------|
|     family name after marriage           |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)             |  This property contains the family name after the Marriage of the Person.                       |     [0..1]          | N/A  |  
|     family name before marriage          |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)              |  This property contains the family name before the Marriage of the Person.                      |     [0..1]          | N/A       | 
|     marital status before marriage       |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)              |  Situation with regard to whether a Person was single, married, separated, divorced or widowed.  |     [0..1]          | [Marital Status](https://op.europa.eu/en/web/eu-vocabularies/th-concept/-/resource/eurovoc/4184) *Discussion ongoing to add terms to the code list* | 

### Person
**Definition**: An individual natural person who may be dead or alive, but not imaginary.

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person) 

|     attribute                            |     expected type               |  definition             |     cardinality     | code list | 
|------------------------------------------|---------------------------------|------------------------|---------------------|-------|
|     given name                           |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                        |  A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johann Sebastian Bach is 'Johann Sebastian'.                                                               |     [1..*]          | N/A       | 
|     family name                          |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                        |  A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. "de Boer", "van de Putte", "von und zu Orlow". Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..*]          | N/A       | 
|     date of birth                        |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)                        |  The day on which the Person was born.        	                                                                                                                                                                                                                                                                                                                                                                                         |     [0..1]          | N/A       |
|     identifier                           |    [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)                  |  The identifier relation is used to link a Person to any formally issued Identifier for that Person.                                                                                                                                                                                                                                                                                                                                      |     [0..*]          | N/A       | 
|     place of birth                       |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#location)                    |  The Location where the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                  |     [0..1]          | N/A       | 
|     citizenship                          |     [Jurisdiction](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_tables_v0.02.md#jurisdiction)                |  The citizenship relationship links a Person to a Jurisdiction that has conferred citizenship rights on the individual such as the right to vote, to receive certain protection from the community or the issuance of a passport.                                                                                                                                                                                                         |     [0..*]          | N/A       | 

### Jurisdiction 
**Definition**: The authority that an official organisation has, to make legal decisions about somebody/something. 

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person) 

|     attribute   |     expected type  |     definition                                                                                                          |     cardinality    |  code list                                                                                                                                                                         | 
|-----------------|--------------------|-------------------------------------------------------------------------------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    name         |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |    The name is simply a string that identifies the Jurisdiction, typically a country, with or without a language tag.   |     [1..*]         |  [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country) *Addition of stateless concept needed* | 
|    id           |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)            |    The value for the id property is a URI for that Jurisdiction.                                                        |     [0..1]         |  [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country) *Addition of stateless concept needed* | 


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

**Source**: [ISA² Core Public Organisation Vocabulary](https://joinup.ec.europa.eu/release/core-public-organisation-vocabulary-v100)

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                       |    cardinality     |   code list   | 
|----------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
|     preferred label  |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                                   |    [1..*]          |   N/A         | 
|     identifier       |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.               |    [0..*]          |   N/A         | 

### Location
**Definition**: An identifiable geographic place or named place.

**Source**: [ISA² Core Location Vocabulary](https://www.w3.org/ns/locn)

_Given that both attributes are optional, at least one of the attributes must be provided._

|     attribute              |     expected type  |     definition                                                                                                                                                                                                                                                 |     cardinality    |  code list                                                                                                                                                                       | 
|----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     geographic name        |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.  |     [0..*]         |   N/A   | 
|     geographic identifier  |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)            |     A URI that identifies the Location.                                                                                                                                                                                                                        |     [0..1]         |  [GeoNames](https://www.geonames.org/)     | 

