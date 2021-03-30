# Tertiary Education Diploma Supplement Evidence

## Entities

### *Tertiary Education Evidence*

**Definition**: Abstract superclass for evidences that are issued after obtaining a Tertiary Education grade.

**Superclass of**: [Tertiary Education Diploma Evidence](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_evidence/data_model/tertiary_education_diploma_evidence_tables.md#tertiary-education-diploma-evidence-1), [Tertiary Education Diploma Supplement Evidence](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_supplement_evidence/data_model/tertiary_education_diploma_supplement_evidence_tables.md#tertiary-education-diploma-supplement-evidence-1) and [Record of Results Evidence](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/record_of_results_evidence/data_model/records_of_results_evidence_tables.md#record-of-results-evidence-1)

|     attribute          |	   expected type	     |	 definition	                                                                                                                                                                        |	  cardinality	   |	code list 																																														    			       |
|------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
|     identifier         |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)	         |   An unambiguous reference to the Tertiary Education Evidence.                                                                                                                       |     [1..1]         |  N/A  						     																																														   |
|     issue date    	 |     [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)		             |	 The date on which the Tertiary Education Evidence was issued.                                                                                                                      |     [1..1]         |  N/A       																																															    			   |
|     language  	     |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                  |   The language in which the Tertiary Education Evidence is issued.                                                                                                                   |     [1..*]         |  [Language](http://publications.europa.eu/resource/authority/language)       																																			   |
|     qualification name |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)	                 |   Full name of the qualification, at least in the original language(s) as it is styled in the original qualification, e.g. Master of Science, Kandidat nauk, Maîtrise, Diplom, etc.  |     [1..*]         |  N/A         																																																		       |
|     issuing place      |     Location   	         |   The Location where the Tertiary Education Evidence was issued.                                                                                                                     |     [1..1]         |  N/A      																																																				   |
|     belongs to         |     Person	             |   The Person that is the holder of the Tertiary Education Evidence.  	                                                                                                            |     [1..1]         |  N/A       																																																    		   |
|     obtained at        |     Education Institution |   The Education Institution that educated the Student.                                                                                                                               |     [0..*]         |  N/A       																																																	    	   |
|     issuing authority  |     Organisation     	 |   The Organisation that issued the Tertiary Education Evidence.                                                                                                                      |     [1..*]         |  N/A 																																																					   |

 
### Tertiary Education Diploma Supplement Evidence

**Definition**: Document accompanying a Tertiary Education Diploma Evidence, providing a standardised description of the nature, level, context, content and status of the studies completed by its holder.

**Subclass of**: Tertiary Education Evidence

