# Manifest

> :warning: **Disclaimer**: Note that this `manifest` is a draft attempt at having a generic data model catering for all evidence types. The name `manifest` has not yet been formally agreed. Sources used to developed the `manifest` are [TOOP Document Response](http://wiki.ds.unipi.gr/display/TOOP/TOOP+Response+Syntax+Mapping#TOOPResponseSyntaxMapping-DocumentResponse) and [CCCEV](https://joinup.ec.europa.eu/collection/semantic-interoperability-community-semic/solution/core-criterion-and-core-evidence-vocabulary)

## Mafinest
Definition: A list of context-neutral attributes being common to all evidence types. 

|     expected type    |     definition                                                                                                                           |     cardinality    |     code list    |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------|------------------|
|     Code             |     The nature of the   – structured or unstructured – document exchanged to prove facts or   compliance with procedural requirements    |     [1..1]         |     TBD          |
|     Code             |     Whether the data   is structured or unstructured                                                                                     |     [1..1]         |     TBD          |
|     Identifier       |     An unambiguous   reference to the Manifest                                                                                           |     [0..*]         |     N/A          |
|     Date             |     The date on which   the Manifest was issued.                                                                                         |     [1..1]         |     N/A          |
|     Organisation     |     An Organisation   with official authority in charge of issuing the Manifest.                                                         |     [1..1]         |     N/A          |
|     URI              |     Scheme that   describes the structure of the data                                                                                    |     [0..1]         |     N/A          |

## Organisation

Definition: Any organisation that is defined as being part of the public sector by a legal framework at any level.

Source: [ISA² Core Public Organisation Vocabulary](https://joinup.ec.europa.eu/release/core-public-organisation-vocabulary-v100)

|     attribute     |     expected type    |     definition                                                                                                                                                                                                                                                                                                                                                                                      |     cardinality    |     code list    |
|-------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|------------------|
|     name          |     Text             |     An Organisation has   a name by which it is referred to                                                                                                                                                                                                                                                                                                                                         |     [1..*]         |     N/A          |
|     identifier    |     Identifier       |     Many   organisations are referred to by an acronym or some other identifier. For   example, among the EU institutions, the ECB is the identifier for the   European Central Bank, OLAF for the European Anti-Fraud Office, and so on.   These are formally recognised by the European Commission which provides a   list of such acronyms. Analogous lists should be used in other contexts.    |     [0..*]         |     N/A          |