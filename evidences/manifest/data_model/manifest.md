# Manifest

> :warning: **Disclaimer**: Note that this `manifest` is a draft attempt at having a generic data model catering for the provision of all evidence types. The name `manifest` has not yet been formally agreed. Sources used to develop the `manifest` are [TOOP Document Response](http://wiki.ds.unipi.gr/display/TOOP/TOOP+Response+Syntax+Mapping#TOOPResponseSyntaxMapping-DocumentResponse) and [CCCEV](https://joinup.ec.europa.eu/collection/semantic-interoperability-community-semic/solution/core-criterion-and-core-evidence-vocabulary)

## Manifest
Definition: A list of context-neutral attributes being common to all evidence types. 

|     attribute            |     expected type    |     definition                                                                                                                           |     cardinality    |     code list    |
|--------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------|------------------|
|     evidence type        |     Code             |     The nature of the   – structured or unstructured – document exchanged to prove facts or   compliance with procedural requirements    |     [1..1]         |     TBD          |
|     format               |     Code             |     The type of encoding of the data, for example PDF, XML                                                                               |     [1..1]         |     TBD          |
|     identifier           |     Identifier       |     An unambiguous   reference to the Manifest                                                                                           |     [0..*]         |     N/A          |
|     Issuing date         |     DateTime         | 	The date (and, optionally, time) on which the evidence was issued                                                                        |     [1..1]         |     N/A          |
|     issuing authority    |     Organisation     |     An Organisation with official authority in charge of issuing the evidence                                                         |     [1..1]         |     N/A          |
|     schema               |     URI              |     Link to the specification of the structure of the data, for example an XSD                                                           |     [0..1]         |     N/A          |

## Organisation

Definition: Any organisation that is defined as being part of the public sector by a legal framework at any level.

Source: [ISA² Core Public Organisation Vocabulary](https://joinup.ec.europa.eu/release/core-public-organisation-vocabulary-v100)

|     attribute     |     expected type    |     definition                                                                                                                                                                                                                                                                                                                                                                                      |     cardinality    |     code list    |
|-------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|------------------|
|     name          |     Text             |     An Organisation has   a name by which it is referred to                                                                                                                                                                                                                                                                                                                                         |     [1..*]         |     N/A          |
|     identifier    |     Identifier       |     Many   organisations are referred to by an acronym or some other identifier. For   example, among the EU institutions, the ECB is the identifier for the   European Central Bank, OLAF for the European Anti-Fraud Office, and so on.   These are formally recognised by the European Commission which provides a   list of such acronyms. Analogous lists should be used in other contexts    |     [0..*]         |     N/A          |

