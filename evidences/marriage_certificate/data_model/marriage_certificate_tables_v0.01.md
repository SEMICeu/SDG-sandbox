# Marriage certificate

## Entities

### Marriage Certificate
**Definition**: Official document proving the marriage of a Person. 

|     attribute            |     expected type          |     definition                                                                        |     cardinality    |
|--------------------------|----------------------------|---------------------------------------------------------------------------------------|--------------------|
|     identifier           |     Identifier             |     An unambiguous reference to the Marriage Certificate.                             |     [1..1]         |
|     issuing date         |     date                   |     The date on which the Marriage Certificate was issued.                            |     [1..1]         |
|     certifies            |     Marriage               |     Attesting in a formal way that the Marriage is true.                              |     [1..1]         |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Marriage Certificate.              |     [1..1]         |
|     issuing place        |     Location               |     The Location where the Marriage Certificate was issued.                           |     [1..1]         |


### Marriage
**Definition**: A legally accepted relationship between two people in which they live together

|     attribute       |     expected type |     definition                                            |     cardinality    |
|------------------   |-------------------|-----------------------------------------------------------|--------------------|
|     marriage date    |     date        |     The date on which the marriage took place              |     [1..1]         |

### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.
|     attribute                            |     expected type     |     definition       |     cardinality     |
|-----------------------------------------|---------------|-------------------------------|---------------------|
|     given name                           |     string    |  A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                             |     [1..1]          |
|     family   name after marriage         |     string    |  This property contains the surname(s) after marriage of the Person.                 |           [1..1]          |
|     family   name before marriage        |     string    |  This property contains the surname(s) before the marriage of the erson.                            |     [1..1]          |
|     marital status   before marriage     |     String    |  The state of being either married or not married.                           |     [1..1]          |
|     capacity to marry                    |     code      | Indicates whether the Person has the legal capacity to marry under the national law        |     [1..1]          |
|     birth   date                         |     date      |  A date that specifies the birth date of a Person.	                              |     [1..1]          |
|     citizenship                          |     code      |  The citizenship relationship links a Person to a Jurisdiction that has conferred citizenship rights on the individual such as the right to vote, to receive certain protection from the community or the issuance of a passport                               |     [1..1]          |                                                                                                                                                                                                                                                                                                                                                                                 |                |     [1..1]        |


### Public Organisation
**Definition**: Any organization that is defined as being part of the public sector by a legal framework at any level.

|     attribute        |     expected type  |     definition                              |    cardinality     |
|----------------------|--------------------|---------------------------------------------|--------------------|
|     preferred label  |     string         |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organization. An organization may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                                             |    [1..*]          |
|     identifier       |     Identifier     |     Many organizations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.                            |    [1..*]          |


### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition            |     cardinality    |
|-----------------|--------------------|---------------------------|--------------------|
|     address     |     Address        |     The address property relationship associates a Location with the Address entity.                     |     [1..1]         |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute      |     expected type |     definition                    |     cardinality    |
|--------------------|-------------------|-------------------------------------------------------|------------------------|
|     post name      |     string        |     The key postal division of the address, usually the city. (INSPIRE's definition is "One or more names created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.").             |         [1..1]         |
|     adminUnitL1    |     string        |     The uppermost administrative unit for the address, almost always a country. The domain of locn:adminUnitL1 is locn:Address and the range is a literal, conceptually defined by the INSPIRE Geographical Name data type.             |     [1..1]         |