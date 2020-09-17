# Phase 7: Create distributions and publish documentation
![Process_Phase 7](img/methodology_phase7.PNG)

**Quick links:**
- [Step 26. Decide on the conformance requirements and develop a conformance statement](phase7.md#step-26-decide-on-the-conformance-requirements-and-develop-a-conformance-statement)
- [Step 27. Create distributions](phase7.md#step-27-create-distributions)
- [Step 28. Publish all documentation](phase7.md#step-28-publish-all-documentation)

**Navigate to the different phases**\
[:arrow_left: Previous phase](phase6.md) 

## `Step 26`. Decide on the conformance requirements and develop a conformance statement 

**Key activities**
> * The [<b>editors</b>](../stakeholders#editors) write a conformance statement.
> * The [<b>Working Group members</b>](../stakeholders#working-group) agree on the conformance statement.


<details>
  <summary><b>Description</b></summary>
  
  A conformance statement declares a minimum set of requirements that an implementation must adhere to, in order to be considered conformant with the respective data model.
  The Working Group members must agree on these conformance requirements. The editor then includes a conformance statement in the common data model.
  
  It is possible that the model has natural divisions so that it might be appropriate to set different conformance levels.
  For example, a model used to describe vehicles may have a group of terms related specifically to motor vehicles that could be used in an implementation that has no needs to understand the terms that relate to bicycles.
  This will consequently lead to the establishment of different conformance levels.

</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
  * Publish the conformance statement together with the common data model.
</details>



## `Step 27`. Create distributions

**Key activities**
> * The [<b>editors</b>](../stakeholders#editors) create the required distributions for the data model.

<details>
  <summary><b>Description</b></summary>
  The data model can be expressed (or serialized) in various formats depending on the specific needs and context. Each distribution (format) will have its own uses and advantages, but also its own disadvantages and limitations. 
  
  Semantic data models can, among others, be expressed in TTL (turtle), RDF/XML, JSON-LD, SHACL, etc. Special care needs to be taken when using multiple formats, as converting between them might not always be without difficulties.
  
  Aside from these machine-readable formats, human-readable formats also need to be created. A visual representation of the entities, attributes and relationships of the data model is always recommended to give a clear overview. This can for example be a UML-diagram, saved as a PNG-file.
  Next to this, human-readable documentation is required with all the necessary information to construct the data models, i.e. the entities and attributes with their definitions, cardinalities, proposed codelists, etc. This can for example be distributed as an HTML-page or a PDF-document.
  
  All these distributions can either be manually created, or automatically via one or multiple tools.
  
  During this step, URIs are also created (or reused when possible) for the data model itself, its entities and their attributes. These identifiers need to be minted and maintained by a (European Commission) service.
  
  Required codelists that do not exist yet, need to be created by e.g. the Publications Office, as part of the EU Vocabularies and serialized as SKOS/RDF and/or XML for example.
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
* Create both machine-readable as well as human-readable distributions of the data models.
* Automate the creation of the distributions as much as possible in order to avoid mistakes.
* We recommend to use URIs under the data.europa.eu which allows for flexibility for where the URIs resolve to.
</details>

<details>
  <summary><b>Tool(s)</b></summary>
  
  * [VocBench3](https://ec.europa.eu/isa2/solutions/vocbench3_en)
  * Toolchain [?]
  * Sparx Enterprise Architect
</details>

<details>
  <summary><b>Example(s)</b></summary>

For instance, the Birth evidence was distributed in [XML](../data_model/birth_certificate_XML_example_v0.01.xml). 
</details>

## `Step 28`. Publish all documentation

**Key activities**
> * The [<b>editors</b>](../stakeholders#editors) publish all documentation on the collaborative tool.

<details>
  <summary><b>Description</b></summary>
  
  The editors publish the final version of the data model, in both machine-readable and human-readable format, on the collaborative tool selected. 
  If possible, the editors should publish the data model as open (meta)data and specify which license is applicable.
  
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
  * Choose an open license, e.g. CC0.
  * Publish the data model, its elements and related documentation via persistent (and ideally, dereferenceable) URIs.
  * Provide machine access to the data model.
</details>

<details>
  <summary><b>Tool(s)</b></summary>
  <i>The collaborative tool, e.g. Confluence, Github.</i>
</details>

