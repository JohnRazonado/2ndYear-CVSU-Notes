## Chapter 4
**Feature modeling** is a modeling approach normally associated with defining product lines.
**Goal modeling** is used to define business goals and relate them to needs and features.
**Process modeli**_**ng**_ is typically used to show user workflows either before or after a product is delivered. 
**Video-based requirements engineering** couples workflow models with video streams.
**Model-Driven Requirements Engineering (MDRE)** methodology described in the next section covers _both_ business modeling and analysis modeling activities, starting with business activities and ending with the detailed interaction of users and the proposed product or system in the same integrated physical model.

![[Pasted image 20230530231236.png]]

Use case modeling has also been found to work well when discovering requirements for service-oriented architecture (SOA) systems.

Service-oriented architecture (SOA)

Unified Requirements Modeling Language (URML)

**Prerequisites for Using MDRE**
- Modeling Skills Not Readily Available
- Inadequate Tooling
- Organization Not Ready for MDRE

  

**MDRE processes** - include requirements gathering activities up to but not including design, where the focus of the elicitation and analysis activities is model creation and utilization

“Begin at the beginning”, the King said, gravely, “and go till you come to the end; then stop.” - Lewis Carroll, Alice’s Adventures in Wonderland, 186
>In this quote we can say that everything starts at some point, the beginning. That's all I can write for now.

  
>The main 4.5: MDRE Processes

**MDRE Processes**
1. **Initial Understanding**
- In the beginning of a project, we would like to know why a system or product is being built. There are, of course, conflicting points of view as to why products are created.
2. **Understanding the Context and How the Product Will Be Used**
- Product vision and scope documents may provide insight into the environment where the product will be used as well as information about the users of the product.
3. **Analyzing Product Features and Creating a Use Case Model**
- Once we have a draft set of features, we are able to start creating a model from which we will derive all our customer requirements (all of them, before ranking).
4. **Starting an MDRE Effort**
- Organization of a model is key to performing programmatic verification and requirements extraction.
5. **Managing Elicitation and Analysis Sessions**
- With MDRE, the management of elicitation and analysis sessions is done using the same process, although the participants may be different. Initially, subject matter experts, the team lead, and analysts will participate.
6. **Improved Productivity Through Distributed Modeling**
- Once a routine is established and some initial modeling has taken place, all the team members should understand how to use some tools; they will start to model in a consistent style.
7. **Conducting Model Reviews**
- Model reviews are conducted at periodic intervals


**Cross-cutting requirements** are those that trace to or impact other requirements in different areas.

Unified Requirements Modeling Language (URML)
>This is probably the language use by the UML tool for most of RE activities. This is as is in a short answer.


>This part is on the 4.5: MDRE Processes. This is some key terms inside of it.

**Feature tree** - shows the relationship of all these features
**Abstract use cases** - represent product features that are at a very high level
**Extending relationship** - is a specialized extension to a well-defined process.
**Business object modeling** - is the process of describing behavior in a domain.
**Loquacious objects** - are those that send many messages to other objects without receiving any.
**Passive object** - is one that receives messages but never sends any (including replies).


>Part of 4.7: Determining Model Completeness

**Serious Model Faults**
> This is part of the "Model Faults That Should Be Corrected Before a Model Is Completed"

|Error|Indicates That|
|---|---|
|Class Not Instanced|A concrete class has been defined to the model; however, an instance of the class cannot be found on any sequence or activity diagram. This means nowhere is it shown how this business object is used.|
|Concrete Use Case Not Defined|A process has not been adequately described. It does not have enough information provided to extract requirements.|
|Dangling Abstract Use Case|A subject area has not yet been modeled, the model is incomplete.|
|Hidden Artifact|Something in the model is not shown on any diagram. It appears to have been forgotten or overlooked.|
|Illegal Extending Association|An extending relationship has an abstract use case at least on one end, causing ambiguity.|
|Illegal Interface Association|A boundary or interface has an association with an abstract use case. This association will result in ambiguous requirements being generated.|
|Interface Not Used|An interface or boundary (a class with a stereotype of boundary) has been shown on a use case diagram, but nowhere is it explained how it is used.|
|Missing Boundary|The interaction of an actor with the product, either via software (a software interface) or visually (a user interface, panel, etc.), is missing.|
|Mixed Use Case Relationships|A use case with mixed abstract/concrete included/extending use cases is ambiguous, and as a result any requirements derived from it may also be ambiguous.|
|Unused Concrete Actor|It probably means that the model is incomplete, or the actor does not communicate with the system. An actor can only access a process through a boundary.|
|Use Case Completeness|Parts of the definition of the use case are missing. This may result in incorrect or incomplete requirements.|


## Chapter 5 and 6

>Part of 5.4: Selecting Significant Stakeholders

**Stakeholder** is any person whose opinions, needs, or preferences are likely to be relevant to the success of the project.

**Examples of stakeholders**
1. _**Installer**_ - In some fields, such as telecommunications or manufacturing, installing the software and configuring it to operate correctly with diverse preexisting equipment constitute a labor-intensive, mentally challenging task.
2. _**Tech support**_ - In many businesses, the staff who answer phone calls from irate customers need good remote diagnostic tools, as well as easy-to-explain user interfaces.
3. _**Competitor**_ - Some stakeholders want to see the project fail! But things get even more complicated when the same company is a partner in one part of a business and a competitor in another.

  
The term “stakeholder” may have any of three meanings, depending on context
1. **Stakeholder class** - A group, category, or type of individual with a certain set of concerns.
2. **Individual stakeholder** - A particular, named person who is a member of one or more stakeholder classes.
3. **Stakeholder representative** - An individual selected to represent a stakeholder class for the purposes of a project.

  

