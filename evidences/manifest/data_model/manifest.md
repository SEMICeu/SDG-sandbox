# Manifest

> :warning: **Disclaimer**: Note that this `manifest` is a draft attempt at having a generic data model catering for the provision of all evidence types. The name `manifest` has not yet been formally agreed. Sources used to develop the `manifest` are [TOOP Document Response](http://wiki.ds.unipi.gr/display/TOOP/TOOP+Response+Syntax+Mapping#TOOPResponseSyntaxMapping-DocumentResponse) and [CCCEV](https://joinup.ec.europa.eu/collection/semantic-interoperability-community-semic/solution/core-criterion-and-core-evidence-vocabulary)

## Manifest
Definition: A list of context-neutral attributes being common to all evidence types. 

|     attribute            |     expected type    |     definition                                                                                                                           |     cardinality    |     code list    |
|--------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------|------------------|
|     evidence type        |     Code             |     The nature of the   – structured or unstructured – document exchanged to prove facts or   compliance with procedural requirements    |     [1..1]         |     TBD          |
|     format               |     Code             |     The type of encoding of the data, for example PDF, XML                                                                               |     [1..1]         |     TBD          |
|     identifier           |     Identifier       |     An unambiguous   reference to the Manifest                                                                                           |     [1..1]         |     N/A          |
|     issuing date         |     DateTime         | 	The date (and, optionally, time) on which the evidence was issued                                                                        |     [1..1]         |     N/A          |
|     issuing authority    |     Organisation     |     An Organisation with official authority in charge of issuing the evidence                                                         |     [1..1]         |     N/A          |
|     language               |     Code              |     The language in which the Evidence is issued                                                          |     [0..1]         |     [Language](http://publications.europa.eu/resource/authority/language)         |
|     schema               |     URI              |     Link to the specification of the structure of the data, for example an XSD                                                           |     [0..1]         |     N/A          |

## Organisation
**Definition**: Represents a collection of people organised together into a community or other social, commercial or political structure. The group has some common purpose or reason for existence which goes beyond the set of people belonging to it and can act as an Agent. Organisations are often decomposable into hierarchical structures.

**Source**: [The Organization Ontology](https://www.w3.org/TR/vocab-org/)

|     attribute           |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                |    cardinality     | code list | 
|-------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     preferred label     |     [Text](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#text)           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                            |    [1..*]          |  N/A      | 
|     identifier          |     [Identifier](https://github.com/SEMICeu/SDG-sandbox/blob/master/technical_documentation/data_types.md#identifier)     |     Many organisations are referred to by some identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.        |    [0..*]          |  N/A      | 

