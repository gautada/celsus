# Architectue Pattern for Locations

**Locations** are a critical part of defining a solution and is used to answer the **Where?** interogatory for a solution. At first **Location** seems simple, as such it can be a physical address or it can be physical place for a device like a server. Simple definitions of physical location of each part in a solution is not valuable to the architecture. The relative grouping of the parts and the contracts between the groups is what is important to the architecture. To define **Location** for architecture we us four architecture components: Geography, Zone, Environment, Instance.

Geography: The atomic physical location of a solution.
Zone: The logical collection 
Environment: ...
Instance: ...

When defining a soluton location can be very complicated very quickly. At first thought, location is a physical place; but, location is also the virtual place like a network configuration or the collection of physcial devices that provide a service or feature required by the solution. This pattern attempts to define a simplified three layer concept that can be used across all solutions.

## Goals
- Define the answer to **"Where?"** using first principles.
- Simplify the fractal nature of virtual locations
- Clarify the cascade of constraints down the location chain
- To reduce complexity of location definition

## Context

![Context Diagram](https://plantuml.com/plantuml/svg/fLHjRzem4FxEh_3Gf844f1JQhjLKH05rbRgkMZjDMZKXurmIQuuTsKv71lptdVC25DPgwb24xRjxNcAVyuPB9b8Vo8THtnlrEqaQY_FQcwVHwKX92tFxGfPo2VhPV9me2V8v_3YJDERikImaGcNn1bvxHnPtcR4GBoTeIoUQ6vYkBbGgVQgp1XMScXOHT0QYHHO3coMmQf61fI66tmekVpQHunQqKN8ndSpjQWSpyC4mZQD1RWjxM4INEuApTl73MM7gDOmbORw96ygST1rVZ6VB4MKHBFygO855yX-jbyUnfrJ6_qzfi57w0e9QhgI9UB8jLkWjBlWAAnPNqeTvWxl_PIFGAiR3ikerUZVAWgc4S9Iu9lNxY1k23ytNTK8DaLtCEXmA4TOd820-moWv9_dBvcmFepwv5LJQhv-kVpGYQnDpvdc9Ys0Vjetr1PzrGcwZTDRX2dkrNPLxhi4UBhcnv1vYX5ZOC8GOhc1CnLv8KqjzwdLdzFZz4UsT7fsS13rwpEZf0HpsPlt3e7lGwzASSpAdo0Tcor2gTQXf77CPTWGFm6F6O_rsPRJvCcVDSYjmbyg69cDE7Hjfasl5YjEhrsf5QpVg8IZC9b5MRv7wvVPYI71Y6AU2Y198b2PC2G6iM0NhZ24seZP7S4Q5o0YrrdMSGK3PXNXWqYS6z2DdOEhDjOVVc7QAtyjnYBIXezaHCn7Lu1CDHgKQAPoTYgxGnpm9jKeJBBCg11k19Y7WPSiz1GY08E2CWsIPWrFi85TZ4c0yS9ePyHLBtTS9EV0e4cMWisKMv2FNIhe2vtNoT3b4ov91OjCzzvLjmgMnLBxi6RiOpSROuaQ9r55iUwWOdEBLrdouVezzjKBCfFeHtCqftupyuf7bSaUdXhTufpMgCog_NbYKrrJXdLtPgTh9RjlVLDRkFdx-DhsUN4vknetc7m00)

This pattern defines 4 conceptual parts to define location.

Geography: Usuallly the physical location with a unique address, examples "East C"exceptions are "Internet", "Kubernetes", ...
Zone: A collection of Environment(s) or Instance(s) that are logically grouped for efficiency
Environment: A collection of resources that form a solution
Instance: A device or service that provides resource(s)


Physical Location or a Gerographical Area --> Network --> Environment(Dev,Test,Prod) or Network Segment

[Context](https://puml.gautier.org/plantuml/uml/fLHjRzem4FwUN-56amOIa5BegwQYDaHTDzPLfLsrLGYPv4Yi9NPaEnqfyDzt3k6bwwYc3aN4T-VdUUxE5-ymxiTP0EI3stRSTYFDalZKsddk7Rg2QvZeLwAKSP1RuqagEF1j-6xEQSByRL58Ov4dQxZrdapxkTAGp3nCIwQIAHZEpqN60ohp2eqPLJKIqn74DJBjw3o5UOrqD0tH_Ivc_6SLEQv1Ai6dGs-YvtzWEW4eN-9R8RU65rX4bnt1LNtnmzKYgRSmbeH54zUK1UdAF-sEPYxr8vZzLK237_5_JBqyZXTAfV__b3fhfHk8gMQ2guYbcs8BlUavc-EEwIKFO59XvdzM6KkHu65fyHQzAw51BONmpT4czct45C675hPDg2AyYL63Go7Yjmd4a9oWbvoIejY2xS5ja-kOSdttfJUeH5gdwiHnKkF1EQmh7SHir0YPZh9HWmcSrVfoksC6xE62AKrk8K68XZL3YEubp1U94z9Cqu0wpH4zEDgdhUFzmyDnYnxuz7WNzbgZzjwukTjgqeBJcr3a0xMHK2PbA6cIC1usOZO6nrUEtwul4ws-pcbffcFiKZdGfCkeOIDrqXF-ulHiorfzN7OQvOhvDBPhn7wuBeq1kG21i3GgGbKojSWQ4ejmXUWjrWCprsCMPhAGM20s8BxWFgGwAr7koXmGZpyoARYv44hOtCAJ3w1Y1txJREzIJOaBvcumvjLtvrEzwzhLvJRwImtfamcTtVUnqBD7od3OMCnqJdxW9s12G9MkD-a6wca9UieaR8DzOp9al82jqWf1cD2oHRanFAHtxW47n1MuNClWtQVAn3yVAU9kcDa890SSSN9fPi1qeEpUPcKIGkDRLNUpik_wDI-J8eNQcMBFAzi0bTMz0fjRLl_Zr_jXpxlmhhgLwcy0)

OSI Layers

https://www.freecodecamp.org/news/osi-model-networking-layers-explained-in-plain-english/

- Please | Physical Layer
- Do | Data Link Layer
- Not | Network Layer
- Tell (the) | Transport Layer
- Secret | Session Layer
- Password (to) | Presentation Layer
- Anyone | Application Layer

