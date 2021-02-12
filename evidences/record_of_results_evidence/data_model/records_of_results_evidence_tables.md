# Record of Results Evidence

## Entities

### *Tertiary Education Evidence*

**Definition**: Abstract superclass for evidences that are issued after obtaining a Tertiary Education grade.

**Superclass of**: [Tertiary Education Diploma Evidence](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_evidence/data_model/tertiary_education_diploma_evidence_tables_v0.02.md#tertiary-education-diploma-evidence-1), [Tertiary Education Diploma Supplement Evidence](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_supplement_evidence/data_model/tertiary_education_diploma_supplement_evidence_tables_v0.02.md#tertiary-education-diploma-supplement-evidence-1) and [Record of Results Evidence](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/record_of_results_evidence/data_model/records_of_results_evidence_tables_v0.02.md#record-of-results-evidence-1)

|     attribute          |	   expected type	     |	 definition	                                                                                                                                                                        |	  cardinality	   |	code list 																																														    			       |
|------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
|     identifier         |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)	         |   An unambiguous reference to the Tertiary Education Evidence.                                                                                                                       |     [1..1]         |  N/A  						     																																														   |
|     issuing date    	 |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)		             |	 The date on which the Tertiary Education Evidence was issued.                                                                                                                      |     [1..1]         |  N/A       																																															    			   |
|     language  	     |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                  |   The language in which the Tertiary Education Evidence is issued.                                                                                                                   |     [1..*]         |  [Language](http://publications.europa.eu/resource/authority/language)       																																			   |
|     qualification name |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)	                 |   Full name of the qualification, at least in the original language(s) as it is styled in the original qualification, e.g. Master of Science, Kandidat nauk, Maîtrise, Diplom, etc.  |     [1..*]         |  N/A         																																																		       |
|     issuing place      |     Location   	         |   The Location where the Tertiary Education Evidence was issued.                                                                                                                     |     [1..1]         |  N/A      																																																				   |
|     belongs to         |     Student	             |   The Student that is the holder of the Tertiary Education Evidence.  	                                                                                                            |     [1..1]         |  N/A       																																																    		   |
|     obtained at        |     Education Institution |   The Education Institution that educated the Student.                                                                                                                               |     [0..*]         |  N/A       																																																	    	   |
|     issuing authority  |     Organisation     	 |   The Organisation that issued the Tertiary Education Evidence.                                                                                                                      |     [1..*]         |  N/A 																																																					   |


### Record of Results Evidence

**Definition**: A record of the Student's progress in his/her studies: the educational components they have taken, the number of ECTS credits they have achieved, and the grades they have been awarded.

**Subclass of**: Tertiary Education Evidence

|     attribute               |     expected type                                   |     definition                                                    		                                         |     cardinality    | code list |
|-----------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     academic year           |     [Period](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#period)                                          |     The period during which the courses and exams took place.                 					                 |     [1..1]         | N/A       |
|     total credits           |     [Float](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#primitive-data-types)                                           |     The total number of ECTS credits of the courses contained within the Record of Results.                        |     [1..1]         | N/A       |
|     contains                |     Course Result                                   |     The specific course results that together make up the Record of Results Evidence.                              |     [0..*]         | N/A       |
|     is record of results of |     Tertiary Education Diploma Supplement Evidence  |     The Tertiary Education Diploma Supplement Evidence to which this Record of Results Evidence is complementary.  |     [0..1]         | N/A       |


### Course Result 

**Definition**: Grade obtained after finishing/completing a course.

|     attribute                |     expected type          |     definition                                                    		                                                                                  |     cardinality    | code list |
|------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     course academic period   |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                   |     Period of the academic year when the course took place, e.g. first semester, second trimester, etc.                                                     |     [0..1]         | N/A       |
|     course academic year     |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)                   |     The annual period of sessions of an educational programme usually beginning in September and ending in June.                              			  |     [0..1]         | N/A       |
|     course credits amount    |     [Float](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#primitive-data-types)                  |     The number of ECTS credits for the course, expressing the volume of learning based on the defined learning outcomes and their associated workload.      |     [1..1]         | N/A      |
|     course field of study    |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)        		    |     The discipline or subject area of a course.                                                                                               			  |     [0..*]         | [ISCED 2013](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-fields-of-education-and-training-2013-detailed-field-descriptions-2015-en.pdf)        |
|     course grade             |     Grade                  |     A mark indicating a degree of accomplishment for a particular course.                                                                                   |     [1..1]         | N/A       |
|     course language          |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)        		    |     Main language in which the course was taught.	                   			                                                                              |     [0..*]         | N/A       |
|     course name              |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                   |     Name given to a number of lectures or other matters dealing with a subject, i.e. the course.                                                            |     [1..1]         | N/A       |



