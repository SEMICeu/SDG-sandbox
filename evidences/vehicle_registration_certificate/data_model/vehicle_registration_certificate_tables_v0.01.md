# Vehicle registration certificate

## Entities

### Vehicle Registration Certificate
**Definition**: Official document proving the registration of a Vehicle. 

|     attribute            |     expected type          |     definition                                                                                                 |     cardinality    |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------|--------------------|
|     registration number  |     Identifier             |     An unambiguous reference to the Vehicle Registration Certificate.                                          |     [1..1]         |
|     certifies            |     Vehicle                |     The Vehicle that is the subject of the Certificate.                                                        |     [1..1]         |
|     validity date        |     Period                 |     The date on which the Vehicle Registration Certificate was issued.                                         |     [1..1]         |
|     registration date    |     date                   |     The date on which the Vehicle was registered.                                                              |     [1..1]         |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Vehicle Registration Certificate.   |     [1..1]         |
|     vehicle owner        |     Agent                  |     The owner of the Vehicle.                                                                                  |     [0..1]         |
|     legal user           |     Agent                  |     The legal user of the Vehicle.                                                                             |     [0..*]         |
|     holder               |     Agent                  |     The holder of the Vehicle Registration Certificate.                                                        |     [1..1]         |


### Vehicle
**Definition**: A machine, usually with wheels and an engine, used for transporting people or goods on land, especially on roads.

|     attribute                                    |     expected type |     definition                                            |     cardinality    |
|--------------------------------------------------|-------------------|-----------------------------------------------------------|--------------------|
|     identification number                        |     Identifier    |                                                           |     [1..1]         |
|     first registration date                      |     date          |                                                           |     [1..1]         |
|     make                                         |     string        |                                                           |     [1..1]         |
|     type                                         |     string        |                                                           |     [1..1]         |
|     type variant                                 |     string        |                                                           |     [1..1]         |
|     type version                                 |     string        |                                                           |     [1..1]         |
|     commercial description                       |     string        |                                                           |     [1..1]         |
|     maximum technically permissable laden mass   |     number        |                                                           |     [1..1]         |
|     actual mass                                  |     number        |                                                           |     [1..1]         |
|     type approval number                         |     string        |                                                           |     [1..1]         |
|     engine capacity                              |     number        |                                                           |     [1..1]         |
|     maximum net power                            |     number        |                                                           |     [1..1]         |
|     fuel type or power source                    |     Code          |                                                           |     [1..1]         |
|     power to weight ratio                        |     number        |                                                           |     [1..1]         |
|     seats                                        |     number        |                                                           |     [1..1]         |
|     standing places                              |     number        |                                                           |     [1..1]         |


### Agent
**Definition**: Any entity that is able to carry out actions.

|     attribute                         |     expected type |     definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality   |
|---------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------|-------------------|
|     identifier                        |     Identifier    |     The identifier relation is used to link an Agent to any formally issued Identifier for that Agent.               |     [1..*]        |
|     registered location               |     Location      |     The registered Location of the Agent.                                                                            |     [1..1]        |                          


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

**Subclass of**: Agent

|     attribute           |     expected type |     definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality   |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
|     given name          |     string        |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                               |     [1..1]        |
|     family name         |     string        |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the Family Name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single Family Name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..1]        |


### Public Organisation
**Definition**: Any Organization that is defined as being part of the public sector by a legal framework at any level.

**Subclass of**: Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from its superclass, Organisation.*


### Organisation
**Definition**: Represents a collection of people organized together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it and can act as an Agent. Organizations are often decomposable into hierarchical structures.

**Subclass of**: Agent

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     |
|----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|     preferred label  |     string         |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organization. An organization may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          |


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