| attribute                   |     expected type                        |     definition                                                 		                                                         |   cardinality      | code list 																																																			  |
|-----------------------------|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| academic programme language |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                                 |     The language in which the qualification was officially delivered and examined.                                             |   [0..*]           | [Language](http://publications.europa.eu/resource/dataset/language)  																																				  |
| Awarding Date               |    [Date](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#datetime)                               |     The date when the qualification was awarded.                                                                  |   [1..1]           | N/A  	 																																											 								  |
| access requirement          |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                                 |     Qualification(s) or periods of study required for access to the programme.                                                 |   [0..*]           | [ISCED 2011](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-isced-2011-en.pdf)  														    				  |
|     access to further study         |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                                             |    Details of access to further academic and/or professional studies the qualification provides, especially to specific qualifications, or levels of study, e.g.: access to Doctoral studies in the country or institution.  |     [0..*]         | [ISCED 2011 Levels]( http://uis.unesco.org/sites/default/files/documents/isced-2011-operational-manual-guidelines-for-classifying-national-education-programmes-and-related-qualifications-2015-en_1.pdf)  |
|     access to regulated profession  |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                                             |    Details of any rights to practise, or professional title, accorded to the holder of the qualification, in accordance with national legislation or requirements by a competent authority.                                  |     [0..*]         | N/A       |
| grade point average         |     Grade                                |     The grade point average of the course results, i.e. grades weighted based on the number of credits.                        |   [0..1]           | N/A       																																																			  |
| language of instruction     |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                                 |     The different languages in which the programme was given.                                                                  |   [0..*]           | [Language](http://publications.europa.eu/resource/dataset/language)       																																			  |
| main field of study         |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                                 |     The main disciplines or subject areas of a qualification.                                                                  |   [0..*]           | [ISCED 2013](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-fields-of-education-and-training-2013-detailed-field-descriptions-2015-en.pdf)       			  |
| mode of learning               |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)                                 |     The mode of learning and/or assessment.         |   [0..1]           | Europass Standard List of Modes Of Learning and Assessment. |
| programme learning outcome |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)                                 |    A statement of what the individual knows, understands
and is able to do on completion of a learning process.          | [0..*]   | N/A    |
| qualification level         |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)			                     |     Level of the obtained qualification.                                                                                       |   [0..1]           | [ISCED 2011](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-isced-2011-en.pdf)     																			  |
| study duration              |     [Float](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#primitive-data-types)                                |     Official duration of the programme in years of full-time study.                                                            |   [0..1]           | N/A       																																																			  |
| total credits               |     [Float](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#primitive-data-types)                                 |     The total number of credit points assigned to the qualification, following the ECTS credit system.	                                                       |   [0..1]           | ECTS scoring scheme from Europass Standard List of Educational Credit Systems.                                                                                                                                                  |
|     total semesters              |     [Float](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#primitive-data-types)                    |     Number of 6-month periods the student already has studied in total.                                                            |     [0..1]         | N/A       |
| is supplement of            |     Tertiary Education Diploma Evidence  |     The Tertiary Education Diploma Evidence to which this Supplement refers.                                                   |   [0..1]           | N/A      
| has record of results       |     Record of Results Evidence           |     The Record of Results Evidence that is complementary to the Tertiary Education Diploma Supplement Evidence.                |   [0..1]           | N/A                                                                                                                                                                                                                   |


### Tertiary Education Diploma Evidence

**Definition**: Any formally awarded qualification/credential, issued by a competent authority attesting the successful completion of a recognised programme of study of tertiary education.

**Subclass of**: Tertiary Education Evidence

For further information, please see the [tertiary education diploma evidence data model](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/tertiary_education_diploma_evidence/data_model/tertiary_education_diploma_evidence_tables.md)


### Record of Results Evidence

**Definition**: An official record or breakdown of a student’s progress and achievements.

**Subclass of**: Tertiary Education Evidence

For further information, please see the [record of results evidence data model](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/record_of_results_evidence/data_model/records_of_results_evidence_tables.md)


### Course Result 

**Definition**: Grade obtained after finishing/completing a course.

For further information, please see the [record of results evidence data model](https://github.com/SEMICeu/SDG-sandbox/blob/master/evidences/record_of_results_evidence/data_model/records_of_results_evidence_tables.md)


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
|     identifier          |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)     |     Many organisations are referred to by some identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [0..*]          |  N/A      | 
|     registered location |     Location      |     The registered location of the Organisation.   																																																																																       |    [0..*]          |  N/A      | 


### Student
**Definition**: A person who attends a Tertiary Education Institution.

|     attribute   				 |     expected type  		|     definition                                                                                  	|     cardinality    | code list | 
|--------------------------------|--------------------------|---------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     student ID        		 |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)        	|     An unambiguous reference to the Student.										        		|     [0..*]         | N/A       |


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
                                                                                                                                                                                    |


## Complex datatypes

### Grade
**Definition**: Mark indicating a degree of accomplishment.

|     attribute   		 |     expected type  		|     definition                                                                                               |     cardinality    | code list | 
|------------------------|--------------------------|--------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     distribution 		 |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)        	        |     Statistical distribution of grades over the number of students that obtained the respective grade.       |     [0..1]         | N/A       |
|     grading scheme     |     [URI](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#data-types)               	|     Dereferenceable identifier to the grading system that was used to give the grade.		   				   |     [0..1]         | N/A       |
|     status 		     |     [Code](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#code)        	        |     An indicator of the status of the course and the obtained grade, e.g. pass, fail, in-progress, unknown.  |     [1..1]         | TBD       |
|     value 		     |     Literal        	    |     A (quantitative or qualitative) value according to the definition in the grading scheme.				   |     [0..1]         | N/A       |