**Quality attribute requirement**- requirement expressed in terms of one or more quality attribute measures.

**Quality attribute scenarios (QASs)** [Bass et al. 2003] are a special kind of structured natural language description of a behavior.

**Quality attribute workshop (QAW)** brings together a diverse set of stakeholders in a one- or two-day meeting to elicit their quality attribute concerns and help them understand one another‘s concerns.

  
>Part of 5.3: Quality Attribute Requirements

Four Link topics areas of quality
1. **Process quality** Quality of the process that is producing the product
2. **Internal quality** Quality of the intermediate work products (some of which may also be deliverable work products)
3. **External quality** Quality of the finished product, before delivery
4. **Quality in use** Quality of the larger processes in which the delivered product is used.

**Quality attribute** is a system or process property indicative of quality in any of these quality topic areas.

>This is part of 5.5: Methods for Architectural Requirements Engineering
>There is an example there below. This part of the Quality Attribute Workshop

A QAS is typically structured to have the following parts:
1. Stimulus 6-11    
2. Stimulus source
3. Artifact
4. Environment
5. Response
6. Response measure



A way of bringing out issues that might not have been considered: (These are types of scenarios)
- **Normal operations** - These are the most obvious scenarios.
- **System-as-object scenarios** – in these scenario, the system is a passive object that is being manipulated by, say, a programmer or an installer.
- **Growth scenarios** - scenarios deal with likely or plausible changes to the requirements in the future. 12
- **Exploratory scenarios** - are improbable scenarios, such as the loss of power from an ―uninterruptible power supply. 13
>This is still part of the Quality Attribute Workshop


**Goal Modeling** - is used to define business goals and relate them to needs and feature.
**Global analysis** -  is a methodology for organizing a broad variety of soft, uncertain information gathered in the early stages of architectural requirements analysis.
**Factors** - Any requirement or stakeholder concern might be a factor, but there are many factors that are neither requirements nor stakeholder concerns in the usual sense.
**Issues** – identified by finding conflicts between factors
**Strategies** - a proposed decision that addresses one or more significant issues.
**Architecturally significant requirement (ASRs)** - carry high risk because they cannot be fully tested until very late in development. (End of Chapter 5 here)
**Software product lines**  - refers to engineering techniques for creating a portfolio of similar software systems from a shared set of software assets using a common means of production. (Start of Chapter 6. This is the real meaning of it and I didn't really look upon on this on my assignment. Well fuuuuu.)
**Platform initiatives** - platform refers to a common set of lower-level software services such as operating system and middleware.
**Platform NFR development** - software process help us to more systematically develop NFR’s for platform.


>Part of the 6.3: PND Practices

**The PND Process**
1. **Define Questionnaires**
2. **Elicit Stakeholders’ Inputs**
3. **Unify Terminology**
4. **Normalize Stakeholders’ Inputs**
5. **Reconcile Stakeholders’ Inputs**
6. **Define the NFRs for the Platform**
7. **Derive the NFRs for the Components**
8. **Check for Consistency**
9. **Check for Testability**
10. **Complete the Constraints**
11. **Tune the NFRs for Feasibility**
12. **Complete NFRs**
13. **Formal Review by Stakeholders**

  

**Define Questionnaires** - this activity defines the questionnaire that will be sent to the stakeholders for their inputs.
**Elicit Stakeholders’ Inputs** - This activity collects inputs from the stakeholders
**_Goal:_** is to complete the answers to the questionnaires and avoid any misunderstandings by having discussions during the on-site workshops.
**Unify Terminology** - This activity aims to unify the terms used in the stakeholders’ inputs.
**Normalize Stakeholders’ Inputs** - This activity aims to make the stakeholders’ inputs comparable with each other on the same scale and operating conditions.
**Reconcile Stakeholders’ Inputs** - This activity identifies and groups the similar stakeholders’ inputs, and then requirements engineers can define a single NFR to address this group of similar stakeholders’ inputs.
**Define the NFRs for the Platform**- This activity defines the NFRs for the platform from the stakeholders’ inputs that address the end-user needs.
**Derive the NFRs for the Components** - This activity allocates the NFRs to the related functional requirements, which are often defined in terms of services in a service-oriented platform.
**Component-level NFR model** - shows the relations among the NFRs at the component level.
**Check for Consistency** - This activity checks the consistency between the NFRs at the platform level with those at the component level.  
**Check for Testability** - This activity checks if the NFRs that have been developed are generally testable or not.
**Complete the Constraints** - This activity identifies the missing constraints under which the NFRs should be defined.
**Tune the NFRs for Feasibility** - This activity aims to ensure that the NFRs are implementable.
**Complete NFRs** - This activity completes the NFR definitions and makes them ready for external review by the stakeholders.
**Formal Review by Stakeholders** - This activity aims to collect feedback comments and get approvals from the stakeholders.

  

  

“„What is the use of a book,‟ thought Alice, „without pictures or conversations?‟” - Lewis Carroll, Alice‟s Adventures in Wonderland, 1865

  
**GOD BLESS….**
**To have Graceful Relationship… Be a Graceful Person…**