![in progress](https://img.shields.io/badge/status-in%20progress-yellow)

# Phase 5: Finalise data model
![Process_Phase 5](img/methodology_phase5.PNG)

**Quick links:**
- [` Step 22`  Review the final data model](../phase5.md#step-22-Review-the-final-data-model)
- [` Step 23`  Update the final data model](../phase5.md#step-23-Update-the-final-model)

**Navigate to the different phases**\
[:arrow_left: Previous phase](phase4.md) **|**
[Next phase :arrow_right:](phase6.md)

## ` Step 22`  Review the final data model 
<i><b>Review</b> - formal assessment potentially leading to changes.</i>

**Key activities**
> * The [<b>Working Group members</b>](../stakeholders#working-group) and the [<b>domain experts</b>](../stakeholders#domain-experts) review the final data model.
> * The [<b>Editors</b>](../stakeholders#editors) assist the Working Group members, collect and categorise the feedback. 

<details>
  <summary><b>Description</b></summary>
  
Working Group members discuss and validate the data model with the business, domain experts and share their questions and / or remarks, if any, with the editors via the adequate channel.

In parallel, the Editors collect and, again, categorise the feedback. For instance:

* Editorial issue
* Minor issue
* Major issue 

This step is also important to set the final agreement on cardinalities. To help with that, the Editors have the possibility to propose editable tables. The sole purpose of the tables is for the Working Group members to indicate whether they are in capacity to provide the attributeslisted in the data model. But also whether a specific attribute is needed to process the evidence.

Ideally, the tables should be composed of the following columns:

* Entity
* Attribute
* Description
* Cardinality
* Country abbreviation 
 - multiple columns allowing Working Group members to specify whether an Attribute can be provided (Y) or not (N))
 - multiple columns allowing Working Group members to specify whether an Attribute is needed (Y) or not (N))

By no means the tables will replace the collaborative tool selected. The latter will still be home to the data model and a place to discuss the latter. The tables are a way to collect input on whether an attribute can be provided or not in a structured manner. In case further information is necessary to provide an answer, whether an attribute can be provided or not, the Working Group members have to be redirected to the collaborative tool selected.

Ultimately, the Working Group members have to come to a semantic agreement with regards to the data model reviewed. Unless there are major semantic changes, this step should be considered as a formal approval from the Working Group members for the data model.
  
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
Aspects to bear in mind while reviewing:
  
* Data elements and entity names
* Model appearance
* Rules of normalization
* Definitions
* Model flexibility

Questions to bear in mind while reviewing: 

* Do I agree with the proposed controlled vocabularies?
* Do I agree with the proposed changes to the data model? 
* Are the entities and attributes definitions clear enough? 
* Does the modelling approach make sense? 
* Do I agree with the proposed cardinalities (i.e. mandatory versus optional)
* With data minimisation in mind, should some of the entities and or attributes be stripped off?
* Will my country be able to provide all the mandatory information? 
* What information does my country need to process the evidence?  
</details>
<details>
  <summary><b>Example(s)</b></summary>
  'Editable table' as described further above: 

| 				 |     Attribute                  | Description | Cardinality | AT | BE | BG | HR | CY | CZ | DK | EE | FI | FR | DE | EL | HU | IS | IE | IT | LV | LI | LT | LU | MT | NL | NO | PL | PT | RO | SK | SI | ES | SE |
|----------------|--------------------------------|-------------|-------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| Birth Evidence |                                |             |             |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
|                | BirthEvidence.identifier       |    [Link]   | [1..1]      |    |    |    |    | Υ  |    |    | Y  |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Y  |    | Y  |    |    |    | Y  | Y  |
|                | BirthEvidence.issuingDate      |    [Link]   | [1..1]      |    |    |    |    | Υ  |    |    | Y  |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Y  |    | Y  |    |    |    | Y  | Y  |
|                | BirthEvidence.certifies        |    [Link]   | [1..1]      |    |    |    |    | Υ  |    |    | Y  |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Y  |    | Y  |    |    |    | Y  | Y  |
|                | BirthEvidence.issuingAuthority |    [Link]   | [1..1]      |    |    |    |    | Υ  |    |    | Y  |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Y  |    | Y  |    |    |    | Y  | Y  |

</details>



## ` Step 23`  Update the final model
<i><b>Review</b> - formal assessment potentially leading to changes.</i>

**Key activities**
> * The [<b>Editors</b>](../stakeholders#editors) process any last feedback and finish the final model. 

<details>
  <summary><b>Description</b></summary>
  
As the Working Group members have given feedback in the previous step, the Editors process these comments and make changes to the data modelas agreed with the Working Group members. From this point, the Editors can only make changes for which the Working Group members have reached a consensus. Since there is no review period anymore, all changes that are carried out during this step should have been discussed with the Working Group members.
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
 * No changes are made during this step that were not agreed upon by the Working Group.
 - The change log is updated to reflect the final changes in order to achieve full transparency towards the Working Group.
</details>

