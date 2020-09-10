# Disclaimer

This page relates to this version [version (v0.11)](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/vehicle_registration_certificate/data_model/vehicle_registration_certificate_diagram_v0.11.pdf) of the model.

---

# Vehicle Registration Evidence

## Entities

### Vehicle Registration Evidence
**Definition**: Official document proving the registration of a Vehicle. 

|     attribute            |     expected type          |     definition                                                                                                 |     cardinality    | code list      |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------|--------------------|----------------|
|     registration number  |     Identifier             |     An unambiguous reference to the Vehicle Registration Evidence.                                             |     [1..1]         | N/A            |
|     validity period      |     Period                 |     The period during which the Vehicle Registration Evidence is valid.                                        |     [1..1]         | N/A            |
|     registration date    |     Date                   |     The date on which the Vehicle was registered.                                                              |     [1..1]         | N/A            |
|     certifies            |     Vehicle                |     The Vehicle that is the subject of the Evidence.                                                           |     [1..1]         | N/A            |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Vehicle Registration Evidence.      |     [1..1]         | N/A            |
|     vehicle owner        |     Agent                  |     The owner of the Vehicle.                                                                                  |     [0..1]         | N/A            |
|     vehicle legal user   |     Agent                  |     The legal user of the Vehicle.                                                                             |     [0..*]         | N/A            |
|     holder               |     Agent                  |     The holder of the Vehicle Registration Evidence.                                                           |     [1..1]         | N/A            |


### Vehicle
**Definition**: A machine, usually with wheels and an engine, used for transporting people or goods on land, especially on roads.

|     attribute                                    |     expected type |     definition                                             																								         |     cardinality    | code list |
|--------------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identification number                        |     Identifier    |     Vehicle identification number (VIN). 																									                         |     [1..1]         | N/A       |
|     first registration date                      |     Date          |     First registration date of the Vehicle.                        															                    		         |     [1..1]         | N/A       |
|     make                                         |     String        |     The make of the Vehicle.                                      																				               		 |     [1..1]         | N/A       |
|     type                                         |     String        |     The type of the Vehicle.                                              																				             |     [1..1]         | N/A       |
|     type variant                                 |     String        |     The type variant of the Vehicle.                                        																		                 |     [0..1]         | N/A       |
|     type version                                 |     String        |     The type version of the Vehicle.                                       																		                 |     [0..1]         | N/A       |
|     commercial description                       |     String        |     The commercial description of the Vehicle.                                            																		     |     [1..*]         | N/A       |
|     maximum technically permissable laden mass   |     Number        |     The maximum technically permissable laden mass of the Vehicle (in kg).                          										                         |     [0..1]         | N/A       |
|     actual mass                                  |     Number        |     The mass of the vehicle in service with bodywork, and with coupling device in the case of a towing vehicle in service from any category other than M1 (in kg).  |     [1..1]         | N/A       |
|     type approval number                         |     String        |     The type-approval number.                                                  																				     |     [0..1]         | N/A       |      
|     engine capacity                              |     Number        |     The engine capacity (in cm3).                                            																			             |     [0..1]         | N/A       |
|     engine maximum net power                     |     Number        |     The engine maximum net power (in kW).                                    																		                 |     [0..1]         | N/A       |
|     fuel type or power source                    |     Code          |     The type of fuel or power source.                                          																		             |     [1..1]         | N/A       |
|     power to weight ratio                        |     Number        |     The power to weight ratio (in kW/kg). (Only for motorcycles.)             												                                         |     [0..1]         | N/A       |
|     seats                                        |     Number        |     The number of seats, including the drivers seat.                          															                             |     [1..1]         | N/A       |
|     standing places                              |     Number        |     The number of standing places (where appropriate).                          														                             |     [0..1]         | N/A       |


### Agent
**Definition**: Any entity that is able to carry out actions.

|     attribute                         |     expected type |     definition                                                                                                       |     cardinality   | code list |
|---------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier                        |     Identifier    |     The identifier relation is used to link an Agent to any formally issued Identifier for that Agent.               |     [1..*]        | N/A       |
|     registered location               |     Location      |     The registered Location of the Agent.                                                                            |     [1..1]        | N/A       |                     


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

**Subclass of**: Agent

|     attribute           |     expected type |     definition  																																																																																																				             |     cardinality   | code list  |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|------------|
|     given name          |     Text          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                               |     [1..1]        | N/A        |
|     family name         |     Text          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family nme field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".      |     [1..1]        | N/A        |


### Organisation
**Definition**: Represents a collection of people organised together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it and can act as an Agent. Organisations are often decomposable into hierarchical structures.

**Subclass of**: Agent

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label  |     Text         |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                              |    [1..*]          | N/A       |


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

**Subclass of**: Organisation


### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition                                                                                  |     cardinality    | code list |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------|--------------------|-----------|
|     address     |     Address        |     The address property relationship associates a Location with the Address entity.            |     [1..1]         | N/A       |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute           |     expected type |     definition                                                                    |     cardinality    | code list |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------|-----------|
|     full address        |     Text          |     The complete address written as a string, with or without formatting.         |     [1..1]         | N/A       |

