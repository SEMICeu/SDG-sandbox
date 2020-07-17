# Certificate of completion of secondary education

## Entities

### Secondary Education Completion Certificate
**Definition**: Official document proving the Secondary Education Completion of a Person. 

|     attribute            |     expected type          |     definition                                                                                								|     cardinality    |
|--------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------|--------------------|
|     identifier           |     Identifier             |     An unambiguous reference to the Secondary Education Completion Certificate.  								                |     [1..1]         |
|     overall grade        |     float                  |     A mark indicating a degree of accomplishment for the whole year.        								      	            |     [1..1]         |
|     issuing authority    |     Issuing Authority      |     The Organisation that issued the Secondary Education Completion Certificate.                                              |     [1..1]         |
|     contains	           |     Course Result          |     The Course Results which the Seconduary Education Completion Certificate contains.             							|     [0..*]         |
|     belongs to           |     Student			    |     The Student to which the certificate belongs.          															     	|     [1..1]         |
 

### Course Result 
**Definition**: Grade obtained after after finishing/completing a course. 

|     attribute    	|     expected type				   |     definition                                          			 											  |     cardinality    |
|-------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------|
|     obtained at   |     Education Institution        |     The Education Institution that organized the course.               				                          |     [1..1]         |
|     course name   |     string       			       |     Name given to a number of lectures or other matter dealing with a subject.              					  |     [1..1]         |
|     course grade  |     float          		       |     A mark indicating a degree of accomplishment for a particular course.                            			  |     [1..1]         |


### Issuing Authority 
**Definition**: An Organisation with official authority in charge of issuing Secondary Education Completion Certificates.

**Subclass of**: Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from its superclass, Organisation.*


### Education Institution
**Definition**: An Orgnanisation that provides instructional services to individuals or education-related services to individuals and other educational institutions.

**Subclass of**: Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from its superclass, Organisation.*


### Organization
**Definition**: Represents a collection of people organized together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it.

|     attribute   		  |     expected type  		|     definition                                                                                  																																																																									  |     cardinality    |
|-------------------------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|    identifier           |     Identifier     		|     Many organizations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.              |    [1..*]          |
|    name 			      |     string        		|     A word or combination of words by which the Organisation is designated, called or known.         		                                                                                                                                                                                                                                                                                          |     [1..1]         |

### Student
**Definition**: A Person who attended school.

|     attribute   				 |     expected type  		|     definition                                                                                  	|     cardinality    |
|--------------------------------|--------------------------|---------------------------------------------------------------------------------------------------|--------------------|
|     student ID number 		 |     Identifier        	|     An unambiguous reference to the Student.										        		|     [1..1]         |

### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute           |     expected type |     definition       											 																																																																																												|     cardinality   |
|-------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
|     identifier          |     Identifier    |     The identifier relation is used to link a person to any formally issued Identifier for that person.     																																																																																	|     [1..*]        |
|     given name          |     string        |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                                  |     [1..1]        |
|     family name         |     string        |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the Family Name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single Family Name field so that, for example, Miguel de Cervantes Saavedra's Family Name would be recorded as "de Cervantes Saavedra".        |     [1..1]        |
|     date of birth       |     date          |     A date that specifies the birth date of a person.                                                                                                                                                                                                                                                                                                                                                                                           |     [1..1]        |
|     place of birth      |     Location      |     The Location where a Person was born.                                                                                                                                                                                                                                                                                                                                                                                                       |     [0..1]        |

### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition                                                                                   |     cardinality    |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------|--------------------|
|     address     |     Address        |     The address property relationship associates a Location with the Address entity.             |     [1..1]         |

### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute             |     expected type |     definition                                                                                                                                                  																	  |     cardinality    |
|---------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|     post name             |     string        |     The key postal division of the address, usually the city. (INSPIRE's definition is "One or more names created and maintained for postal purposes to identify a subdivision of addresses and postal delivery points.").          |     [1..1]         |
|     admin unit level 1    |     string        |     The uppermost administrative unit for the address, almost always a country. The domain of locn:adminUnitL1 is locn:Address and the range is a literal, conceptually defined by the INSPIRE Geographical Name data type.         |     [1..1]         |
