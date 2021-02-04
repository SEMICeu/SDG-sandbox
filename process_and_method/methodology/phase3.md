![in progress](https://img.shields.io/badge/status-in%20progress-yellow)

# Phase 3: Select controlled vocabularies
![Process_Phase 3](img/methodology_phase3.PNG)

**Quick links:**
- [`Step 10` Identify and propose controlled vocabularies across the model](../phase3.md#step-10-Identify-and-propose-controlled-vocabularies-across-the-model)
- [`Step 11` Choose recommended controlled vocabularies](../phase3.md#step-11-Choose-recommended-controlled-vocabularies)
- [`Step 12` Create controlled vocabularies](../phase3.md#step-12-Create-controlled-vocabularies)
- [`Step 13` Harmonise controlled vocabularies across the data model](../phase3.md#step-13-Harmonise-controlled-vocabularies-across-the-data-model)
- [`Step 14` Document core set of attributes and recommended vocabularies](../phase3.md#step-14-Document-core-set-of-attributes-and-recommended-vocabularies)



**Navigate to the different phases**\
[:arrow_left: Previous phase](phase2.md) **|**
[Next phase :arrow_right:](phase4.md)

## `Step 10` Identify and propose controlled vocabularies across the model
<i><b>Technical analysis</b> - identification of technical requirements and related solutions.</i>

**Key activities**
> * The [<b>Working Group members</b>](../stakeholders#working-group) and the [<b>domain experts</b>](../stakeholders#domain-experts) propose controlled vocabularies for the different attributes defined in the previous phases.
> * The [<b>Editors</b>](../stakeholders#editors) synthesise the propositions and complement with additional standard controlled vocabularies where relevant.

<details>
  <summary><b>Description</b></summary>
  
Once a core set of common attributes has been agreed upon and the draft data model is stable enough, the set of controlled vocabularies, for those attributes where a controlled vocabulary is needed, needs to be analysed. 

The editors create a table with the common attributes along one dimension and the local implementations along the other dimension, placing the controlled vocabularies suggested in the cells. Along with the controlled vocabularies, the Working Group is tasked to propose usage notes for all the attributes agreed upon.

</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>

* Controlled vocabularies at the EU level are multilingual which helps in cross- border data exchange scenarios.
* (domain-specific) Controlled vocabularies which are internationally accepted should be considered. 
* Controlled vocabularies should have governance processes in place, be hosted in a sustainable manner and be provided free of charge.

</details>

<details>
  <summary><b>Tool(s)</b></summary>

* [EU Vocabularies](https://op.europa.eu/en/web/eu-vocabularies/controlled-vocabularies)
* [Core Public Service Application Profile](https://joinup.ec.europa.eu/collection/semantic-interoperability-community-semic/solution/core-public-service-vocabulary-application-profile)

</details>

<details>
  <summary><b>Example(s)</b></summary>
  
For instance, for the [gender attribute](https://github.com/SEMICeu/SDG-sandbox/issues/143) the [Human Sex](https://op.europa.eu/en/web/eu-vocabularies/at-concept-scheme/-/resource/authority/human-sex/?target=Browse&uri=http://publications.europa.eu/resource/authority/human-sex) controlled vocabulary has been identified and proposed.n. 
  
</details>

## `Step 11` Choose recommended controlled vocabularies
<i><b>Technical analysis</b> - identification of technical requirements and related solutions.</i>

**Key activities**
> * The [<b>Editors</b>](../stakeholders#editors) put forward the different propositions for each attribute working towards a decision.
> * The [<b>Working Group members</b>](../stakeholders#working-group) and the [<b>domain experts</b>](../stakeholders#domain-experts) discuss - through the collaborative tool - and select the controlled vocabularies.

<details>
  <summary><b>Description</b></summary>
  
 Based on the table of controlled vocabularies, the Working Group members discuss which controlled vocabularies are the most appropriate to be recommended as well as the soundness of the proposed usage notes. This may be based on the status of particular vocabularies (e.g. if they are based on an international standard) or on their usage across multiple implementations.

In the case of divergent views, a live discussion may be organised by the Editors and the moderator to agree on the most controversial proposed solutions.

  
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
It is important to agree on common official controlled vocabularies that can harmonise across different countries the way in which specific values of properties can be specified, allowing for a uniform indexing and retrieving of data based on common terms. 

</details>

<details>
  <summary><b>Example(s)</b></summary>

As suggested by the Working Group, the editors have used the [language code list](http://publications.europa.eu/resource/authority/language) as controlled vocabulary for the language attribute of all tertiary education related evidences ([see issue #120](https://github.com/SEMICeu/SDG-sandbox/issues/120)). 

</details>

## `Step 12` Create controlled vocabularies
<i><b>Technical analysis</b> - identification of technical requirements and related solutions.</i>

**Key activities**
> * The [<b>Editors</b>](../stakeholders#editors) create a proposition of new controlled vocabularies.
> * The [<b>Working Group members</b>](../stakeholders#working-group) review the proposition and provide comments.
> * The [<b>Publication Office</b>](../stakeholders#publication-office)The Publications Office creates controlled vocabularies.

<details>
  <summary><b>Description</b></summary>
  
 In the event of no controlled vocabularies being available, the Editors (or Working Group members) have the opportunity to propose the creation of controlled vocabularies. Required controlled vocabularies, that do not exist yet, need to be created by the Publications Office, as part of the EU Vocabularies. Of course, existing controlled vocabularies can be updated, if necessary.  


</details>


<details>
  <summary><b>Tool(s)</b></summary>

* [The Publication Office](https://op.europa.eu/en/web/eu-vocabularies/controlled-vocabularies)
</details>

</details>

## `Step 13` Harmonise controlled vocabularies across the data model
<i><b>Technical analysis</b> - identification of technical requirements and related solutions.</i>

**Key activities**
> The [<b>Editors</b>](../stakeholders#editors) harmonise the controlled vocabularies and usage notes across the data model while ensuring the alignment between data models.


<details>
  <summary><b>Description</b></summary>
  
The Editors consider all controlled vocabularies and usage notes across the data model - and across all SDG data models - , check their consistency and identify any overlaps or gaps. 
Editors may propose changes to the recommendations, for example if different controlled vocabularies have been recommended for identical or similar attributes.
Editors may also propose slight changes to the usage notes, for example to harmonise the writing style across the model or solve inconsistencies.

</details>

## `Step 14` Document core set of attributes and recommended vocabularies
<i><b>Technical analysis</b> - identification of technical requirements and related solutions.</i>

**Key activities**
> The [<b>Editors</b>](../stakeholders#editors) document the consensus and construct the working draft.

<details>
  <summary><b>Description</b></summary>
  
On the basis of discussions in phase 3 and phase 4, the editors will document the decisions and prepare to update the draft data model.

</details>
