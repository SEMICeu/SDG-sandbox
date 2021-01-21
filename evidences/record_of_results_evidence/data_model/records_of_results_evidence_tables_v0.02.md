# Disclaimer

This page relates to [version (v0.02)](record_of_results_evidence_diagram_v0.02.png) of the model.

---
# Record of Results Evidence

## Entities

### *Tertiary Education Evidence*

**Definition**: Abstract superclass for evidences that are issued after obtaining a Tertiary Education grade.

**Superclass of**: Tertiary Education Diploma Evidence (and Tertiary Education Diploma Supplement Evidence and Record of Results Evidence)

|     attribute          |	   expected type	     |	 definition	                                                                                                                                                                        |	  cardinality	   |	code list 																																														    			       |
|------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
|     identifier         |     Identifier	         |   An unambiguous reference to the Tertiary Education Evidence.                                                                                                                       |     [1..1]         |  N/A  						     																																														   |
|     issuing date    	 |     Date		             |	 The date on which the Tertiary Education Evidence was issued.                                                                                                                      |     [1..1]         |  N/A       																																															    			   |
|     language  	     |     Code                  |   The language in which the Tertiary Education Evidence is issued.                                                                                                                   |     [1..*]         |  [Language](http://publications.europa.eu/resource/authority/language)       																																			   |
|     qualification name |     Text	                 |   Full name of the qualification, at least in the original language(s) as it is styled in the original qualification, e.g. Master of Science, Kandidat nauk, Maîtrise, Diplom, etc.  |     [1..*]         |  N/A         																																																		       |
|     issuing place      |     Location   	         |   The Location where the Tertiary Education Evidence was issued.                                                                                                                     |     [1..1]         |  N/A      																																																				   |
|     belongs to         |     Student	             |   The Student that is the holder of the Tertiary Education Evidence.  	                                                                                                            |     [1..1]         |  N/A       																																																    		   |
|     obtained at        |     Education Institution |   The Education Institution that educated the Student.                                                                                                                               |     [1..*]         |  N/A       																																																	    	   |
|     issuing authority  |     Organisation     	 |   The Organisation that issued the Tertiary Education Evidence.                                                                                                                      |     [1..*]         |  N/A 																																																					   |


### Record of Results Evidence

**Definition**: A record of the Student's progress in his/her studies: the educational components they have taken, the number of ECTS credits they have achieved, and the grades they have been awarded.

**Subclass of**: Tertiary Education Evidence

|     attribute               |     expected type                                   |     definition                                                    		                                         |     cardinality    | code list |
|-----------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     academic year           |     Period                                          |     The period during which the courses and exams took place.                 					                 |     [1..1]         | N/A       |
|     total credits           |     Float                                           |     The total number of ECTS credits of the courses contained within the Record of Results.                        |     [1..1]         | N/A       |
|     contains                |     Course Result                                   |     The specific course results that together make up the Record of Results Evidence.                              |     [0..*]         | N/A       |
|     is record of results of |     Tertiary Education Diploma Supplement Evidence  |     The Tertiary Education Diploma Supplement Evidence to which this Record of Results Evidence is complementary.  |     [0..1]         | N/A       |


### Course Result 

**Definition**: Grade obtained after finishing/completing a course.

|     attribute                |     expected type          |     definition                                                    		                                                                                  |     cardinality    | code list |
|------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     course academic period   |     Text                   |     Period of the academic year when the course took place, e.g. first semester, second trimester, etc.                                                     |     [0..1]         | N/A       |
|     course academic year     |     Date                   |     The annual period of sessions of an educational programme usually beginning in September and ending in June.                              			  |     [0..1]         | N/A       |
|     course credits amount    |     Float                  |     The number of ECTS credits for the course, expressing the volume of learning based on the defined learning outcomes and their associated workload.      |     [1..1]         | [ECTS]( https://ec.europa.eu/assets/eac/education/ects/users-guide/glossary_en.htm#european-credit-transfer-and-accumulation-system)      |
|     course field of study    |     Code        		    |     The discipline or subject area of a course.                                                                                               			  |     [0..*]         | [ISCED 2013](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-fields-of-education-and-training-2013-detailed-field-descriptions-2015-en.pdf)        |
|     course grade             |     Grade                  |     A mark indicating a degree of accomplishment for a particular course.                                                                                   |     [1..1]         | N/A       |
|     course language          |     Code        		    |     Main language in which the course was taught.	                   			                                                                              |     [0..1]         | N/A       |
|     course name              |     Text                   |     Name given to a number of lectures or other matters dealing with a subject, i.e. the course.                                                            |     [1..1]         | N/A       |


### Tertiary Education Diploma Supplement Evidence

**Definition**: Document accompanying a Tertiary Education Diploma Evidence, providing a standardised description of the nature, level, context, content and status of the studies completed by its holder.

**Subclass of**: Tertiary Education Evidence

| attribute                   |     expected type                        |     definition                                                 		                                                         |   cardinality      | code list 																																																			  |
|-----------------------------|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| academic programme language |     Code                                 |     The language in which the qualification was officially delivered and examined.                                             |   [0..1]           | [Language](http://publications.europa.eu/resource/dataset/language)  																																				  |
| academic year               |     Period                               |     The period during which the courses and exams took place.                                                                  |   [1..1]           | N/A  	 																																											 								  |
| access requirement          |     Code                                 |     Qualification(s) or periods of study required for access to the programme.                                                 |   [0..*]           | [ISCED 2011](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-isced-2011-en.pdf)  														    				  |
| grade point average         |     Grade                                |     The grade point average of the course results, i.e. grades weighted based on the number of credits.                        |   [0..1]           | N/A       																																																			  |
| language of instruction     |     Code                                 |     The different languages in which the programme was given.                                                                  |   [0..*]           | [Language](http://publications.europa.eu/resource/dataset/language)       																																			  |
| main field of study         |     Code                                 |     The main disciplines or subject areas of a qualification.                                                                  |   [0..*]           | [ISCED 2013](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-fields-of-education-and-training-2013-detailed-field-descriptions-2015-en.pdf)       			  |
| mode of study               |     Code                                 |     The way the programme was undertaken, e.g. full-time, part-time, intermittent/sandwich, e-learning, distance, etc.         |   [0..1]           | TBC      																																																			  |
| programme learning outcomes |     Text                                 |     Statements of what the Student knows, understands and is able to do after completing his/her studies and receiving the qualification (knowledge, skills, competencies). Learning outcomes should be expressed in the present tense, e.g.: “The graduate can analyse consumer behaviour trends and apply them in a given consumer market”.           | [0..1]   | N/A    |
| qualification level         |     Code			                     |     Level of the obtained qualification.                                                                                       |   [0..1]           | [ISCED 2011](http://uis.unesco.org/sites/default/files/documents/international-standard-classification-of-education-isced-2011-en.pdf)     																			  |
| study duration              |     Float                                |     Official duration of the programme in years of full-time study.                                                            |   [0..1]           | N/A       																																																			  |
| total credits               |     Float                                |     Total student workload required, described in terms of ECTS credits.                                                       |   [0..1]           | N/A                                                                                                                                                                                                                   |
| is supplement of            |     Tertiary Education Diploma Evidence  |     The Tertiary Education Diploma Evidence to which this Supplement refers.                                                   |   [0..1]           | N/A      


### Tertiary Education Diploma Evidence

**Definition**: Any formally awarded qualification/credential, issued by a competent authority attesting the successful completion of a recognised programme of study of tertiary education.

**Subclass of**: Tertiary Education Evidence

|     attribute                       |     expected type                                    |    definition                                                    		                                                                                                                                                    |     cardinality    | code list |
|-------------------------------------|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     academic programme              |     Text                                             |    The set of course units, the various components of which complement and build on each other in order to provide the student with a higher education qualification.                                                        |     [1..1]         | N/A       |
|     access to further study         |     Code                                             |    Details of access to further academic and/or professional studies the qualification provides, especially to specific qualifications, or levels of study, e.g.: access to Doctoral studies in the country or institution.  |     [0..*]         | [ISCED 2011 Levels]( http://uis.unesco.org/sites/default/files/documents/isced-2011-operational-manual-guidelines-for-classifying-national-education-programmes-and-related-qualifications-2015-en_1.pdf)  |
|     access to regulated profession  |     Text                                             |    Details of any rights to practise, or professional title, accorded to the holder of the qualification, in accordance with national legislation or requirements by a competent authority.                                  |     [0..*]         | N/A       |
|     level of distinction            |     Code                                             |    Indication of the level of distinction with which an academic degree has been earned, e.g. First Class Honors Degree, Summa Cum Laude, Merit, Avec Distinction, Avec mention, etc.                                        |     [0..1]         | TBD       |
|     overall grade                   |     Grade                                            |    A mark indicating a degree of accomplishment.                                                                                                                                                                             |     [1..1]         | N/A       |
|     thesis title                    |     Text                                             |    Title of the dissertation completed by a student as part of a tertiary education degree.                                                                                                                                  |     [0..1]         | N/A       |


### Education Institution
**Definition**: An Organisation that provides instructional services to individuals or education-related services to individuals and other educational institutions.

**Subclass of**: Organisation

*No additional attributes are defined for this entity. It does inherit, however, all the attributes from the Organisation entity listed here below.*


### Organisation
**Definition**: Represents a collection of people organized together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it and can act as an Agent. Organizations are often decomposable into hierarchical structures.

|     attribute           |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list |
|-------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier          |     Identifier     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [1..*]          |  N/A      |
|     preferred label     |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          |  N/A      |
|     registered location |     Location       |     The registered location of the Organisation.   																																																																															     	       |    [0..1]          |  N/A      |


### Student
**Definition**: A person who attends a Tertiary Education Institution.

|     attribute   				 |     expected type  		|     definition                                                                                  	|     cardinality    | code list | 
|--------------------------------|--------------------------|---------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     student ID        		 |     Identifier        	|     An unambiguous reference to the Student.										        		|     [0..*]         | N/A       |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute           |     expected type |     definition       											 																																																																																												|     cardinality   | code list |
|-------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier          |     Identifier    |     The identifier relation is used to link a Person to any formally issued Identifier for that Person.     																																																																																	|     [0..*]        | N/A       |
|     family name         |     Text          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".        |     [1..1]        | N/A       |
|     given name          |     Text          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johann Sebastian Bach is “Johann Sebastian”.                                                                |     [1..1]        | N/A       |
|     date of birth       |     Date          |     A date that specifies the birth date of a Person.                                                                                                                                                                                                                                                                                                                                                                                           |     [1..1]        | N/A       |
|     sex                 |     Code          |     The chromosomal state, and reproductive organs and structures of a Person that allows them to be distinguished as female or male.            			                                                                                                                                                                                                                                                                  		            |     [0..1]        | [Human Sex](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/human-sex/?target=Browse&uri=http://publications.europa.eu/resource/authority/human-sex) |
|     place of birth      |     Location      |     The Location where a Person was born.                                                                                                                                                                                                                                                                                                                                                                                                       |     [0..1]        | N/A       |
|     registered address  |     Address       |     The registered address of the Person.                                                    																																																																																          			|     [0..1]        | N/A       |


### Location
**Definition**: A spatial region or named place.

|     attribute             |     expected type  |     definition                                                                                                                                                                                                                                                     |     cardinality    | code list |
|---------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     geographic name       |     Text           |     A geographic name is a proper noun applied to a spatial object. The INSPIRE Data Specification on Geographical Names [INGN] provides a detailed model for describing a 'named place', including methods for providing multiple names in multiple scripts.      |     [0..1]         | N/A       | 
|     geographic identifier |     URI            |     A URI that identifies the Location.                                                                                                                                                                                                                            |     [0..1]         | N/A       |
|     address               |     Address        |     The address property relationship associates a Location with the Address entity.                                                                                                                                                                               |     [0..1]         | N/A       |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute           |     expected type |     definition                                                                                                              |     cardinality    | code list																																											   |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     admin unit level 1  |     Code          |     The uppermost administrative unit for the address, almost always a country.                                             |     [1..1]         | [Country](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/country/?target=Browse&uri=http://publications.europa.eu/resource/authority/country)       |
|     admin unit level 2  |     Text          |     The region of the address, usually a county, state or other such area that typically encompasses several localities.    |     [0..1]         | N/A                                                                                                                                                                                     |
|     full address        |     Text          |     The complete address written as a string, with or without formatting.                                                   |     [0..1]         | N/A                                                                                                                                                                                     |


## Complex datatypes

### Grade
**Definition**: Mark indicating a degree of accomplishment.

|     attribute   		 |     expected type  		|     definition                                                                                               |     cardinality    | code list | 
|------------------------|--------------------------|--------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     distribution 		 |     Text        	        |     Statistical distribution of grades over the number of students that obtained the respective grade.       |     [0..1]         | N/A       |
|     grading scheme     |     URI               	|     Dereferenceable identifier to the grading system that was used to give the grade.		   				   |     [0..1]         | N/A       |
|     status 		     |     Code        	        |     An indicator of the status of the course and the obtained grade, e.g. pass, fail, in-progress, unknown.  |     [1..1]         | TBD       |
|     value 		     |     Literal        	    |     A (quantitative or qualitative) value according to the definition in the grading scheme.				   |     [0..1]         | N/A       |



