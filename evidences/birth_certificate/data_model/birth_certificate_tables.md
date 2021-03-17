# Birth Evidence

## Entities

### Birth Evidence
**Definition**: Official document or data proving the Birth of a Child.

**Source**:  [Public documents forms](https://beta.e-justice.europa.eu/35981/EN/public_documents_forms) 

|     attribute            |     expected type          |     definition                                                                                |     cardinality    | code list | 
|--------------------------|----------------------------|-----------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier           |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)            |     An unambiguous reference to the Birth Evidence.                                           |     [0..1]         |    N/A    |
|     issuing date         |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)  |     The date on which the Birth Evidence was issued.                                          |     [1..1]         |    N/A    | 
|     certifies birth           |     [Birth](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#birth)                  |     Attesting in a formal way that the Birth is true.                                         |     [1..1]         |    N/A    | 
|     issuing authority    |     [Public Organisation](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#public-organisation)     |     A Public Organisation with official authority in charge of issuing the Birth Evidence.    |     [1..1]         |    N/A    |
|     issuing place        |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#location)              |     The Location where the Birth Evidence was issued.                                         |     [0..1]         |    N/A    | 


### Birth
**Definition**: The event indicating the moment a Child emerges from the body of another Person, i.e. start of life.

**Source**:  [Public documents forms](https://beta.e-justice.europa.eu/35981/EN/public_documents_forms) 

|     attribute    |     expected type |     definition                                            |     cardinality    | code list | 
|------------------|-------------------|-----------------------------------------------------------|--------------------|-----------|
|     child        |     [Child](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#child)        |     The Person who is born at the Birth.                  |     [1..1]         |    N/A    | 
|     parent       |     [Parent](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#parent)        |     The Parent of the Child.                              |     [0..2]         |    N/A    | 

### Child
**Definition**: A Person of any age, who is a son or daughter.

**Subclass of**: Person

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person) 

|     attribute           |     expected type |     definition          |     cardinality   |    code list  | 
|-------------------------|-------------------|-------------------------|-------------------|--------------------|
|     date of birth       |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)          |     The day on which the Child was born.        |     [1..1]        |    N/A     | 
|     place of birth      |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#location)      |     The Location where the Child was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [1..1]        |    N/A       | 
|     sex                 |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)          |     The chromosomal state, and reproductive organs and structures of a Person that allows them to be distinguished as female or male.                                                                                                                                                                                                                                                                                                        |     [1..1]        |    [Human Sex](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/human-sex/?target=Browse&uri=http://publications.europa.eu/resource/authority/human-sex) | 

### Parent
**Definition**: One of the two Persons who are jointly the cause of the Child's Birth, i.e. natural parent.

**Subclass of**: Person

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person) 

|     attribute           |     expected type |     definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality   |    code list                                                                                                                                                                               |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     date of birth       |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)          |     The day on which the Parent was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [0..1]        |    N/A                                                                                                                                                                                     | 
|     sex                 |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)          |     The chromosomal state, and reproductive organs and structures of a Person that allows them to be distinguished as female or male.                                                                                                                                                                                                                                                                                                        |     [0..1]        |    [Human Sex](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/human-sex/?target=Browse&uri=http://publications.europa.eu/resource/authority/human-sex) | 
|     place of birth      |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#location)      |     The Location where the Parent was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [0..1]        |    N/A                                                                                                                                                                                     |


### Person
**Definition**: An individual natural person who may be dead or alive, but not imaginary.

**Source**:[ISA² Core Person Vocabulary](https://www.w3.org/ns/person)  

|     attribute           |     expected type |     definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality   |    code list                                                                                                                                                                               |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     identifier          |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)    |     The identifier relation is used to link a Person to any formally issued Identifier for that Person.                   |     [0..*]        |    N/A                     |                   
|     given name          |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johann Sebastian Bach is “Johann Sebastian”.                                                               |     [1..*]        |    N/A      |  
|     family name         |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".     |     [1..*]        |    N/A |  
|     citizenship         |     [Jurisdiction](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables.md#jurisdiction)  |     The citizenship relationship links a Person to a Jurisdiction that has conferred citizenship rights on the individual such as the right to vote, to receive certain protection from the community or the issuance of a passport. Multiple citizenships are recorded as multiple instances of the citizenship relationship.                                                                                                               |     [0..*]        |    N/A  | 



### Jurisdiction 
**Definition**: The authority that an official organisation has, to make legal decisions about somebody/something. 

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person) 

|     attribute   |     expected type  |     definition                                                                                                          |     cardinality    |  code list                                                                                                                                                                         | 
|-----------------|--------------------|-------------------------------------------------------------------------------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    name         |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |    The name is simply a string that identifies the Jurisdiction, typically a country, with or without a language tag.   |     [1..*]         |  N/A | 
|    id           |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)            |    The value for the id property is a URI for that Jurisdiction.                                                        |     [0..1]         |  [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country) *Addition of stateless concept needed*|


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
|     geographic name        |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.  |     [0..*]         |   N/A | 
|     geographic identifier  |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)            |     A URI that identifies the Location.                                                                                                                                                                                                                        |     [0..1]         |  [GeoNames](https://www.geonames.org/)    | 
