# Disclaimer

This page relates to this [version (v0.01)](social_security_registration_evidence_diagram_v0.01.png) of the model.

---


# Social Security Registration Evidence

## Entities

### Social Security Registration Evidence
**Definition**: Official document proving a Person is registered for Social Security. 

|     attribute                            |     expected type          |     definition                                                                                                     |     cardinality    | code list |
|------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier                           |     Identifier             |     An unambiguous reference to the Social Security Registration Evidence.                                         |     [1..*]         | N/A       |
|     social security coverage start date  |     Date                   |     The date on which the social security coverage started.                                                        |     [1..1]         | N/A       |
|     social security coverage status      |     Code                   |     The status of the social security coverage.                                                                    |     [1..1]         | TBD       | 
|     belongs to                           |     Person			        |     The Person to which the Social Security Registration Evidence belongs.                                         |     [1..1]         | N/A       |
|     issuing authority                    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Social Security Registration Evidence.  |     [1..1]         | N/A       |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute                            |     expected type               |  definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality     | code list |
|------------------------------------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-----------| 
|     identifier                           |     Identifier                  |  The identifier relation is used to link a Person to any formally issued Identifier for that Person.                                                                                                                                                                                                                                                                                                                                      |     [1..*]          | N/A       |
|     given name                           |     Text                        |  A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is 'Johan Sebastian'.                                                               |     [1..1]          | N/A       |
|     family name                          |     Text                        |  A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. "de Boer", "van de Putte", "von und zu Orlow". Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..1]          | N/A       |
|     domicile                             |     Location                    |  A Person's fixed, permanent and principal home for legal purposes.                                                 																																																																														 |     [0..1]          | N/A       |


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label  |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          | N/A       |
|     identifier       |     Identifier     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [1..*]          | N/A       |


### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition                                                                                  |     cardinality    | code list |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------|--------------------|-----------|
|     address     |     Address        |     The address property relationship associates a Location with the Address entity.            |     [1..1]         | N/A       |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute           |     expected type |     definition                                                               |     cardinality    | code list |
|-------------------------|-------------------|------------------------------------------------------------------------------|--------------------|-----------|
|     full address        |     Text          |     The complete address written as a string, with or without formatting.    |     [1..1]         | N/A       |

