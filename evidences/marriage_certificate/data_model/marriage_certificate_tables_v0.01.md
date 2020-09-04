# Disclaimer

This page relates to this [version (v0.11)](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/marriage_certificate/data_model/marriage_certificate_diagram_v0.11.pdf) of the model

---


# Marriage Evidence

## Entities

### Marriage Evidence
**Definition**: Official document proving the marriage of a Person. 

|     attribute            |     expected type          |     definition                                                                                        |     cardinality    | code list |
|--------------------------|----------------------------|-------------------------------------------------------------------------------------------------------|--------------------|--------- |
|     identifier           |     Identifier             |     An unambiguous reference to the Marriage Certificate.                                             |     [1..1]         | N/A | 
|     issuing date         |     Date                   |     The date on which the Marriage Certificate was issued.                                            |     [1..1]         | N/A |
|     certifies            |     Marriage               |     Attesting in a formal way that the Marriage is true.                                              |     [1..1]         | N/A |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Marriage Certificate.      |     [1..1]         | N/A |
|     issuing place        |     Location               |     The Location where the Marriage Certificate was issued.                                           |     [0..1]         | N/A |


### Marriage
**Definition**: A legally accepted relationship between two people in which they live together.

|     attribute          |     expected type |     definition                                            |     cardinality    | code list |
|------------------------|-------------------|-----------------------------------------------------------|--------------------| ----------|
|     marriage date      |     Date          |     The date on which the marriage took place.            |     [1..1]         |N/A |
|     place of marriage  |     Location      |     The Location where the marriage took place.           |     [0..1]         |N/A |
|     spouse one         |     Person        |     One of the two Persons that got married.              |     [1..1]         |N/A |
|     spouse two         |     Person        |     The other of the two Persons that got married.        |     [1..1]         |N/A |

### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute                            |     expected type     |     definition                                                                                                                                                                                                                                                                                                                                                                 |     cardinality     | code list |
|------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-----------| 
|     identifier                           |     Identifier        |  The identifier relation is used to link a person to any formally issued Identifier for that person.                                                                                                                                                                                                                                                                           |     [1..*]          |N/A |
|     given name                           |     Text            |  A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is 'Johan Sebastian'.    |     [1..1]          |N/A |
|     family name         |     Text        |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the Family Name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single Family Name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..1]        | N/A|
|     date of birth                        |     Date              |  A date that specifies the birth date of a Person.	                                                                                                                                                                                                                                                                                                                            |     [1..1]          |N/A |
|     citizenship                          |     Jurisdiction      |  The citizenship relationship links a Person to a Jurisdiction that has conferred citizenship rights on the individual such as the right to vote, to receive certain protection from the community or the issuance of a passport.                                                                                                                                              |     [0..1]          |     N/A |        
|     additional info                          |     Additional Marriage Info      |  Additional information provided subsquently to a marriage.                                                                                                                                              |     [0..1]          |     N/A |    

### Jurisdiction 
**Definition**: The authority that an official organization has to make legal decisions about somebody/something. 

|     attribute   |     expected type  |     definition                                                                                  |     cardinality    | code list |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------|--------------------|-----------|
|    name    |     Text        |    The name is simply a string that identifies the jurisdiction, typically a country, with or without a language tag             |     [1..1]         | [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country) | 
|    id   |     URI        |    The value for the id property is a URI for that jurisdiction.          |     [1..1]         |N/A |

### Additional Marriage Info 
**Definition**: Additional information provided subsquently to a marriage.

|     attribute                            |     expected type     |     definition          |     cardinality     | code list |
|------------------------------------------|-----------------------|-------------------------|---------------------|---------------| 
|     family name after marriage           |     Text            |  This property contains the surname(s) after marriage of the Person.   |     [0..1]          | N/A |
|     family name before marriage          |     Text            |  This property contains the surname(s) before the marriage of the Person.    |     [0..1]          | N/A |
|     marital status before marriage       |     Code              |  The state of being either married or not married.     |     [0..1]          | [Marital Status](https://op.europa.eu/en/web/eu-vocabularies/th-concept/-/resource/eurovoc/4184) |
|     capacity to marry                    |     Code              |  Indicates whether the Person has the legal capacity to marry under the national law.   |     [0..1]          | N/A | 

### Public Organisation
**Definition**: Any organization that is defined as being part of the public sector by a legal framework at any level.

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------| -------|
|     preferred label  |     Text         |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organization. An organization may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          |N/A |
|     identifier       |     Identifier     |     Many organizations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [1..*]          |N/A |

### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition                                                                                  |     cardinality    | code list |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------|--------------------|-----------|
|     geographic name     |     Text        |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.              |     [1..1]         | N/A | 
|     geographic identifier     |     URI        |     A URI that identifies the location. GeoNames.org provides stable, widely recognised identifiers for more than 10 million geographical names that can be used as links to further information.            |     [1..1]         |N/A |

