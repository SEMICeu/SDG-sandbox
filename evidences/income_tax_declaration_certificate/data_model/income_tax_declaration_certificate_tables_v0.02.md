# Disclaimer

This page relates to [version (v0.12)](income_tax_declaration_certificate_diagram_v0.12.png) of the model. 

---

# Income Tax Declaration Evidence

## Entities

### Income Tax Declaration Evidence
**Definition**: Official document in which a Tax Payer declares the Monetary Amount that he or she has earned and the income taxes that he or she has paid in one fiscal year.

|     attribute            |     expected type          |     definition                                                                                                                                             |     cardinality    | code list |
|--------------------------|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------|
|     identifier           |     Identifier             |     An unambiguous reference to the Income Tax Declaration Evidence.                                                                                       |     [0..1]         | N/A       |
|     issuing date         |     Date                   |     The date on which the Income Tax Declaration was issued.                                                                                               |     [1..1]         | N/A       |
|     fiscal year          |     Date                   |     Reference year for which the Income Tax is due.                                                                                                        |     [1..1]         | N/A       |
|     belongs to           |     Tax Payer              |     The Tax Payer to whom the Tax Declaration applies.                                                                                                     |     [1..1]         | N/A       |
|     issuing authority    |     Public Organisation    |     The National Competent Authority which is in charge of issuing the Income Tax Declaration.                                                             |     [1..1]         | N/A       |
|     total income         |     Monetary Amount        |     The total amount of taxable income of the Tax Payer in the respective year.                                                                            |     [1..1]         | N/A       |
|     income tax           |     Monetary Amount        |     The total amount (positive or negative) of tax due on the income in the respective year.                                                               |     [0..1]         | N/A       |


### Monetary Amount
**Definition**: A monetary value.

|     attribute            |     expected type          |     definition                                                                                          |     cardinality    | code list                                                                                      |
|--------------------------|----------------------------|---------------------------------------------------------------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------|
|     currency             |     Code                   |     The currency in which the Monetary Amount is expressed.                                             |     [1..1]         | [Currency](https://op.europa.eu/en/web/eu-vocabularies/at-dataset/-/resource/dataset/currency) |
|     amount               |     Float                  |     The quantitative value of the Monetary Amount.                                                      |     [1..1]         | N/A                                                                                            |


### Tax Payer
**Definition**: A Person subject to pay an income tax.

**Subclass of**: Person

|     attribute              |     expected type |     definition                                                          |     cardinality    | code list | 
|----------------------------|-------------------|-------------------------------------------------------------------------|--------------------|-----------|
|     national fiscal number |     Identifier    |     An unambiguous reference to the Tax Payer.                          |     [1..1]         | N/A       | 
|     domicile               |     Location      |     A Person's fixed, permanent and principal home for legal purposes.  |     [0..1]         | N/A       |


### Person
**Definition**: An individual person who may be dead or alive, but not imaginary.

|     attribute           |     expected type |     definition                                                                                                                                                                                                                                                                                                                                                                                                                               |     cardinality   | code list |
|-------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------|
|     identifier          |     Identifier    |     The identifier relation is used to link a Person to any formally issued Identifier for that Person.                                                                                                                                                                                                                                                                                                                                      |     [1..*]        | N/A       |
|     given name          |     Text          |     A given name, or multiple given names, are the denominator(s) that identify an individual within a family. These are given to a Person by his or her parents at birth or may be legally recognised as 'given names' through a formal process. All given names are ordered in one field so that, for example, the given name for Johan Sebastian Bach is “Johan Sebastian”.                                                               |     [1..1]        | N/A       |
|     family name         |     Text          |     A family name is usually shared by members of a family. This attribute also carries prefixes or suffixes which are part of the family name, e.g. “de Boer”, “van de Putte”, “von und zu Orlow”. Multiple family names, such as are commonly found in Hispanic countries, are recorded in the single family name field so that, for example, Miguel de Cervantes Saavedra's family name would be recorded as "de Cervantes Saavedra".     |     [1..1]        | N/A       |


### Public Organisation
**Definition**: Any organisation that is defined as being part of the public sector by a legal framework at any level.

|     attribute        |     expected type  |     definition                                                                                                                                                                                                                                                                                                                                                                                       |    cardinality     | code list |
|----------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------| 
|     preferred label  |     Text           |     As defined in the ORG Ontology, a preferred label is used to provide the primary, legally recognised name of the organisation. An organisation may only have one such name in any given language. Primary names may be provided in multiple languages with multiple instances of the preferred label property.                                                                                   |    [1..*]          | N/A       |
|     identifier       |     Identifier     |     Many organisations are referred to by an acronym or some other identifier. For example, among the EU institutions, the ECB is the identifier for the European Central Bank, OLAF for the European Anti-Fraud Office, and so on. These are formally recognised by the European Commission which provides a list of such acronyms. Analogous lists should be used in other contexts.               |    [1..*]          | N/A       |


### Location
**Definition**: A spatial region or named place.

|     attribute   |     expected type  |     definition                                                                                  |     cardinality    | code list |
|-----------------|--------------------|-------------------------------------------------------------------------------------------------|--------------------|-----------|
|     address     |     Address        |     The address property relationship associates a Location with the Address entity.            |     [1..1]         | N/A       |


### Address
**Definition**: An "address representation" as conceptually defined by the INSPIRE Address Representation data type.

|     attribute           |     expected type |     definition                                                               |     cardinality    | code list |
|-------------------------|-------------------|------------------------------------------------------------------------------|--------------------|-----------|
|     full address        |     Text          |     The complete address written as a string, with or without formatting.    |     [1..1]         | N/A       |

