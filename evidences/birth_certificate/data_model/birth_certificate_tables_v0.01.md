# Birth certificate

## Entities

### Birth Certificate
**Definition**: Official document proving the Birth of a Person. 

|     attribute            |     expected type          |     definition                                                                                |     cardinality    |
|--------------------------|----------------------------|-----------------------------------------------------------------------------------------------|--------------------|
|     identifier           |     Identifier             |     An unambiguous reference to the Birth Certificate.                                        |     [1..1]         |
|     issuing date         |     date                   |     The date on which the Birth Certificate was issued.                                       |     [1..1]         |
|     certifies            |     Birth                  |     Attesting in a formal way that the Birth is true.                                         |     [1..1]         |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Birth Certificate. |     [1..1]         |
|     issuing place        |     Location               |     The Location where the Birth Certificate was issued.                                      |     [1..1]         |


### Birth
**Definition**: The start of life when a child emerges from the body of its parent.

|     attribute    |     expected type |     definition                                            |     cardinality    |
|------------------|-------------------|-----------------------------------------------------------|--------------------|
|     parent one    |     Person        |     The first parent of the child.                        |     [1..1]         |
|     parent two    |     Person        |     The second parent of the child.                       |     [1..1]         |
|     child        |     Person        |     The Person who is born at the Birth.                  |     [1..1]         |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute           |     expected type |     definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality   |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
|     identifier          |     Identifier    |     The identifier relation is used to link a person to any formally issued Identifier for that person.                                                                                                                                                                                                                                                                                                                                      |     [1..*]        |
|     given name          |     string        |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                               |     [1..1]        |
|     family name         |     string        |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the Family Name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single Family Name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..1]        |
|     date of birth       |     date          |     A date that specifies the birth date of a person.                                                                                                                                                                                                                                                                                                                                                                                        |     [1..1]        |
|     gender              |     Code          |     The gender of an individual should be recorded using a controlled vocabulary that is appropriate for the specific context. In some cases, the chromosomal or physical state of an individual will be more important than the gender that they express, in others the reverse will be true. What is always important is that the controlled vocabulary used to describe an individual's gender is stated explicitly.                      |     [1..1]        |
|     citizenship         |     Jurisdiction  |     The citizenship relationship links a Person to a Jurisdiction that has conferred citizenship rights on the individual such as the right to vote, to receive certain protection from the community or the issuance of a passport. Multiple citizenships are recorded as multiple instances of the citizenship relationship.                                                                                                               |     [1..*]        |
|     place of birth      |     Location      |     The Location where a Person was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [1..1]        |


### Public Organisation
**Definition**: Any organization that is defined as being part of the public sector by a legal framework at any level.

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                       |    cardinality     |
|----------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|     preferred label  |     string         |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organization. An organization may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                                   |    [1..*]          |
|     identifier       |     Identifier     |     Many organizations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.               |    [1..*]          |


### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition                                                                                  |     cardinality    |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------|--------------------|
|     address     |     Address        |     The address property relationship associates a Location with the Address entity.            |     [1..1]         |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute      |     expected type |     definition                                                                                                                                                                                                                    |     cardinality    |
|--------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|     post name      |     string        |     The key postal division of the address, usually the city. (INSPIRE's definition is "One or more names created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.").        |                                                                                                                                                                                                                                                                                            [1..1]         |
|     admin unit level 1    |     string        |     The uppermost administrative unit for the address, almost always a country. The domain of locn:adminUnitL1 is locn:Address and the range is a literal, conceptually defined by the INSPIRE Geographical Name data type.       |     [1..1]         |

