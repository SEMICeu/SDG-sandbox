# Disclaimer

This page relates to [version (v0.15)](certificate_of_completion_of_secondary_education_diagram_v0.15.png) of the model.

---
# Secondary Education Completion Evidence

## Entities

### Secondary Education Completion Evidence
**Definition**: Official document or data proving that a Learner completed secondary education (ISCED 2011 level 3).



|     attribute               |     expected type          |     definition                                                 		                        |     cardinality    | code list | 
|-----------------------------|----------------------------|------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier              |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)             |     An unambiguous reference to the Secondary Education Completion Evidence.                   |     [0..1]         | N/A       | 
|     overall grade           |     [Grade](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#grade)                  |     A mark indicating a degree of accomplishment.         |     [0..1]         | N/A       | 
|     school year             |     [Period](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#period)               |     The annual period of sessions of the Education Institution.        					    |     [0..1]         | N/A       | 
|     final examination date  |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)                   |     The date of the final assessment designed to test the qualification or knowledge acquired. |     [0..1]         | N/A       | 
|     issuing date            |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)                   |     The date on which the Secondary Education Completion Evidence was issued.                  |     [0..1]         | N/A       | 
|     programme name 		  |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                   |     The programme name of the Secondary Education.											    |     [0..*]         | N/A       | 
|     issuing authority       |     [Organisation](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#organisation)    |     The Organisation that issued the Secondary Education Completion Evidence.           |     [1..*]         | N/A       | 
|     contains	              |     [Course Result](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#course-result)          |     The Course Result(s) which the Secondary Education Completion Evidence contains.  	        |     [0..*]         | N/A       | 
|     belongs to              |     [Learner](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#learner)			       |     The Learner to whom the Secondary Education Completion Evidence belongs.                 	|     [1..1]         | N/A       | 
|     obtained at             |     [Education Institution](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#education-institution)  |     The Education Institution(s) that educated the Learner.  	      							    |     [0..*]         | N/A       | 
 

### Course Result 
**Definition**: Grade obtained after finishing/completing a course, for each course the Learner attended. 

|     attribute      	|     expected type				   |     definition                                          			 											  |     cardinality    | code list | 
|-----------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     course name       |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)       			       |     Name given to a number of lectures or other matters dealing with a subject.              					  |     [0..*]         | [European Science Vocabulary](https://op.europa.eu/en/web/eu-vocabularies/at-dataset/-/resource/dataset/euroscivoc)      | 
|     course grade      |     [Grade](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#grade)          		       |     A mark indicating a degree of accomplishment for a particular course.             			  |     [0..1]         | N/A       | 
|     course language   |      [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                         |     Language in which the course was taught.               				                                      |     [0..*]         | [Language](http://publications.europa.eu/resource/authority/language)       | 
|     course id   |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)                          |     An unambiguous reference to the course.               				                                      |     [0..1]         | N/A       | 
|     obtained at       |     [Education Institution](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#education-institution)        |     The Education Institution that organised and delivered the course.               				                          |     [0..*]         | N/A       | 

### Education Institution
**Definition**: An Organisation that provides instructional services to individuals or education-related services to individuals and other educational institutions.

**Subclass of**: Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from Organisation listed here below.*


### Organisation
**Definition**: Represents a collection of people organised together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it and can act as an Agent. Organisations are often decomposable into hierarchical structures.

**Source**: [The Organization Ontology](https://www.w3.org/TR/vocab-org/)

|     attribute           |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list | 
|-------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label     |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          |  N/A      | 
|     identifier          |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [0..*]          |  N/A      | 
|     registered location |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#location)       |     The registered location of the Organisation.   																																																																																       |    [0..1]          |  N/A      | 


### Learner
**Definition**: A Person who attends a Secondary Education Institution.

|     attribute   				 |     expected type  		|     definition                                                                                  	|     cardinality    | code list | 
|--------------------------------|--------------------------|---------------------------------------------------------------------------------------------------|--------------------|-----------|
|     learner id 		 |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)        	|     An unambiguous reference to the Learner.										        		|     [0..*]         | N/A       | 


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person)

|     attribute           |     expected type |     definition       											 																																																																																												|     cardinality   | code list | 
|-------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier          |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)    |     The identifier relation is used to link a Person to any formally issued Identifier for that Person.     																																																																																	|     [0..*]        | N/A       | 
|     given name          |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johann Sebastian Bach is “Johann Sebastian”.                                                                  |     [1..*]        | N/A       | 
|     family name         |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".        |     [1..*]        | N/A       | 
|     date of birth       |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)          |     The day on which the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                       |     [0..1]        | N/A       |
|     sex                 |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)          |     The chromosomal state, and reproductive organs and structures of a Person that allows them to be distinguished as female or male.                                                                                                                                                                                                                                                                                                        |     [0..1]        |    [Human Sex](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/human-sex/?target=Browse&uri=http://publications.europa.eu/resource/authority/human-sex) | 
|     place of birth      |     [Location](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/birth_certificate/data_model/birth_certificate_tables_v0.02.md#location)      |     The Location where the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [0..1]        |    N/A                                                                                                                                                                                     | 
|     registered address  |     [Address](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#education-institution)      |     The registered address of the Person.                                                    																																																																																          			|     [0..1]        | N/A       | N/A |

#### Location
**Definition**: An identifiable geographic place or named place.

**Source**: [ISA² Core Location Vocabulary](https://www.w3.org/ns/locn)

_Given that both attributes are optional, at least one of the attributes must be provided._


|     attribute              |     expected type  |     definition                                                                                                                                                                                                                                                 |     cardinality    |  code list                                                                                                                                                                       | 
|----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     geographic name        |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.  |     [0..*]         |  N/A  | 
|     geographic identifier  |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)            |     A URI that identifies the Location.                                                                                                                                                                                                                        |     [0..1]         |  [GeoNames](https://www.geonames.org/)   | 
|     address               |     [Address](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/certificate_of_completion_of_secondary_education/data_model/certificate_of_completion_of_secondary_education_tables_v0.02.md#address)        |     The address property relationship associates a Location with the Address entity.                                                                                                                                                                               |     [0..1]         | N/A       | 

### Address
**Definition**: A spatial object that in a human readable way identifies a fixed location of a property.

**Source**: [ISA² Core Location Vocabulary](https://www.w3.org/ns/locn)

|     attribute           |     expected type |     definition                                                                                                              |     cardinality    | code list																																											   | 
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     admin unit level 1  |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)          |     The uppermost administrative unit for the address, almost always a country.                                             |     [1..1]         | [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country)       | 
|     admin unit level 2  |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     The region of the address, usually a county, state or other such area that typically encompasses several localities.    |     [0..*]         | [NUTS](http://publications.europa.eu/resource/dataset/nuts)   | [ISA² Core Location Vocabulary](https://joinup.ec.europa.eu/collection/semantic-interoperability-community-semic/solution/core-location-vocabulary/release/100) | 
|     full address        |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     The complete address written as a string, with or without formatting.                                                   |     [0..*]         | N/A                                                                                                                                                                                     | 


## Complex datatypes

### Grade
**Definition**: Mark indicating a degree of accomplishment.

|     attribute   		 |     expected type  		|     definition                                                                                               |     cardinality    | code list | 
|------------------------|--------------------------|--------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     distribution 		 |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)        	        |     Statistical distribution of grades over the number of students that obtained the respective grade.       |     [0..1]         | N/A       |
|     grading scheme     |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)               	|     Dereferenceable identifier to the grading system that was used to give the grade.		   				   |     [0..1]         | N/A       |
|     status 		     |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)        	        |     An indicator of the status of the course and the obtained grade, e.g. pass, fail, in-progress, unknown.  |     [1..1]         | TBD       |
|     value 		     |     Literal        	    |     A (quantitative or qualitative) value according to the definition in the grading scheme.				   |     [0..1]         | N/A       |

