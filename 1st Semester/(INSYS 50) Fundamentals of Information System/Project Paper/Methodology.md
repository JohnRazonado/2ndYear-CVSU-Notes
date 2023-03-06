> Still not yet decided on the main title I guess?
> Need to discuss tomorrow I guess.

> See the [[Initial Project Proposal#Restaurant Inventory Manager|Project Proposal Topic]]

This part entails the picking of different "[Software development process](https://en.wikipedia.org/wiki/Software_development_methodology)" by picking one software development methodology to rule the proposal that can be used to give flow and strategy in creating the system.

> for now, I am more towards using SDLC or Waterfall at this moment.

%%## Waterfall
> Waterfall will be the methodology or Feature-Driven Development

Many consider the waterfall method to be the most traditional software development method. The waterfall method is a rigid linear model that consists of sequential phases (requirements, design, implementation, verification, maintenance) focusing on distinct goals. Each phase must be 100% complete before the next phase can start. There’s usually no process for going back to modify the project or direction.

It is super linear in nature. You can't go back to the last phase like design if the customer wants to but it subjects to having more time to the other phase.

Due to linear in nature like this proposal in return to which mostly not need feedback on the client until it was created was going to be hard in my end point but this is the easy one to discuss and explain in the end. Which is suitable on the design we need and this is due be cause we are a small team to which mostly 2 or 3 of the members are going to be a developer at this point.

#### SDLC (Software Development Life Cycle)
> This methodology is pretty old by according to recent standard that new methodologies has the same strategy to this one but tweaking stuffs on the flow.

This also fall the new term of **Feature Driven Development** approach that I need to search upon.

Still unknown what to really do now.%%


## Feature-Driven Development
![[Pasted image 20230205235250.png]]

> I'm rotting for this one since this is more compelling and still have the modern design of SDLC and some parts of agile that I think we need.

%%
### Comments
But more sites thinks that this is not suitable for one or two man developer since it carries a lot of duties for different side of things.
like testing, designing decision, building feature, rebuilding it, and so more that is making stuffs more inefficient.


I guess waterfall is the main call at this point. But still undecided since most of the point of FDD is having iteration on the fly. But most of the related projects used FDD and tweak it so it can have minimize impact of being preferred to large and long-term works by not overflowing different manifesto's of it.%%

### Core meaning
#### As an Agile Methodology
Teams use the agile development methodology to minimize risk (such as bugs, cost overruns, and changing requirements) when adding new functionality. In all agile methods, teams develop the software in iterations that contain mini-increments of the new functionality. There are many different forms of the agile development method, including scrum, crystal, extreme programming (XP), and feature-driven development (FDD).

>https://www.synopsys.com/blogs/software-security/top-4-software-development-methodologies/


An Agile methodology for developing software, Feature-Driven Development (FDD) is customer-centric, iterative, and incremental, with the goal of delivering tangible software results often and efficiently. FDD in Agile encourages status reporting at all levels, which helps to track progress and results.

FDD allows teams to update the project regularly and identify errors quickly. Plus, clients can be provided with information and substantial results at any time. FDD is a favorite method among development teams because it helps reduce two known morale-killers in the development world: Confusion and rework.

>https://www.planview.com/resources/articles/fdd-agile/

#### According Design Rush
This software development methodology is best suited for big teams that work on project-oriented or object-oriented technology and organizations that are moving from stage-based to iterative approaches.  
  
Feature-driven development combines several software development practices and methodologies into one. Its main objective is to focus on organizing software development around its features and delivering working products quickly.

**Advantages**:
-   Helps move large projects with continued success
-   Obtains structure and a good overview of the project through its five simple processes: model development, feature list building, planning, design and build by feature
-   Built on set standards for software development and uses industry’s recognized best practices, making it easy for developers to understand the method quickly

**Disadvantages**:
-   Not suitable for smaller projects and teams due to complexity
-   Lead developers need to be highly trained and fully equipped because a lot of responsibility is on them
-   This highly complex process needs to be monitored at each phase to avoid significant issues

![[Pasted image 20230206193726.png]]

### According to some paper
**Feature Driven Development (FDD)**
Created by Jeff De Luca in late 1990s, Feature-Driven Development (FDD) is an agile software development methodology, which focuses on customer requested features, grouping of these features into areas and iteratively designs and builds the features. FDD includes milestones for project status tracking and produces two-week regular builds to keep customers as up-to-date as possible. 
Palmer and Felsing (2002) outline the main characteristics of FDD approach: 
1. Domain Object Modeling: Creation of a visual model (class, UML) depicting the system. Model is updated in each iteration with new features.
2. Developing by Feature: Implement only the required features by the customer.
3. Individual Class (Code) Ownership: Each developer develops and maintains a class that is assigned to him or her.
4. Feature Teams: Working together to find a solution to a feature. 
5. Inspections: Includes unit testing, and design and code inspections. 
6. Configuration Management: Tracking changes. 
7. Regular Builds: Demonstrate to the customer as up-to-date as possible. 
8. Visibility of progress and results.

![[Pasted image 20230206202415.png]]

![[Pasted image 20230206232741.png]]

Need modern editing of this thing.

### More info from the paper
Feature-Driven Development (FDD) is an agile software development methodology that was created by Jeff DeLuca between 1997 and 1999. It is one of the most widely used agile methodologies in industry. It can be described as “right first time” approach to agile software development. FDD claims to be suitable for mission critical systems (Palmer & Felsing, 2002)

#### Steps of FDD
##### Develop an Overall Model
Initial phase is the startup phase, which is performed once in a project. This phase begins by developing an overall model for the project, and it’s known as shape modeling or domain object modeling. UML diagrams depicting what classes are in the domain and how they connect and interact with each other is prepared and the required methods and attributes are placed in the classes. Sequence diagrams are also prepared, if required. The models are crucial for having a shared understanding for the multi-disciplinary team. Visual models provide guidance to the developers and customers. The models are updated in each iteration with new features. 

Khramthchenko (2005) identifies the three different roles and the modeling process in the domain object modeling phase. In this phase, domain experts identify user stories, developers to build class diagrams using color UML according to these user stories, and project managers to organize the project and identify team progress. It is important that all user stories are supported in the visual model that was created by the team (Khramthchenko, 2005). The model is updated with new methods, attributes and relations for every user story that extends the current model. Color UML associates color codes with UML diagrams. It was proposed by Peter Coad, Eric Lefebvre, and Jeff De Luca (Coad, Luca & Lefebvre, 1999). Colors are associated with different archetypes to determine their type. Coad, Luca and Lefebvre (1999) defines archetypes as the following:

1. Pink (Moment/Interval): For business purposes, events that occur at a moment in time or in an interval of time. 
2. Yellow (Roles): Different roles being played.
3. Blue (Description): Description that labels and classifies objects.
4. Green (Party, Place, or Thing): Tangible thing that is uniquely identifiable.

Colored UML enables building UML models faster, and promotes shared understanding for domain experts and developers. In FDD, it is encouraged for modeling to be done in teams consisting of developers and domain experts

##### Build a Feature List
Startup phase continues with building a detailed, prioritized features list. Features list team is formed to build the features list. Team members need to have an understanding of the basic scope of the project to develop the feature list. Features should be small and should usually take about two weeks to complete. If a feature takes more than two weeks to complete, it should be decomposed into smaller features. Short iterations provide and demonstrate working up-to-date builds to the customer. In order to group similar activities, the features are divided into feature sets and subject areas.
It is recommended to have a formal documentation available in FDD. Internal websites, such as wikis, is good place to store information about the project. Project diagrams, list of team members, feature list, work assigned to developers, reports are examples of documentation that can be stored. These documentation become especially important in large scale projects that has long development times since it is useful to see past decisions and reasons for them. It is also important for the customer to have access to the latest requirements.

##### Plan by Feature
After building the feature list, Plan by Feature phase begins. In this phase, the order of features to be implemented is determined. The order is based on various factors such as complexity of the feature, work load of developers and dependencies between features. Planning team assigns due dates for the activities based on dependencies, work load, complexity of the development.

Furthermore, the team assigns classes for the developers. The developer is responsible for the classes that are assigned to him or her. Palmer and Felsing (2002) identify advantages and disadvantages in individual class ownership. According to Palmer and Felsing (2002), an individual is assigned to maintain and develop classes which give the individual responsibility. The class will be faster to maintain and develop when the individual is highly familiar. With many developers working on the project, individual class ownership provides easier to find an expert on a particular class when a developer needs assistance for a dependency or similar work. Finally, it gives the individual to take pride in his or her work (Palmer & Felsing, 2002). 

On the other hand, individual class ownership has disadvantages. If developers are busy, code dependencies may slow down. If class owner leaves the project, it takes time to get another developer up to speed. Collective code ownership solves the code dependency waiting issue but introduces non-ownership or ownership by few dominant developers inside the development team.

##### Design by Feature
After startup phase, development continues with the construction phase. Construction phase is iterative for feature sets, activities will be performed for each feature. First activity is Design by Feature Set, where features that are going to be implemented in approximately two weeks are selected by the chief programmer and sequence diagrams for the features is designed. Object model is updated with the new and updated class details. For each feature, these make up a design package. Design inspection is performed to review the work.

##### Build by Feature
Design by Feature is followed by Build by Feature process. In Build by Feature process, features selected by the chief programmer and passed successfully in the design inspection are implemented. Code is developed by the class owners. After the code is complete, unit test and code inspection is performed to make sure all the requirements are met. If it passes the inspections successfully, it will be promoted to a build.

##### Milestones
Definition of milestones is important in software projects, as they establish an explicit and unambiguous definition of what needs to be done (De Luca, 2003). De Luca (2003) identifies that usual developer responses to whether a feature is completed are ambiguous, there established milestones are required for a sharp definition of tasks.  

FDD uses milestones to track project development progress. Each feature consists of six milestones and progress is completed sequentially. Percentages are added to indicate completeness and to provide more accurate monitoring. De Luca (2003) outlines the activities in each feature as the following:

1. Domain Walkthrough – 1%
2. Design – 40% 
3. Design Inspection – 3% 
4. Code – 45% 
5. Code Inspection – 10% 
6. Promote To Build – 1%

Domain Walkthrough, Design and Design Inspection are Design by Feature activities, while Code, Code Inspection and Promote to Build are Build by Feature activities.



### References 
https://etd.ohiolink.edu/apexprod/rws_etd/send_file/send?accession=ohiou1271449120&disposition=inline

Palmer, S. R., & Felsing, J. M. (2002). A practical guide to feature-driven development. Prentice Hall PTR.

https://csis.pace.edu/~marchese/CS616/Agile/FDD/fdd.pdf

https://www.lucidchart.com/blog/why-use-feature-driven-development

https://www.planview.com/resources/articles/fdd-agile/

C. P. Puri, Agile Management: Feature Driven Development, 2009, Global India publications, ISBN: 9380228260

Doi: 10.1109/52.877874 Russ, M. L., & McGregor, J. D. (2000). A Software Development Process for Small Projects. IEEE Software, 17(5), 96–101. doi:10.1109/52.877874


# Picking the right one
### In the end
I'll stick with FDD since it is manageable with a small team but needed to also minimize a lot of features to be crunched down and still have the paper in tact from time to time and so on.

## Check other Related paper
Most of them use the old method which is SDLC which is mostly usable I guess to us but I'll try to seek more information.

## Check Flexibility and Requirements
Check if you need a lot of flexibility or your fine with sticking with a more linear flow.

Agile if great with web development due to in need of fast approach and high flexibility demand
Classic software development probability doesn't need that and require more static and predictable flow and stability like **waterflow**

The more capable methodology that could fit based on different resources that I've gathered from websites and other related papers are:
- SDLC's Waterfall method
- Feature-Driven Development
- General SDLC

### [[Restaurant Inventory Manager#What can the system do|What can the system do]]
- Automated System inventory management
	- Check inventory needed by having the ingredients known to the system
		- Having a [[Chapter 5 - Electronic and Mobile Commerce and Enterprise Systems#^4622d7|catalog management]]
	- Process needed items to filled up to the manufacturers and suppliers
		- Need to have an [[Chapter 5 - Electronic and Mobile Commerce and Enterprise Systems#^9623cb|electronic exchange]]
		- Also have the [[Chapter 5 - Electronic and Mobile Commerce and Enterprise Systems#^c12bee|Order processing system]]
- Store all information to database
	- add items on the system
	- edit inventory information
	- have recovery system to back it up.
	- access by different users
		- Administrator (full control)
		- supplier (optional but more on reading only)
		- Inventory admin (have control on the inventory management)
		- normal employee (read ingredients menu only and inventory)
			- Can also have an alert system to let the inventory admin know some shortage.
- Have a decision support system
	- Allowing to have an aid on how to increase profit and what to really put on the menu in the long term
	- This will help enabling the admin become a better problem solver and decision maker
	- Adding tools that presents information about sales, profit, and different chart enabling the support system side helpful to higher ups.
	- This is optional since I don't really know what it really is and how it is implemented on the internal side or things.
### [[|What do it really needs to accomplish?]]
- Cost-volume profit evaluation (needed since it can handle the sales of the cashier part)
- Decision support system
	- for charts and sales reports
	- more input to the menu system.



## Define Software's end-user
Check who's your target to use the software
Is it require a fixed requirement or does it need a flexible approach?

Access by different users
- Administrator (full control)
- supplier (optional but more on reading only)
- Inventory manager (have control on the inventory management)
- normal employee (read ingredients menu only and inventory)
	- Can also have an alert system to let the inventory admin know some shortage.

## Check project size
This is a more certain and a small specific targeted team and customer which doesn't require a lot of flexibility in my opinion.

Project size will be on having multiple setup and pretty hard since it needs a:
- Tablet/Computer system
	- For managing the inventory manually with a GUI system.
	- Checking different menu items and ingredients for lookup (still need to check upon.)

## Check time frame (Development time frame)
- Around 8-10 months 
- that will probably include the creation of the proposal, creation of the project system, testing, deployment, and up to data gathering and conclusion of the system.
- 

## Check team's location
- Abian's restaurant
