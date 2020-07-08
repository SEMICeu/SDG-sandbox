# Income tax declaration certificate

## Entities

### Income Tax Declaration Certificate
**Definition**: Official document in which a Tax Payer declares the Monetary Amount that he or she has earned and the taxes that he or she has paid in one year.

|     attribute            |     expected type          |     definition                                                                                          |     cardinality    |
|--------------------------|----------------------------|---------------------------------------------------------------------------------------------------------|--------------------|
|     identifier           |     Identifier             |     An unambiguous reference to the Income Tax Declaration Certificate.                                 |     [1..1]         |
|     issuing date         |     date                   |     The date on which the Income Tax Declaration was issued.                                            |     [1..1]         |
|     payment date         |     date                   |     The date on which the balance of the Income Tax was paid.                                           |     [1..1]         |
|     belongs to           |     Tax Payer              |     The Tax Payer to whom the Tax Declaration applies.                                                  |     [1..1]         |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Tax Declaration Certificate. |     [1..1]         |
|     total income         |     Monetary Amount        |     The total amount of income of the Tax Payer in the respective year.                                 |     [0..1]         |
|     income tax           |     Monetary Amount        |     The total amount of tax due on the earned income in the respective year.                            |     [0..1]         |


### Monetary Amount
**Definition**: A monetary value.

|     attribute            |     expected type          |     definition                                                                                          |     cardinality    |
|--------------------------|----------------------------|---------------------------------------------------------------------------------------------------------|--------------------|
|     currency             |     Code                   |     The currency in which the Monetary Amount is expressed.                                             |     [1..1]         |
|     value                |     Double                 |     The quantitative value of the Monetary Amount.                                                      |     [1..1]         |


### Tax Payer
**Definition**: The start of life when a child emerges from the body of its parent.

**Subclass of**: Person

|     attribute              |     expected type |     definition                                                          |     cardinality    |
|----------------------------|-------------------|-------------------------------------------------------------------------|--------------------|
|     nationalFiscalNumber   |     Identifier    |     An unambiguous reference to the Tax Payer.                          |     [1..1]         |
|     domicile               |     Location      |     A Person's fixed, permanent and principal home for legal purposes.  |     [0..1]         |


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

|     attribute           |     expected type |     definition                                                                                                                                                                                                                                  |     cardinality    |
|-------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|     full address        |     string        |     The complete address written as a string, with or without formatting.                                                                                                                                                                       |     [1..1]         |
|     PO box              |     string        |     The Post Office Box number.                                                                                                                                                                                                                 |     [1..1]         |
|     thoroughfare        |     string        |     An address component that represents the name of a passage or way through from one location to another. A thoroughfare is not necessarily a road, it might be a waterway or some other feature.                                             |     [1..1]         |
|     locator designator  |     string        |     A number or a sequence of characters that uniquely identifies the locator within the relevant scope(s). The full identification of the locator could include one or more locator designators.                                               |     [1..1]         |
|     locator name        |     string        |     Proper noun(s) applied to the real world entity identified by the locator. The locator name could be the name of the property or complex, of the building or part of the building, or it could be the name of a room inside a building.     |     [1..1]         |
|     address area        |     string        |     The name or names of a geographic area or locality that groups a number of addressable objects for addressing purposes, without being an administrative unit.                                                                               |     [1..1]         |
|     post name           |     string        |     The key postal division of the address, usually the city. (INSPIRE's definition is "One or more names created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.").                      |     [1..1]         |
|     admin unit level 2  |     string        |     The region of the address, usually a county, state or other such area that typically encompasses several localities.                                                                                                                        |     [1..1]         |
|     admin unit level 1  |     string        |     The uppermost administrative unit for the address, almost always a country.                                                                                                                                                                 |     [1..1]         |
|     post code           |     string        |     The post code (a.k.a postal code, zip code etc.).                                                                                                                                                                                           |     [1..1]         |
|     address ID          |     string        |     A globally unique identifier for an address.                                                                                                                                                                                                |     [1..1]         |