### Tertiary Education Diploma Supplement Evidence

**Definition**: Document accompanying a Tertiary Education Diploma Evidence, providing a standardised description of the nature, level, context, content and status of the studies completed by its holder.

**Subclass of**: Tertiary Education Evidence

For further information, please see the [tertiary education diploma supplement evidence data model](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_supplement_evidence/data_model/tertiary_education_diploma_supplement_evidence_tables_v0.02.md)   


### Tertiary Education Diploma Evidence

**Definition**: Any formally awarded qualification/credential, issued by a competent authority attesting the successful completion of a recognised programme of study of tertiary education.

**Subclass of**: Tertiary Education Evidence

For further information, please see the [tertiary education diploma evidence data model](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_evidence/data_model/tertiary_education_diploma_evidence_tables_v0.02.md)


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
|     registered location |     Location      |     The registered location of the Organisation.   																																																																																       |    [0..*]          |  N/A      | 


### Student
**Definition**: A person who attends a Tertiary Education Institution.

|     attribute   				 |     expected type  		|     definition                                                                                  	|     cardinality    | code list | 
|--------------------------------|--------------------------|---------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     student ID        		 |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)        	|     An unambiguous reference to the Student.										        		|     [0..*]         | N/A       |


#### Person

**Definition**: An individual person who may be dead or alive, but not imaginary.

**Source**: [ISA² Core Person Vocabulary](https://www.w3.org/ns/person)

|     attribute           |     expected type |     definition       											 																																																																																												|     cardinality   | code list | 
|-------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier          |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)    |     The identifier relation is used to link a Person to any formally issued Identifier for that Person.     																																																																																	|     [0..*]        | N/A       | 
|     given name          |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johann Sebastian Bach is “Johann Sebastian”.                                                                  |     [1..*]        | N/A       | 
|     family name         |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".        |     [1..*]        | N/A       | 
|     date of birth       |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)          |     The day on which the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                       |     [0..1]        | N/A       |
|     sex                 |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)          |     The chromosomal state, and reproductive organs and structures of a Person that allows them to be distinguished as female or male.                                                                                                                                                                                                                                                                                                        |     [0..1]        |    [Human Sex](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/human-sex/?target=Browse&uri=http://publications.europa.eu/resource/authority/human-sex) | 
|     place of birth      |     Location      |     The Location where the Person was born.                                                                                                                                                                                                                                                                                                                                                                                                    |     [0..1]        |    N/A                                                                                                                                                                                     | 
|     registered address  |     Address     |     The registered address of the Person.                                                    																																																																																          			|     [0..1]        | N/A       | N/A |


#### Location
**Definition**: An identifiable geographic place or named place.

**Source**: [ISA² Core Location Vocabulary](https://www.w3.org/ns/locn)

_Given that both attributes are optional, at least one of the attributes must be provided._


|     attribute              |     expected type  |     definition                                                                                                                                                                                                                                                 |     cardinality    |  code list                                                                                                                                                                       | 
|----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     geographic name        |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.  |     [0..*]         |  N/A  | 
|     geographic identifier  |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)            |     A URI that identifies the Location.                                                                                                                                                                                                                        |     [0..1]         |  [GeoNames](https://www.geonames.org/)   | 
|     address               |     Address        |     The address property relationship associates a Location with the Address entity.                                                                                                                                                                               |     [0..1]         | N/A       | 

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


