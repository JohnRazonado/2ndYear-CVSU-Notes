##  Chapter 7: Requirements Management

![[Pasted image 20230628205854.png]]
>Will probably explain this image


The purpose of **requirements management** is to manage all of a project’s or product’s requirements post-elicitation, and to identify inconsistencies between those requirements and a project’s plans or work products .
**Requirements management** - includes the version control of all artifacts that are the sources of requirements or the products of the requirements management process. 
Examples of artifacts that would be controlled include 
- Source documents, pictures, and blueprints 
- Memos and meeting minutes 
- Requirements and stakeholder requests 
- Documents produced from requirements, including requirements, design, and test specifications. 
 
A **requirements baseline** is the set of requirements, source documents, and all documents derived from the set of requirements at a specific point in time. 
- Contract is normally considered the initial baseline..

**Feature creep** applies when many small changes are permitted without control or formal review.
**CCB** - change control board (CCB).

The **role of the CCB** is to provide a *central control mechanism* to ensure that every change request is properly *considered, authorized, and coordinated.*
The CCB considers modification requests (MRs), and after considering the impact of the proposed change, some of the MRs will result in changes to requirements or other artifacts. 

**ERB** - engineering review board 
**ECR**s - engineering change requests
**ECO**s - engineering change orders 
<mark style="background: #FFB8EBA6;">CCB is analogous to an engineering review board </mark>(ERB)

**Table 7.1 Requirements Engineering Change Management**
(Part of 7.2 Change management)
(Some decision making components done for RE by the CCB)

