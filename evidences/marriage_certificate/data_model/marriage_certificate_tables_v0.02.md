# Disclaimer

This page relates to [version (v0.12)](marriage_certificate_diagram_v0.12.png) of the model.

---

# Marriage Evidence

## Entities

### Marriage Evidence
**Definition**: Official document proving the Marriage of two Persons.

|     attribute            |     expected type          |     definition                                                                                        |     cardinality    | code list |
|--------------------------|----------------------------|-------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier           |     Identifier             |     An unambiguous reference to the Marriage Evidence.                                                |     [1..1]         | N/A       | 
|     issuing date         |     Date                   |     The date on which the Marriage Evidence was issued.                                               |     [1..1]         | N/A       |
|     certifies            |     Marriage               |     Attesting in a formal way that the Marriage is true.                                              |     [1..1]         | N/A       |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Marriage Evidence.         |     [1..1]         | N/A       |
|     issuing place        |     Location               |     The Location where the Marriage Evidence was issued.                                              |     [0..1]         | N/A       |


### Marriage
**Definition**: A legally accepted relationship between two Persons in which they live together.

|     attribute          |     expected type |     definition                                            |     cardinality    | code list |
|------------------------|-------------------|-----------------------------------------------------------|--------------------|-----------|
|     marriage date      |     Date          |     The date on which the Marriage took place.            |     [1..1]         | N/A       |
|     place of marriage  |     Location      |     The Location where the Marriage took place.           |     [0..1]         | N/A       |
|     spouse             |     Person        |     The Person that was married.                          |     [2..2]         | N/A       |


### Married Person
**Definition**: A Person who has entered into a Marriage.

|     attribute                            |     expected type     |  definition                                                                                     |     cardinality     | code list                                                                                        |
|------------------------------------------|-----------------------|-------------------------------------------------------------------------------------------------|---------------------|--------------------------------------------------------------------------------------------------| 
|     family name after marriage           |     Text              |  This property contains the family name after the Marriage of the Person.                       |     [0..1]          | N/A                                                                                              |
|     family name before marriage          |     Text              |  This property contains the family name before the Marriage of the Person.                      |     [0..1]          | N/A                                                                                              |
|     marital status before marriage       |     Code              |  Situation with regard to whether a Person is single, married, separated, divorced or widowed.  |     [0..1]          | [Marital Status](https://op.europa.eu/en/web/eu-vocabularies/th-concept/-/resource/eurovoc/4184) |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute                            |     expected type               |  definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality     | code list |
|------------------------------------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-----------| 
|     identifier                           |     Identifier                  |  The identifier relation is used to link a Person to any formally issued Identifier for that Person.                                                                                                                                                                                                                                                                                                                                      |     [0..*]          | N/A       |
|     given name                           |     Text                        |  A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is 'Johan Sebastian'.                                                               |     [1..1]          | N/A       |
|     family name                          |     Text                        |  A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. "de Boer", "van de Putte", "von und zu Orlow". Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..1]          | N/A       |
|     date of birth                        |     Date                        |  The day on which the Person was born.        	                                                                                                                                                                                                                                                                                                                                                                                         |     [0..1]          | N/A       |
|     place of birth                       |     Location                    |  The Location where the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                  |     [0..1]          | N/A       |
|     citizenship                          |     Jurisdiction                |  The citizenship relationship links a Person to a Jurisdiction that has conferred citizenship rights on the individual such as the right to vote, to receive certain protection from the community or the issuance of a passport.                                                                                                                                                                                                         |     [0..*]          | N/A       |        


### Jurisdiction 
**Definition**: The authority that an official organisation has, to make legal decisions about somebody/something. 

|     attribute   |     expected type  |     definition                                                                                                          |     cardinality    | code list 																																										  |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    name         |     Text           |    The name is simply a string that identifies the Jurisdiction, typically a country, with or without a language tag.   |     [1..1]         | [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country) | 
|    id           |     URI            |    The value for the id property is a URI for that Jurisdiction.      												     |     [1..1]         | N/A 																																											  |


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label  |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          | N/A       |
|     identifier       |     Identifier     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [0..*]          | N/A       |


### Location
**Definition**: A spatial region or named place.

|     attribute              |     expected type  |     definition                                                                                                                                                                                                                                                 |     cardinality    |  code list                                                                                                                                                                       |
|----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     geographic name        |     Text           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.  |     [1..1]         |  [Place](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/place/?target=Browse&uri=http://publications.europa.eu/resource/authority/place)     | 
|     geographic identifier  |     URI            |     A URI that identifies the Location.                                                                                                                                                                                                                        |     [1..1]         |  [Place](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/place/?target=Browse&uri=http://publications.europa.eu/resource/authority/place)     |

