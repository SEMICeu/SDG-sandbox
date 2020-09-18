# Disclaimer

This page relates to this [version (v0.01)](extract_of_criminal_records_evidence_diagram_v0.01.png) of the model.

---


# Extract of Criminal Records Evidence

## Entities

### Extract of Criminal Records Evidence
**Definition**: Official document containing the criminal Offences of a Person. 

|     attribute            |     expected type          |     definition                                                                                                   |     cardinality    | code list |
|--------------------------|----------------------------|------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     criminal record      |     Boolean                |     An indicator that declares the (non)existence of a criminal record for a Person.                             |     [1..1]         | N/A       |
|     identifier           |     Identifier             |     An unambiguous reference to the Extract of Criminal Records Evidence.                                        |     [1..1]         | N/A       | 
|     issuing date         |     Date                   |     The date on which the Extract of Criminal Records Evidence was issued.                                       |     [1..1]         | N/A       |
|     belongs to           |     Person                 |     The Person to whom the Extract of Criminal Records applies.                                                  |     [1..1]         | N/A       |
|     issuing authority    |     Public Organisation    |     A Public Organisation with official authority in charge of issuing the Extract of Criminal Records Evidence. |     [1..1]         | N/A       |
|     contains  		   |     Offence                |     The Offence that is the subject of the criminal records.                                                     |     [0..*]         | N/A       |


### Offence
**Definition**: An infraction of law that is punishable by a state or other authority.

|     attribute              |  expected type |     definition                                                                                  |     cardinality    | code list																																		    |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|     level of completion    |  Code          |     The level at which the Offence was completed, e.g. completed or attempt.                    |     [0..1]         | See Annex A of the Council Decision 2009/316/JHA of 6 April 2009 on the establishment of the European Criminal Records Information System (ECRIS).   |
|     level of participation |  Code          |     The level at which the Persons has participated in the Offence, e.g. perpetrator or aider.  |     [0..1]         | See Annex A of the Council Decision 2009/316/JHA of 6 April 2009 on the establishment of the European Criminal Records Information System (ECRIS).   |
|     offence category       |  Code          |     A classification of the Offence.                                                            |     [1..1]         | See Annex A of the Council Decision 2009/316/JHA of 6 April 2009 on the establishment of the European Criminal Records Information System (ECRIS).   |
|     penalty category       |  Code          |     A classification of the received penalty for the Offence.                                   |     [1..1]         | See Annex B of the Council Decision 2009/316/JHA of 6 April 2009 on the establishment of the European Criminal Records Information System (ECRIS).   |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute                            |     expected type               |  definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality     | code list |
|------------------------------------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-----------| 
|     identifier                           |     Identifier                  |  The identifier relation is used to link a Person to any formally issued Identifier for that Person.                                                                                                                                                                                                                                                                                                                                      |     [1..*]          | N/A       |
|     given name                           |     Text                        |  A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is 'Johan Sebastian'.                                                               |     [1..1]          | N/A       |
|     family name                          |     Text                        |  A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. "de Boer", "van de Putte", "von und zu Orlow". Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".     |     [1..1]          | N/A       |
|     date of birth                        |     Date                        |  A date that specifies the birth date of a Person.	                                                                                                                                                                                                                                                                                                                                                                                     |     [1..1]          | N/A       |
|     place of birth                       |     Location                    |  The Location where a Person was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [0..1]          | N/A       |


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

|     attribute           |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|-------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label     |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          | N/A       |
|     identifier          |     Identifier     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [1..*]          | N/A       |
|     registered location |     Location       |     The registered location of the Public Organisation.   																																																																																       |    [0..1]          | N/A       |


### Location
**Definition**: A spatial region or named place.

|     attribute              |     expected type  |     definition                                                                        																																								            |     cardinality    | code list |
|----------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     geographic name        |     Text           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.   |     [1..1]         | N/A       | 
|     geographic identifier  |     URI            |     A URI that identifies the location.                                                                                                                                                                     												    |     [1..1]         | N/A       |

