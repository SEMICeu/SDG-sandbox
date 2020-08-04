![in progress](https://img.shields.io/badge/status-in%20progress-yellow)


# Phase 4: Review data model and incorporate comments
![Process_Phase 4](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/resources/20200713_WP4_methodology_Phase4_v0.03.jpg)

**Quick links:**
- [`Step 13`. Review draft data model](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase4.md#step-13-review-draft-data-model)
- [`Step 14`. Proposition enhancements](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase4.md#step-14-proposition-enhancements)
- [`Step 15`. Propose additional attributes](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase4.md#step-15-propose-additional-attributes)
- [`Step 16`. Perform semantic mapping of attributes](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase4.md#step-16-perform-semantic-mapping-of-attributes)
- [`Step 17`. Harmonise, entities, attributes and descriptions across the data model](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase4.md#step-17-harmonise-entities-attributes-and-descriptions-across-the-data-model)
- [`Step 18`. Update draft data model](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase4.md#step-18-update-draft-data-model)

**Navigate to the different phases**\
[:arrow_left: Previous phase](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase3.md) **|**
[Next phase :arrow_right:](https://github.com/barthelemyf/SDG-sandbox/blob/master/process_and_method/methodology/phase5.md)

## ` Step 13` . Review draft data model

**Key activities**

> * The [<b>Working Group members</b>](https://github.com/cbahim/SDG-sandbox/tree/master/process_and_method/stakeholders#working-group) directly review the proposed model and/or contact domain experts for reviewing it.
> * The [<b>editors</b>](https://github.com/cbahim/SDG-sandbox/tree/master/process_and_method/stakeholders#editors) process the comments received and propose solutions.

<details>
  <summary><b>Description</b></summary>
  
  Each published draft of the Data Model is reviewed by the Working Group and domain experts when relevant. 
  The Working Group and the editors agree on a tool to collaborate and capture the feedback.
  The reviewers create issues in the tool. When comments are received outside of the collaborative tool, the editor creates an issue in the issue tracker for each comment. 

  The editors respond within an agreed timeframe to each issue, informing the reviewer that they have noticed the comment.

  The reviewers are encouraged to propose a solution to their own issue. The editors consolidate the proposed solutions and explain the pros and cons of the different solutions  to the Working Group. If needed, the editors seek for additional contribution from the reviewers in collaboration with the moderator and rapporteur.

  The editors classify the issues and tag major issues which should be commented in priority by the reviewers.

  The moderators make sure that the agreement process is transparent for all reviewers.
  The Working Group must resolve each comment in one of three ways:
  
  * `Accepted`: This usually means that changes will be made that will be reflected in the next draft.
  *	`Rejected`: No changes will be made to the draft.
  *	`Partially accepted`: Some of the comment is accepted but other parts are rejected.

  After consideration of the comment, the editor records the resolution and sends a response to
  the reviewer. To a semantic issue, the response usually includes a summary of the context of the issue, the resolution agreed by the Working Group and the justification for the resolution, particularly in case the issue is rejected.

  The issues can be categorised in different ways. For example:
  *	**`Editorial issues`**
    Bug-fixes such as spaces, typos or small errors within the data models can directly be corrected by the editorial team who presents a summary of all editorial issues in the     next meeting following the correction.

  *	**`Semantic issues`**
    Issues concerning for instance the definitions used, the data type, the name of the entity or the namespace referred. The editors propose a resolution to the issue through the   collaborative tool, asking for further information to the Working Group when necessary. The proposed resolutions are discussed with the Working Group in the next meeting         following the issue creation  or directly via the collaborative tool.

  Semantic issues include the proposition of enhancements to the data model published or the proposition of additional attributes or entities that are not present in the model.  
  For further details about these two types of contribution, please check the dedicated steps.
</details>
<details>
  <summary><b>Rules and guidelines</b></summary>

* Creation of issues: to the maximal extent, contributors should be encouraged to directly create their issues on the collaborative tool.
* Use labelling and tagging for increasing searchability and responsiveness of contributors.
* Consider your audience for deciding how to present and discuss issues:
    * Presentation: technical vs business oriented
    * Voting mechanism: see consensus
* Give some structure or agree on issue naming for increasing comprehension of the issues. For example: 

```diff
+ Name of the data model or sub-part (e.g. relevant entity): | short statement of the issue
! VehicleRegistrationCertificate evidence should contain registration status
```
</details>
<details>
  <summary><b>Tool(s)</b></summary>
  
  Key aspects to consider:
  *	**Proprietary vs open access and licensing:** 
  ```diff
  + Are there licences or other requirements for accessing the tool? 
  ! GitHub: For contributing to a public repository, GitHub asks to create an account with a valid email address.
  + What are the licensing conditions?
  ! GitHub: For public repositories, the administrator can decide which licence applies. GitHub provides guidelines for licensing public repositories. As the content of public repositories is publicly available, the licences proposed are open source.
  + What are the limits of the free version?
  ! Each account created can use 1 GB of storage and 1 GB of monthly bandwidth for free. 
  ```
  *	**Archiving and persistence:** 
  ```diff
  + Who is owning and maintaining the tool? 
  ! GitHub: GitHub, Inc. owned by Microsoft is the organisation owning GitHub.
  + Has the owner engaged to store the content for a certain period? 
  ! GitHub intends to keep public repositories available except if specific conditions are met (such as violation of Terms of Service).
  ```
  *	**User-friendliness and adoption**
  ```diff
  + What is the current level of adoption of the tool?
  ! GitHub: most of the Working Group members are familiar with GitHub.
  + How easily can someone learn the basics?
  ! GitHub: Accessing and creating issues in GitHub is straightforward and well-documented. Additional features can be learnt along the way.
  ```
  *	**Security**
  ```diff
  + Is the content restricted?
  ! GitHub: There are no access restrictions for public repositories. 
  ```
</details>
<details>
  <summary><b>Example(s)</b></summary>
  The following example describes the review of a draft data model followed by the creation of an issue and its processing by the editors and Working Group members.
  
  The process is the following:
  
  1. The editors publish on GitHub under the correct folder the diagram and tables describing the [Vehicle registration certificate](https://github.com/SEMICeu/SDG-sandbox/tree/master/evidences/vehicle_registration_certificate/data_model).
  1. While reviewing the model, a semantic expert or a domain expert will try to answer the following questions:
     * Are all elements necessary for this evidence described in the model?
     * Are there conflicts between the elements of the model and the elements used in your country?
     * Do you agree with the definition of the elements?
     * Is the element mandatory or optional in your country (cardinality)?
     * Do you have specific codes or expected type (e.g. format of date, address etc.) for attributes?
  1. The reviewers document their issues on GitHUB. For example, concerning the vehicle registration certificate, the following issue was created [#45](https://github.com/SEMICeu/SDG-sandbox/issues/45)

  You may notice that the issue describes in practice several comments related to the vehicle registration certificate as well as an image of the data model used within the country. 
  
  To simplify the contribution of other reviewers to this issue, the editors will analyse the proposition, categorise it with labels, verify whether the issue should be restructured and describe the pros and cons of the issue documented. In our example, each bullet point from the general comments should represent a separate issue. 
  However, the editors should avoid as much as possible to complexify the structure of GitHub issues by creating complex hierarchies between the issues. For instance, the visual data model proposed by the issue owner does not need to be separated from the initial issue 45 since it represents a direct source of information which may be relevant for more than one issue. A good practice from here could be for other reviewers to share, as comments to this issue, their own data models.

> A simple guide if you would like to know how to [create an issue](https://docs.github.com/en/github/managing-your-work-on-github/creating-an-issue) on GitHub.
>
> 1. The editors or the moderator answer, usually within one working day, to the initial issue created by ackowledging the issue or directly giving an initial answer.
> 2. The editors give more details about the pros and cons of the issue(s) raised to trigger the discussions and comments from other Working Group members. 
> 3. The discussion continues as comments to the issue.
> 4. When no agreement has been reached, the editors prepare the discussions and alternatives to be tackled during the next webinar following the public review period.

 
</details>


## ` Step 14` . Proposition enhancements

**Key activities**
>
>

<details>
  <summary><b>Description</b></summary>
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
</details>

<details>
  <summary><b>Tool(s)</b></summary>
</details>

<details>
  <summary><b>Example(s)</b></summary>
 
 ```
  TBD
  ```
</details>



## ` Step 15` . Propose additional attributes

**Key activities**
>
>

<details>
  <summary><b>Description</b></summary>
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
</details>

<details>
  <summary><b>Tool(s)</b></summary>
</details>

<details>
  <summary><b>Example(s)</b></summary>

```
  TBD
  ```
</details>

## ` Step 16` . Perform semantic mapping of attributes

**Key activities**
> * Upon receiving additional attributes from the [<b>Working Group members</b>](https://github.com/cbahim/SDG-sandbox/tree/master/process_and_method/stakeholders#working-group), [<b>the editors</b>](https://github.com/cbahim/SDG-sandbox/tree/master/process_and_method/stakeholders#editors) will perform a semantic clustering of attributes. Afterward, editors will map the ‘semantic clusters’ to existing attributes, if any. Should there not be an attribute to map a ‘semantic cluster’ to, the editors will propose a new attribute (or entity). 
> * the [<b>Working Group members</b>](https://github.com/cbahim/SDG-sandbox/tree/master/process_and_method/stakeholders#working-group) discuss the ‘semantic clusters’ - and potentially the new attribute(s) - and work towards consensus. 

<details>
  <summary><b>Description</b></summary>
  Wherever attributes do not convey exactly the same information, ‘semantic clusters’ of similar attributes should be constructed to find a common, higher-level, and more general attribute to which the more specific attributes can be mapped. 
  
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
  
  * [SKOS Simple Knowledge Organization System - Mapping](https://www.w3.org/TR/skos-reference/#mapping) - How to map attributes 
</details>

<details>
  <summary><b>Tool(s)</b></summary>
  <i>There are no specific tools for this step.</i>
</details>

<details>
  <summary><b>Example(s)</b></summary>
  
 ```
  TBD
  ```
</details>

## ` Step 17` . Harmonise, entities, attributes and descriptions across the data model

**Key activities**
>
>

<details>
  <summary><b>Description</b></summary>
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
</details>

<details>
  <summary><b>Tool(s)</b></summary>
</details>

<details>
  <summary><b>Example(s)</b></summary>

```
  TBD
  ```
</details>

## ` Step 18` . Update draft data model

**Key activities**
>
>

<details>
  <summary><b>Description</b></summary>
</details>

<details>
  <summary><b>Rules and Guidelines</b></summary>
</details>

<details>
  <summary><b>Tool(s)</b></summary>
</details>

<details>
  <summary><b>Example(s)</b></summary>
 ```
  TBD
  ```
</details>

```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
