# Disclaimer

This page relates to this [version (v0.12)](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_diagram_v0.12.pdf) of the model.

---
# Secondary Education Completion Evidence

## Entities

### Secondary Education Completion Evidence
**Definition**: Official document proving the Secondary Education Completion of a Student. 

|     attribute               |     expected type          |     definition                                                 		                        |     cardinality    | code list |
|-----------------------------|----------------------------|------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     identifier              |     Identifier             |     An unambiguous reference to the Secondary Education Completion Evidence.                   |     [1..1]         | N/A       |
|     overall grade           |     Float                  |     A mark indicating a degree of accomplishment for the whole year (in percentage).           |     [1..1]         | N/A       |
|     school year             |     Date                   |     The annual period of sessions of the educational institution.        					    |     [0..1]         | N/A       |
|     final examination date  |     Date                   |     The date of the final assessment designed to test the qualification or knowledge acquired. |     [0..1]         | N/A       |
|     issuing date            |     Date                   |     The date on which the Secondary Education Completion Evidence was issued.                  |     [0..1]         | N/A       |
|     issuing authority       |     Issuing Authority      |     The Organisation that issued the Secondary Education Completion Evidence.                  |     [1..1]         | N/A       |
|     contains	              |     Course Result          |     The Course Results which the Secondary Education Completion Evidence contains.  	        |     [0..*]         | N/A       |
|     belongs to              |     Student			       |     The Student to which the evidence belongs.                                                	|     [1..1]         | N/A       |
|     obtained at             |     Education Institution  |     The Education Institution that delivered the evidence.               				        |     [0..1]         | N/A       |
 

### Course Result 
**Definition**: Grade obtained after finishing/completing a course. 

|     attribute    	|     expected type				   |     definition                                          			 											  |     cardinality    | code list |
|-------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     course name   |     Text       			       |     Name given to a number of lectures or other matters dealing with a subject.              					  |     [0..1]         | N/A       |
|     course grade  |     Float          		       |     A mark indicating a degree of accomplishment for a particular course (in percentage).             			  |     [0..1]         | N/A       |
|     obtained at   |     Education Institution        |     The Education Institution that organized the course.               				                          |     [0..1]         | N/A       |


### Issuing Authority 
**Definition**: An Organisation with official authority in charge of issuing Secondary Education Completion Evidences.

**Subclass of**: Public Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from Public Organisation listed here below.* 


### Education Institution
**Definition**: An Organisation that provides instructional services to individuals or education-related services to individuals and other educational institutions.

**Subclass of**: Public Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from Public Organisation listed here below.*


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

|     attribute           |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|-------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label     |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          |  N/A      |
|     identifier          |     Identifier     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [1..*]          |  N/A      |
|     registered location |     Location       |     The registered location of the Public Organisation.   																																																																																       |    [1..1]          |  N/A      |


### Student
**Definition**: A Person who attended school.

|     attribute   				 |     expected type  		|     definition                                                                                  	|     cardinality    | code list | 
|--------------------------------|--------------------------|---------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     student ID number 		 |     Identifier        	|     An unambiguous reference to the Student.										        		|     [1..1]         | N/A       |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute           |     expected type |     definition       											 																																																																																												|     cardinality   | code list |
|-------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier          |     Identifier    |     The identifier relation is used to link a Person to any formally issued Identifier for that Person.     																																																																																	|     [1..*]        | N/A       |
|     given name          |     Text          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                                  |     [1..1]        | N/A       |
|     family name         |     Text          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".        |     [1..1]        | N/A       |
|     date of birth       |     Date          |     A date that specifies the birth date of a Person.                                                                                                                                                                                                                                                                                                                                                                                           |     [1..1]        | N/A       |


### Location
**Definition**: A spatial region or named place.

|     attribute              |     expected type  |     definition                                                                                                                                                                                                                                                 |     cardinality    |  code list                                                                                                                                                                |
|----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     geographic name        |     Text           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.  |     [1..1]         |  https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/place/?target=Browse&uri=http://publications.europa.eu/resource/authority/place       | 
|     geographic identifier  |     URI            |     A URI that identifies the Location.                                                                                                                                                                                                                        |     [1..1]         |  https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/place/?target=Browse&uri=http://publications.europa.eu/resource/authority/place       |
|     address                |     Address        |     The address property relationship associates a Location with the Address entity.                                                                                                                                                                           |     [0..1]         |  N/A                                                                                                                                                                      |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute           |     expected type |     definition                                                                                                              |     cardinality    | code list |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     admin unit level 2  |     Text          |     The region of the address, usually a county, state or other such area that typically encompasses several localities.    |     [1..1]         | N/A       |

