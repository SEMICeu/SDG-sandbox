# Disclaimer

This page relates to version [version (v0.13)](vehicle_registration_certificate_diagram_v0.13.png) of the model.

---

# Vehicle Registration Evidence

## Entities

### Vehicle Registration Evidence
**Definition**: Official document proving the registration of a Vehicle. 

|     attribute               |     expected type          |     definition                                                                                                                                                                      |     cardinality    | code list                                                                            |
|-----------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------|
|     registration number     |     Identifier             |     A numeric or alphanumeric identifier that uniquely identifies the Vehicle (or vehicle owner) within the isssuing region's vehicle register. Also known as license/number plate. |     [1..1]         | N/A                                                                                  |
|     status                  |     Code                   |     Actual status of the vehicle registration.                                            																							 |     [0..1]         | [Issue #16](https://github.com/SEMICeu/SDG-sandbox/issues/16#issuecomment-674108962) |  
|     first registration date |     Date                   |     Date of first registration of the Vehicle (somewhere in the world).																											 |     [0..1]         | N/A                                                                                  |
|     start registration date |     Date                   |     Start date of registration of the Vehicle in the Member State.        																											 |     [1..1]         | N/A                                                                                  |
|     end registration date   |     Date                   |     End date of registration of the Vehicle in the Member State. (Is populated if the vehicle has been de-registered in the Member State.)    										 |     [0..1]         | N/A                                                                                  |
|     certifies               |     Vehicle                |     The Vehicle that is the subject of the Vehicle Registration Evidence.                                                                                                           |     [1..1]         | N/A                                                                                  |
|     issuing authority       |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Vehicle Registration Evidence.                                                                           |     [1..1]         | N/A                                                                                  |
|     vehicle owner           |     Agent                  |     The natural person or legal person that is the legal owner of the vehicle (i.e. the entity that has bought the vehicle, and has the right to sell it).                          |     [0..1]         | N/A                                                                                  |
|     vehicle legal user      |     Agent                  |     The natural person or legal person that has the legal right to use the Vehicle.                                                                                                 |     [0..*]         | N/A                                                                                  |
|     holder                  |     Agent                  |     The natural person or legal person in whose name the vehicle is registered.                                                                                                     |     [0..1]         | N/A                                                                                  |


### Vehicle
**Definition**: A machine, usually with wheels and an engine, used for transporting people or goods on land, especially on roads.

|     attribute                                    |     expected type        |     definition                                             																								            |     cardinality    | code list                                         |
|--------------------------------------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------------------------------------------|
|     identification number                        |     Identifier           |     Vehicle identification number (VIN). 																									                        |     [1..1]         | N/A                                               |
|     make                                         |     Text               |     The make of the Vehicle, e.g. Ford, Opel, Renault, etc.                                    																	    |     [1..1]         | N/A                                               |
|     type                                         |     Text               |     The type of the Vehicle as described in B. of Annex II of 2007/46/EC.                                              											    |     [1..1]         | N/A                                               |
|     type variant                                 |     Text               |     The type variant of the Vehicle as described in B. of Annex II of 2007/46/EC.                                        											|     [0..1]         | N/A                                               |
|     type version                                 |     Text               |     The type version of the Vehicle as described in B. of Annex II of 2007/46/EC.                                       											|     [0..1]         | N/A                                               |
|     commercial name                              |     Text               |     The commercial name of the Vehicle, e.g. Focus, Astra, Megane.                                            														|     [1..*]         | N/A                                               |
|     maximum technically permissable laden mass   |     Number               |     The maximum technically permissable laden mass of the Vehicle (in kg).                          										                        |     [0..1]         | N/A                                               |
|     actual mass                                  |     Number               |     The mass of the vehicle in service with bodywork, and with coupling device in the case of a towing vehicle in service from any category other than M1 (in kg).  |     [1..1]         | N/A                                               |
|     type approval number                         |     Text               |     The type-approval number.                                                  																				        |     [0..1]         | N/A                                               |      
|     engine capacity                              |     Number               |     The engine capacity (in cm3).                                            																			            |     [0..1]         | N/A                                               |
|     engine maximum net power                     |     Number               |     The engine maximum net power (in kW).                                    																		                |     [0..1]         | N/A                                               |
|     fuel type or power source                    |     Code                 |     The type of fuel or power source.                                          																		                |     [1..1]         | TBD                                               |
|     power to weight ratio                        |     Number               |     The power to weight ratio (in kW/kg). (Only for motorcycles.)             												                                        |     [0..1]         | N/A                                               |
|     seats                                        |     Number               |     The number of seats, including the drivers seat.                          															                            |     [1..1]         | N/A                                               |
|     standing places                              |     Number               |     The number of standing places (where appropriate).                          														                            |     [0..1]         | N/A                                               |
|     environmental category 					   |     Code                 |     Indication of the environmental category of EC type-approval.                                                                                                   |     [0..1]         | Directive 70/220/EEC(2) or Directive 88/77/EEC(3) |
|     CO2										   |     Float                |     Exhaust emissions of carbon dioxide (in g/km).                                                                                                                  |     [0..1]         | N/A                                               |
|     CO										   |     Float                |     Exhaust emissions of carbon monoxide (in g/km).                                                                                                                 |     [0..1]         | N/A                                               |
|     HC										   |     Float                |     Exhaust emissions of hydrocarbon (in g/km).                                                                                                                     |     [0..1]         | N/A                                               |
|     NOx	        							   |     Float                |     Exhaust emissions of nitrogen oxides (in g/km).                                                                                                                 |     [0..1]         | N/A                                               |
|     HC + NOx		    						   |     Float                |     Exhaust emissions of hydrocarbon and nitrogen oxides (in g/km).                                                                                                 |     [0..1]         | N/A                                               |
|     undergoes		    						   |     Technical Inspection |     The last Technical Inspection the Vehicle underwent.                                                                                                            |     [0..1]         | N/A                                               |


### Technical Inspection
**Definition**: The event when a Vehicle's compliance to the technical and legal specifications is verified.

|   attribute              |     expected type |     definition  														                                                                                      |     cardinality   | code list  |
|--------------------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|------------|
|   last inspection date   |     Date          |     The last date on which the Vehicle underwent a Technical Inspection.                                                                                     |     [1..1]        | N/A        |
|   validity period        |     Period        |     The Period during which the Vehicle is deemed technically safe to drive on public roads and after which it needs to be inspected again.                  |     [1..1]        | N/A        |


### Agent
**Definition**: Any entity that is able to carry out actions.

|     attribute                         |     expected type |     definition                                                                                                       |     cardinality   | code list |
|---------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier                        |     Identifier    |     The identifier relation is used to link an Agent to any formally issued Identifier for that Agent.               |     [0..*]        | N/A       |
|     registered location               |     Location      |     The registered Location of the Agent.                                                                            |     [0..1]        | N/A       |                     


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

**Subclass of**: Agent

|     attribute           |     expected type |     definition  																																																																																																				             |     cardinality   | code list  |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|------------|
|     given name          |     Text          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                               |     [1..1]        | N/A        |
|     family name         |     Text          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family nme field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".      |     [1..1]        | N/A        |
|     date of birth       |     Date          |     The day on which the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [0..1]        | N/A        |
|     place of birth      |     Location      |     The Location where the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                  |     [0..1]        | N/A        |


### Organisation
**Definition**: Represents a collection of people organised together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it and can act as an Agent. Organisations are often decomposable into hierarchical structures.

**Subclass of**: Agent

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label  |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          | N/A       |


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

**Subclass of**: Organisation

|     attribute                         |     expected type |     definition                                                                                                                             |     cardinality   | code list |
|---------------------------------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier                        |     Identifier    |     The identifier relation is used to link a Public Organisation to any formally issued Identifier for that Public Organisation.          |     [1..*]        | N/A       |


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

