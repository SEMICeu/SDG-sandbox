![in progress](https://img.shields.io/badge/status-in%20progress-yellow)

# Phase 1: Identify and analyse existing standardisation efforts, evidences and data models
![Process_Phase 1](img/methodology_phase1.PNG)

**Quick links:**
- [`Step 1` Identify and share existing models and standardisation efforts](#step-1-Identify-and-share-existing-models-and-standardisation-efforts)
- [`Step 2` Identify and share entities, attributes and descriptions used in national implementations](#step-2-Identify-and-share-entities,-attributes-and-descriptions-used-in-national-implementations)
- [`Step 3` Identify and analyse models used or standardisation efforts (elsewhere)](#step-3-Identify-and-analyse-models-used-or-standardisation-efforts-(elsewhere))


**Navigate to the different phases**\
[:arrow_left: Previous phase](README.md) **|**
[Next phase :arrow_right:](phase2.md)

## `Step 1` Identify and share existing models and standardisation efforts
<i><b>Business analysis</b> - identification of business needs and related solutions.</i>

**Key activities**
> * The [<b>Working Group members</b>](../stakeholders#working-group) and [<b>domain experts</b>](../stakeholders#domain-experts) identify and share existing models, standardisation efforts or policies. 
> * The [<b>responsible DG</b>](https://ec.europa.eu/info/departments_en) in line with the evidence being modelled share existing models, standardisation efforts or policies.
> * The [<b>Editors</b>](../stakeholders#editors) collect information from the Working Group members and the responsible DG.

<details>
  <summary><b>Description</b></summary>
  
Working Group members will share information they possess related to the OOTS data model for specific evidence types being built. Similarly, DGs with competencies in relation to the scope of the evidence being modelled, will share relevant information and existing legal pieces of work (and/or other relevant pieces of work)

The objective is to gather information in order to have a global overview of data models, and/or standardisation rules implemented and used across Europe and leverage this insight to develop a OOTS data model for specific evidence types. 

This step is specifically interested in information available at global, i.e. European level, rather than at national level, which is the scope of step 2. 

</details>


<details>
  <summary><b>Rules and Guidelines</b></summary>
  
One important aspect of this step is ensuring data quality. This is ensured by the requirement that all data come from authoritative sources. Working Group members are responsible for identifying and contacting the authorities that hold the relevant information. In addition, reusing content based on intrinsic licenses may necessitate the use of a specific license for the model being developed.

</details>


<details>
  <summary><b>Tool(s)</b></summary>

A collaborative tool, e.g. Confluence, GitHub.

</details>


<details>
  <summary><b>Example(s)</b></summary>
  
For example, for social security, [EESSI (Electronic Exchange of Social Security Information)](https://ec.europa.eu/social/main.jsp?catId=869&langId=en) is an IT system already in place. For education related matters, [Europass](https://ec.europa.eu/social/main.jsp?catId=1266&langId=en), from DG EMPL, is in place. 

</details>

## `Step 2` Identify and share entities, attributes and descriptions used in national implementations
<i><b>Technical analysis</b> - identification of technical requirements and related solutions.</i>

**Key activities**
> * The [<b>Working Group members</b>](../stakeholders#working-group) share existing national data models or examples of evidences.
> * The [<b>Working Group members</b>](../stakeholders#working-group) contact relevant [<b>domain experts</b>](../stakeholders#domain-experts) in order to identify and report features describing data models used in national implementations.
> * The [<b>Editors</b>](../stakeholders#editors) collect information from the Working Group members.

<details>
  <summary><b>Description</b></summary>
  
Step 2 is about the national implementation of data models or legislative pieces. Contrary to step 1, step 2 is looking at gathering elements from national contexts. 

It is possible that relevant data models (semantic or other) do not exist or were not shared in step 1. Step 2 will remediate this by gathering relevant elements from national implementations.

Working Group members will share information on:
* Examples of evidences
* Entities they judge paramount for the OOTS data model for specific evidence types being built
 - Attributes they judge mandatory and optional;
 - Descriptions of elements in their national implementations.

Before sending any data, the Working Group members should consider the following:
* Has the data model been validated and implemented by a competent authority?
* Has the data model been issued in a final version?

  
</details>

<details>
  <summary><b>Tool(s)</b></summary>
  
A spreadsheet can be used to present and compare the different data models. 

</details>

<details>
  <summary><b>Example(s)</b></summary>
  
The table below illustrates how SKOS mapping properties can be used to compare models. 

|     Italy data model    |     Spain data model    |     SKOS mapping   value    |
|-------------------------|-------------------------|-----------------------------|
|     Person              |     Person              |     exact match             |
|     Birth               |                         |     no match                |

If provided, the table can also include definitions and URIs to ease comparison.

Example of an implementation (Person Condition Register and Registration Register) shared by Germany: see [issue #89](https://github.com/SEMICeu/SDG-sandbox/issues/89).
Example of a data model shared by Spain: [issue #37](https://github.com/SEMICeu/SDG-sandbox/issues/37#issue-664501128).

</details>



## `Step 3` Identify and analyse models used or standardisation efforts (elsewhere)
<i><b>Business analysis</b> - identification of business needs and related solutions.</i>


**Key activities**
> The [<b>Editors</b>](../stakeholders#editors) analyse European and global initiatives to standardise the exchange of information.


<details>
  <summary><b>Description</b></summary>
  
In parallel with steps 1 and 2, the Editors document the information received and any European and/or global initiatives that aim at standardising data exchanges between Member States. The output of this step will serve as a basis for drafting the OOTS data model for specific evidence types.

Step 1 and 2 are the source of information for step 3. While Working Group members and competent DGs gather information, the editors will focus on documenting and analysing the information received. Editors should also do a research effort to not exclude any relevant data model and standardization effort used elsewhere. 

This step supplements part of step 2, concerns existing harmonisation of information contained in the evidences at European level. The editors may reuse the necessary elements from these initiatives. 

</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
Reusing content based on intrinsic licenses may necessitate the use of a specific license for the model being developed.

</details>

<details>
  <summary><b>Tool(s)</b></summary>
  
Below are some links of input sources. 

* [Study on Data Mapping for the cross-border application of the Once-Only technical system SDG](https://sdg.mindigital.gr/uploads/Deloitte_final_report.pdf)
* [Linked Open Vocabularies](https://lov.linkeddata.es/dataset/lov)
* [Core Vocabularies](https://ec.europa.eu/isa2/solutions/core-vocabularies_en)
* [Euro Vocabularies](https://op.europa.eu/en/web/eu-vocabularies/home)
* [Ontology design patterns](http://ontologydesignpatterns.org/wiki/Main_Page)
* [eProcurement ontology](https://joinup.ec.europa.eu/collection/eprocurement/solution/eprocurement-ontology) 
* [Public Documents forms | DG Justice](https://beta.e-justice.europa.eu/35981/EN/public_documents_forms)

</details>

<details>
  <summary><b>Example(s)</b></summary>

The Core Person Vocabulary can be used when modelling data related to people.

</details>
