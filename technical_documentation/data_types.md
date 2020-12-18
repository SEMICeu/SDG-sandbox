# Data Types

Source: *This page is based on the [Core Vocabularies Business, Location and Person Specification v1.00](https://github.com/SEMICeu/Core-Person-Vocabulary/blob/master/releases/1.00/Core_Vocabularies-Business_Location_Person-Specification-v1.00.pdf).*


## Primitive data types

For a full explanation on primitive datatypes, we refer to the [W3C XML Schema Definition Language (XSD) 1.1 Part 2: Datatypes](https://www.w3.org/TR/xmlschema11-2/#built-in-primitive-datatypes). Here we just give a quick overview of the relevant primitive datatypes and their definition.

|   primitive datatype   |   definition
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   [string](https://www.w3.org/TR/xmlschema-2/#string)               |   The string datatype represents a finite-length sequence of characters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|   [boolean](https://www.w3.org/TR/xmlschema-2/#boolean)           |   The boolean datatype represents the values of two-valued logic.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|   [decimal](https://www.w3.org/TR/xmlschema-2/#decimal)              |   The decimal datatype represents a subset of the real numbers, which can be represented by decimal numerals. The ·value space· of decimal is the set of numbers that can be obtained by dividing an integer by a non-negative power of ten, i.e., expressible as i / 10n where i and n are integers and n ≥ 0. Precision is not reflected in this value space; the number 2.0 is not distinct from the number 2.00. The order relation on decimal is the order relation on real numbers, restricted to this subset.                                                                                                                                                                                                                 |
|   [float](https://www.w3.org/TR/xmlschema-2/#float)             |   The float datatype is patterned after the IEEE single-precision 32-bit floating point datatype [IEEE 754-2008]. Its value space is a subset of the rational numbers. Floating point numbers are often used to approximate arbitrary real numbers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|   [double](https://www.w3.org/TR/xmlschema-2/#double)              |   The double datatype is patterned after the IEEE double-precision 64-bit floating point datatype [IEEE 754-2008]. Each floating point datatype has a value space that is a subset of the rational numbers. Floating point numbers are often used to approximate arbitrary real numbers.																																																																                                                                                                                                                                                |							
|   [duration](https://www.w3.org/TR/xmlschema-2/#duration)             |   The duration datatype is a datatype that represents durations of time. The concept of duration being captured is drawn from those of [ISO 8601], specifically durations without fixed endpoints. For example, "15 days" (whose most common lexical representation in duration is "'P15D'") is a duration value; "15 days beginning 12 July 1995" and "15 days ending 12 July 1995" are not duration values. Duration can provide addition and subtraction operations between duration values and between duration/dateTime value pairs, and can be the result of subtracting dateTime values. However, only addition to dateTime is required for XML Schema processing and is defined in the function ·dateTimePlusDuration·.      |
|   [dateTime](https://www.w3.org/TR/xmlschema-2/#dateTime)             |   The dateTime datatype represents instants of time, optionally marked with a particular time zone offset.  Values representing the same instant but having different time zone offsets are equal but not identical.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|   [time](https://www.w3.org/TR/xmlschema-2/#time)                 |   The time datatype represents instants of time that recur at the same point in each calendar day, or that occur in some arbitrary calendar day.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|   [date](https://www.w3.org/TR/xmlschema-2/#date)                |   The date datatype represents top-open intervals of exactly one day in length on the timelines of dateTime, beginning on the beginning moment of each day, up to but not including the beginning moment of the next day).  For non-timezoned values, the top-open intervals disjointly cover the non-timezoned timeline, one per day.  For timezoned values, the intervals begin at every minute and therefore overlap.                                                                                                                                                                                                                                                                                                             |
|   [anyURI](https://www.w3.org/TR/xmlschema-2/#anyURI)              |   The anyURI datatype represents an Internationalized Resource Identifier Reference (IRI). An anyURI value can be absolute or relative, and may have an optional fragment identifier (i.e., it may be an IRI Reference). This type should be used when the value fulfills the role of an IRI, as defined in [RFC 3987] or its successor(s) in the IETF Standards Track.                                                                                                                                                                                                                                                                                                                                                              |


### Date(Time)

Dates recorded within public sector data sets exist in many different formats.
In order to make those dates interoperable, it is important that they should be represented in a regular manner wherever possible.
The most widely used date formats are those that conform to ISO 8601:2004 [ISO 8601] of which the relevant XML Datatypes [XSD] are a subset.
Dates should be recorded as formatted strings that are conformant with that standard with the relevant data type declaration.

Known dates are recorded as literals in the form `yyyy-mm-dd` and then typed as `xsd:date`.

Where the full date and time are both known, and this can be important in records of death for example, use the `xsd:dateTime` format of `yyyy-mm-ddThh:mm:ss` with or without timezone information.

Where just a year is known use `xsd:gYear` (yyyy) and where just the month is known use `xsd:gYearMonth` (yyyy-mm).
The 'g' is for Gregorian. Non-Gregorian dates are not covered by XSD.

For emphasis, the datatype should be explicitly stated so that software can correctly interpret the data.
If a date is provided in a string that is conformant with a standard other than XSD, and that is not covered by XSD, then it should be typed accordingly.
It should also be noted that the UK Government provides a URI scheme for time intervals that may be useful [DGUT] and that 8601:2004 itself allows intervals to be defined.

In some public sector data sets, full dates are not always known. For example, dates such as "some time in the 1920s" or "between 1925 and 1932" are not uncommon.
There is no agreed formal way to record such uncertainty dates and therefore an un-typed plain string should be used.
In other words, a string like "between 1925 and 1932" cannot be improved upon.
To use an interval as the value for, say, a date of birth, is incorrect, The date of birth is not the time interval that began in 1925 and ended in 1932, rather, it was an instant some time during that period.
There is an important difference between declaring that an event occurred throughout a time interval and that it occurred at an unknown instant within a time interval.

Some data sets use other methods to express uncertainty such as using false dates.
Sometimes '00' or '??' is used to indicate uncertainty so that "August 1986" might be recorded as either 1986-00-00 or 1986-00-??.
This practice is unnecessary and strongly discouraged, particularly if such dates are typed as XSD dates.
If a string such as 1986-08-00 is fed to software expecting an `xsd:date` then it will either reject the data, in which case data is lost, or it might convert it to the nearest actual date 1986-08-01.
In the latter case, the accurate yet imprecise date of "August 1986" has now been converted to a more precise date of 1st August 1986 that may be anything up to 30 days wide of the truth.

In summary:
- use the appropriate XSD data type wherever possible (dateTime, date, gYearMonth, gYear);
- where data is missing, don't invent it or try to fool the system - just give the date as an un-typed string.

#### Period

For the expression of a period of time (also called: time interval), we refer to the [Extended Date/Time Format (EDTF)](https://www.loc.gov/standards/datetime/) Specification.
‘2004-02-01/2005-02-08’ is an example of a (EDTF Level 0) time interval with calendar day precision, beginning sometime on February 1, 2004 and ending sometime on February 8, 2005.


## Text

The text data type is a combination of a string and a language identifier.
It is useful for names and descriptions that are available in multiple languages.
Where this is so, each version of the data should be included and each one associated with the relevant language identifier.
RFC 3066 [RFC 3066] provides a commonly used set of identifiers for natural languages. This is the set recognised by UN/CEFACT and XML Schema.

Languages are represented by two character codes, optionally followed by a locale definition such as "de" meaning German and "de-at" meaning "German as spoken in Austria."

XML Example:
```
<Location>
  <geographicName xml:lang="en">London</geoGraphicName>
  <geographicName xml:lang="fr">Londres</geoGraphicName>
</Location>
```

RDF Example:
```
[] a locn:Location ;
  locn:geographicName "London"@en ;
  locn:geographicName "Londres"@fr .
```


## Code

Interoperability between data sets is increased dramatically when terms from controlled vocabularies are used in favour of free text.
The conceptual Code data type is used wherever one or more controlled vocabularies are known to exist for a particular domain of interest.
It is not the job of Core Vocabularies to mandate which controlled vocabularies are used but we offer some guidance on how to use them.

It is important not only to use a term from a controlled vocabulary correctly (ideally a user interface would allow a term to be selected from a list rather than entered manually)
but also to identify the source of the term, i.e. to use or, where necessary create, a datatype that is unambiguously associated with the term.

How this is done depends on the controlled vocabulary in question and how it is published.


### XML Representation

To increase interoperability, the Core Data Type ‘Code’ of the UN/CEFACT Core Component Library [UN/CEFACT] can be used to provide metadata to the origin of the code.
Where the publisher of the controlled vocabulary does not provide an XML schema it is necessary to use the Code datatype.
For example, the following encodes the company type of "C18.01.02 - Other printing" according to Rev 2 of the European Commission's NACE codes.

```
<CompanyTypeCvbusinessCode>
  <Content>C18.01.02 - Other printing</Content>
  <List>NACE</List>
  <ListAgency>European Commission</ListAgency>
  <ListVersion>Rev 2</ListVersion>
<CompanyTypeCvbusinessCode>
```

### RDF Representation

The Code datatype is best encoded in RDF as a SKOS Concept [SKOS].
Some controlled vocabularies are already published as such concept schemes.
For example, to encode the female gender (section 3.1.6) using the SDMX code list, it is possible simply to provide
http://purl.org/linked-data/sdmx/2009/code#sex-F as the venue of the gender property.

Where a vocabulary is not already available as a SKOS concept scheme, best practice is to create one as part of the data set (or better still, use someone else's encoding of it).
For example, Jeni Tennison encoded the Observation Status codes from the SDMX Code lists [SDMX A2] for use by the UK Government following this approach [UKCODE]. 

Using this approach we might create a SKOS Concept scheme based on the ISO 5218 code as shown in the following Turtle:

```
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix schema: <http://schema.org/> .
@prefix dcterms: <http://purl.org/dc/terms/> .

# First define a class that represents any value within the code list

<http://example.com/def/iso5218/sex>
  rdf:type <http://www.w3.org/2000/01/rdf-schema#Class> ;
  rdfs:label "Sex" ;
  rdfs:comment "This is the class of human sexes as defined by ISO 5218:2004" ;
  rdfs:subClassOf <http://www.w3.org/2004/02/skos/core#Concept> .
  
# Now define the concept scheme itself.
# Notice that the URI for each term in the vocabulary is listed
# as a top concept. This is a 'flat' scheme. Use the full power
# of SKOS to describe hierarchical schemes. Other appropriate
# terms can be used to add further annotation about the concept scheme
# if necessary (see lines 24 and 25).

<http://example.com/id/iso5218/>
  rdf:type <http://www.w3.org/2004/02/skos/core#ConceptScheme> ;
  skos:prefLabel "Codes for the representation of human sexes"@en ;
  skos:prefLabel "Codes de représentation des sexes humains"@fr ;
  skos:notation "ISO/IEC 5218:2004" ;
  skos:note "ISO 5218 specifies a uniform representation of human sexes for the interchange of information" ;
  skos:definition <http://standards.iso.org/ittf/PubliclyAvailableStandards/c036266_ISO_IEC_5218_2004(E_F).zip> ;
  skos:hasTopConcept <http://example.com/id/iso5218/0> ;
  skos:hasTopConcept <http://example.com/id/iso5218/1> ;
  skos:hasTopConcept <http://example.com/id/iso5218/2> ;
  skos:hasTopConcept <http://example.com/id/iso5218/9> ;
  schema:version "2004" ;
  dcterms:creator [dcterms:title "ISO"] .

# Now provide more detail about each of those concepts

<http://example.com/iso5218/id/sex/0>
  rdf:type <http://www.w3.org/2004/02/skos/core#Concept> ;
  rdf:type <http://example.com/def/iso5218/sex> ;
  skos:topConceptOf <http://example.com/id/iso5218/> ;
  skos:prefLabel "Not known"@en ;
  skos:prefLabel "Inconnu"@fr ;  # Note that labels can be provided in any number of languages
  skos:notation "0" ;  # The actual controlled vocabulary term is here, in this case, a single digit.
  skos:definition "More detail of the vocabulary term if available (it's not in the case of ISO 5218)" .
 
<http://example.com/iso5218/id/sex/1>
  rdf:type <http://www.w3.org/2004/02/skos/core#Concept> ;
  rdf:type <http://example.com/def/iso5218/sex> ;
  skos:topConceptOf <http://example.com/id/iso5218/> ;
  skos:prefLabel "Male"@en ;
  skos:prefLabel "Masculin"@fr ;
  skos:notation "1" .

<http://example.com/iso5218/id/sex/2>
  rdf:type <http://www.w3.org/2004/02/skos/core#Concept> ;
  rdf:type <http://example.com/def/iso5218/sex> ;
  skos:topConceptOf <http://example.com/id/iso5218/> ;
  skos:prefLabel "Feale"@en ;
  skos:prefLabel "Féminin"@fr ;
  skos:notation "2" .

<http://example.com/iso5218/id/sex/9>
  rdf:type <http://www.w3.org/2004/02/skos/core#Concept> ;
  rdf:type <http://example.com/def/iso5218/sex> ;
  skos:topConceptOf <http://example.com/id/iso5218/> ;
  skos:prefLabel "Not applicable"@en ;
  skos:prefLabel "Sans objet"@fr ;
  skos:notation "9" .
```

The following table shows how the terms used to create this concept scheme map to the Core Vocabularies Conceptual Model.

|   Conceptual Model   |   RDF term used
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   content            |   skos:prefLabel                                                                                                                                                                                                                                                                      |
|   list               |   skos:notation as a property of the concept scheme itself, in the example, this is ISA/IEC 5218:2004.                                                                                                                                                                                |
|   list agency        |   dcterms:creator (if the publisher has a URI, so much the better, if not, it may be necessary to create a blank node as shown in the example. The value of dcterms:creator should always be the URI of an Agent class, not a simple string or the URI of a Web site homepage etc.).  |
|   list version       |   schema:version                                                                                                                                                                                                                                                                      |


## Identifier

The Identifier class is a critical aspect of the Business Core Vocabulary.
As noted in section 3.1.12, it is also important in many data sets about individuals.
In these cases and more, the identifier itself will be some sort of alpha-numeric string but that string only has meaning if it is contextualised.
In the case of Legal Entities, the issuing of an identifier is a signal that legal entity status has been conferred on an organisation and it's important to know:
- the issuing agency;
- the date on which it was issued;
- the type of identifier issued (if the authority issues more than one type of identifier).
In general, identifiers are issued according to some sort of scheme and those schemes themselves may evolve over time and have version numbers.
Section 5.8 of the UN/CEFACT Core Components Data Type Catalogue Version 3.1 defines a complex data type of Identifier with the following properties:
- content
- scheme identifier
- scheme identifier version
- scheme identifier agency
In terms of the conceptual model for the Core Vocabularies, we can interpret these as follows:

|   Conceptual Model      |   RDF term used
|-------------------------|---------------------------------------|
|   identifier            |   content                             |
|   identifier type       |   scheme identifier                   |
|   date of issue         |   N/A                                 |
|   issuing authority     |   scheme identifier agency            |
|   issuing authority URI |   N/A                                 |
|   N/A                   |   scheme identifier version           |

The Identifier data type is used in ADMS [ADMS] (which was developed in parallel to the Core Vocabularies) to record identifiers for semantic assets. This class is re-used for the Core Vocabularies as described below.


### XML Representation

In an XML representation, the following snippet illustrates the use of the legal identifier. It is recommended to use URIs to encode the identifier type, and issuing authority ID.

```
<LegalIdentifierCvidentifier>
  <Identifier>String</Identifier>
  <IdentifierType>String</IdentifierType>
  <cbc:IssueDate>1967-08-13</cbc:IssueDate>
  <IssuingAuthority>String</IssuingAuthority>
  <IssuingAuthorityID>normalizedString</IssuingAuthorityID>
</LegalIdentifierCvidentifier>
```


### RDF Representation

Taking the RDF Schema for ADMS [ADMSRDF] as a guide, the Identifier data type should be used as follows:

- QName: adms: Identifier
- URI: http://www.w3.org/ns/adms#Identifier
- identifier: use skos:notation to provide the actual identifier (the Identifier class is effectively meaningless without this property and conceptually it is mandatory)
- identifier type: use dcterms:type to provide an identifier for the type of identifier issued (the identifier scheme)
- date of issue: use dcterms:created
- issuing authority: use adms:schemeAgency
- issuing authority: use dcterms:creator

If required, adms:schemeVersion can be used to identify the version of the identifier scheme.



