# Architecture Pattern for Context Diagram

A context is a good starting pount when defining or reviewing a system's architecture. This diagram should show a big picture 
of the system within the context of the environment that it will be running. This diagram is intended first for business and non-technical
people to begin to understand the dependencies of the system and the relative relationships within the environment. Secondly, this diagram 
is used by technical audiences to understand scope. To achieve this a context must limit the focus to one system.  Therefore each system in 
an environment would define it's own context.

## Elements

- **Systems** - Any technology that directly supports a business process.
- **People** - Types of users that interact with the system
- **Boundaries** - A logical grouping of areas that join **systems** and/or **people** into areas that share a logical proximity.
- **Relationships** - A connection between elements, usually single direction and designates enterprise entities.

## Defined Elements

- Systems should be related as upstream/downstream relationships. 
  - **Upstream** - systems that provide data entities to the target system.
  - **Target** - This is the primary system that this diagram is documenting
  - **Downstream** - systems that consume data entites from the target system
- People should be defined a generic technical grouping.
  - **Anonymous** - A generic **NOT** identified user of the system
  - **User** - an authenticated user of the system but not managed centrally
  - **Managed** - A generic identified or authenticated user of the system
- Boundaries represent the logical groupings within in the business
  - **Enterprise** - Defines the systems and people that are logically held within the organization
  - **System** - Defines a grouping of sub-systems. If there are multiple systems that are grouped to support a business process but 
      otherwise are defined as seperate systems.
- Relationships define people interacting with systems or system integrations.
  - **Uses** - Relationship between people and systems. This desgnates normal system usage.
  - **Admins** - Relationship between people and systems. This desgnates elevated system credentials usage.
  - **Upstream** - Relationship between systems.  This specifies the enterprise data entity exchanged to the specific system and would spec the 
      middleware system used for exchange
  - **Downstream** - Relationship between systems.  This specifies the enterprise data entity exchanged from the specific system and would spec the 
      middleware system used for exchange
      
## Reading

The context diagram is ment to be read left to right and then top to bottom.

## Guidelines

- **Limit the number of systems:** Most context diagrams should not be overly complicated. As a general rule there should not be hundreds or even tens of 
    upstream and downstream systems.  If there are that many systems then they could probably be artificially grouped on the diagram and 
    described as a summary of what they do.
    
## Example 

```
@startuml
!include <C4/C4.puml>
!include <C4/C4_Context.puml>

Boundary("B1", "Upstream") {
 System("UP1", "Upstream01")
 System("UP2", "Upstream02")
 System("UP3", "Upstream03")
 Lay_D("UP1", "UP2")
 Lay_D("UP2", "UP3")
}

System("TARGET", "Target")

Boundary("B2", "Downstream") {
 System("DOWN1", "Downstream01")
 System("DOWN2", "Downstream02")
 Lay_D("DOWN1", "DOWN2")
}

Rel_R("UP1", "TARGET", "Customer")
Rel_R("UP2", "TARGET", "Transactions")
Rel_R("UP3", "TARGET", "History")
Rel_R("TARGET", "DOWN1", "Usage")
Rel_R("TARGET", "DOWN2", "Transactions(Returns)")


Lay_R("UP2", "TARGET")
Lay_R("TARGET", "DOWN1")
@enduml
```