|Change Control Decision-Making Components | Description|
|---|---|
|Summary| Deciding whether to accept a proposed change to the requirements of a system|
|Inputs| Proposed requirements change, including justification and rationale|
|Steps| Considering the impact of the proposed change, costs, benefits, ROI|
|Deliverables|“Yes,” “No,” “Defer,” or “Yes,” but with modifications|
|Responsible| Change control board (CCB|
|Contributors| Proposer and CCB members|
|Methods| Tradeoff analysis|
|Tools| Costing tools, tracing tools, tradeoff tools|

**Table 7.2 Main Types of RE Analysis initiated by a CCB**

|Type of Analysis| Description| Processes Supported|
|---|---|---|
|Impact analyis| Follow incoming links, to answer the question: "What if this were to change?"| Change management|
|Derivation analysis| Follow outgoing links, to answer the question: "Why is this here?"| Cost-benefit analysis|
|Coverage analysis| Count statements that have links, to answer the question: "Have I covered everything?" Most often used as a measure of progress| General engineering, management reporting|

**Impact Analysis**
The objective of **Impact analysis** is to determine the financial, resource, or temporal cost of a change request or new feature.
> need to see every parts of the project that will change due to the new request/feature.

**Derivation analysis** is concerned with discovering the origin or rationale of a function, module, etc.
> Need to know why such feature or function is in the product.

**Coverage analysis** measures the ratio of defined to actual product features.
> Measure the contract compliance (e.g., what was agreed on versus what is currently being delivered.)

**Routine requirements activities** are those that take place on most, if not all projects.
> This is on 7.3

**Volatility** is usually measured by gathering statistics from a requirements data management system (RDMS).
>Part of "Identifying volatile requirements"

**Requirements** **traceability** is the ability to describe and follow the life of a requirement, in both a forward and backward direction; i.e., from its origins,
>Part of 7.4

**Traceability** is the key to coverage, derivation, and impact analyses.
>Main key to cover in Requirements traceability

**Goal-based traceability** starts with business goals or objectives, and traces are then used to determine that the business objectives have been met.
>Need to consider if the traces meet the business standards that are implace.

### Types of Traces
- **Forward from** **requirements** Allocation to system components to establish accountability and support change impact
- **Backward to** **requirements** Verification of system compliance to requirements, and avoidance of gold plating
- **Forward to** **requirements** Changes in stakeholder needs or assumptions that may require radical reassessment of requirements relevance
- **Backward from** **requirements** Contribution structures crucial for validating requirements.

**Project measurements** are used for day-to-day evaluation of project status, and to determine the completeness of an artifact or task to trigger the review process.

**Quality metrics** are those metrics that measure the quality of requirements artifacts (including the final product) but do not necessarily convey information about project progress or productivity.

**REMP** - requirements engineering management plan.

## Chapter 8: Requirements-Driven System Testing
by Marlon Vieira, Bill Hasling

![[Pasted image 20230628210040.png]]
>Need to explain this one too.

**Software Testing** is the process of executing software with the intent of finding errors [Myers, 1979], and it basically supports validation & verification (V&V) activities.

  

**CMMI (Capability Maturity Model Integration)** guidelines describe validation as the activity that demonstrates if a product will meet its intended use, and verification as the activity for ensuring that the product meets specified requirements.

**Verification** is mainly done by the development and testing teams, and it typically includes other non-testing-based techniques such as peer reviews, inspections, and debugging. On the other hand,

**Validation activities** are based on specified requirements, and the requirements engineers are very much involved.

**Model-based testing** attempts to derive test cases from a given model of the system under test (SUT) using a variety of test selection criteria.

**Model** is an abstract view of the system and specifies typically (parts of) the behavior of the system in terms of its control flow and/or data flow.

Three different types of models typically can be created
- **Requirements** **models** that specify the intended behavior of the system
- **Usage models** that reflect the behavior of a potential user
- **Models constructed** from the source code directly (where the system under test is a software product)


Approaches to use models for test generation
>This is part of the "Model-Based Testing"

1. Use case diagrams are used to identify the usage scenarios of the system. Abstract use cases represent related collections of use cases, and concrete use cases are the basis for test generation.
2. Package diagrams are applied to provide a hierarchy to divide a large model for easier navigation, and they also can be used to split a large model into multiple files to support multiple users.
3. Activity diagrams are used to show details of each use case in relation to steps on using the system. Activities are used not only to show test steps, but also to show expected results or validation steps. Swim lanes are used to distinguish between test steps and validation steps. Activities can be annotated with properties to provide information to be used in test generation.
4. Class diagrams are used to define equivalence classes to represent data variations used in testing. Variables are described as notes within an activity diagram to reference an equivalence class of data variations defined in a class diagram.

## Chapter 9: Rapid Development Techniques for Requirements Evolution
**Requirements elicitation and analysis** are *very much people-oriented activities.*

**Stakeholders** are *encouraged* to share their vision of the new product, understand each other’s *viewpoints, negotiate tradeoffs, and eventually come up with a common view of the features of a product such that it will be competitive in the market.*

**Prototypes** have the *potential of being more easily comprehensible both to stakeholders and developers*, without much special training.

**Exploratory prototypes** are used when the functionality is evolving or being discovered during the project. Agile approaches such as Scrum [Schwaber et al. 2004] may work well on software projects for such situations, where the functionality is added incrementally.

**Scrum** - may be applied both to early phase activities such as for rapidly developing a throwaway prototype, or during implementation where the development is broken down into monthly sprints.

### Requirements Engineering and Prototype Development in Parallel
**Requirement elicitation and analysis** are generally a precondition for successful development work.

**Scheduling a meeting** with the goal of identifying inconsistencies among stakeholders is not a very productive approach in our experience, since we don’t know a priori what all the inconsistencies are.

A more constructive approach to requirements discovery is to elicit requests from individual stakeholders, present these requests in a common and unambiguous form, and then collect feedback from the stakeholders.
Conflicts and inconsistencies can be detected in two ways:
1. Harmonized view can’t be constructed due to our perception of conflicts
2. Harmonized view gets rejected by some stakeholders because their perception of the system differs from our assumptions.

The *iterative nature of this prototyping process* allows us to *concentrate on manageable units and to make quick progress* toward a common and unambiguous representation.

**Storyboards** are a visual and textual medium that allows multiple stakeholders to produce, modify, and comment on the content,

**Storyboards** can be used for *high-level modeling of user stories over multiple events/interactions*, and they can also be used to model the low-level user interface (UI) interactions that occur for a specific application or even one of its user screens.

**Visual prototyping** is most commonly used in the context of UI design. Storyboards provide useful support for this type of prototyping.

**Fully executable prototypes** are the most generic alternative for creating a realistic and unambiguous representation of some aspect of the application.

**Branch prototypes** are the most common type of prototyping used by many software development organizations. A branch prototype is created every time a *development team starts to work out some uncertain issue by modifying the existing product* code without necessarily planning to add the changes to the product.

Creation of **fully executable prototypes** is *occasionally required* in order to understand the <mark style="background: #FFB8EBA6;">technological viability of the planned solutions.</mark>

A **primary optimization goal** for our prototyping approach is to *emphasize the collaborative aspects of interaction among the stakeholders* and to maximize the emergent shared understanding.
>part of "Modification Optimization"

The **prototyping process** is <mark style="background: #ADCCFFA6;">centered on artifacts that unambiguously represent</mark> some aspect of the planned system or feature.
>Also part of "Modification Optimization"

### Tips for Prototyping
>Part of 9.4 having some detailed information

1. Eliminate unnecessary work
2. Accelerate learning
3. Decide as early as possible
4. Deliver as fast as possible
5. Empower the team
6. Trade off reuse requirements with prototype speed
7. Develop bottom-up

