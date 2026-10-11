# Standards on Software Design Principles

## Domain driven design (DDD)

Domain driven design is a software design approach that focuses on modeling the core domain and its logic. It emphasizes collaboration between technical and domain experts to create a shared understanding of the domain.

Key concepts in DDD include:

- **Entities**: Objects that have a distinct identity and lifecycle within the domain.
- **Value Objects**: Immutable objects that represent descriptive aspects of the domain with no conceptual identity.
- **Aggregates**: Clusters of related entities and value objects that are treated as a single unit for data changes.
- **Repositories**: Mechanisms for accessing and persisting aggregates.
- **Services**: Operations or actions that do not naturally fit within entities or value objects but are part of the domain logic.
- **Bounded Contexts**: Explicit boundaries within which a particular model is defined and applicable.

## SOLID Principles

SOLID is an acronym for five design principles intended to make software designs more understandable, flexible, and maintainable.

Key SOLID principles include:

- **Single Responsibility Principle (SRP)**: A class should have only one reason to change, meaning it should have only one job or responsibility.
- **Open/Closed Principle (OCP)**: Software entities should be open for extension but closed for modification.
- **Liskov Substitution Principle (LSP)**: Subtypes must be substitutable for their base types without altering the correctness of the program.
- **Interface Segregation Principle (ISP)**: Clients should not be forced to depend on interfaces they do not use.
- **Dependency Inversion Principle (DIP)**: High-level modules should not depend on low-level modules. Both should depend on abstractions.

## BCE

BCE stands for Boundary, Control, and Entity. It is a design principle used to structure software systems by dividing them into three types of objects:

- **Boundary objects**: These represent the interface between the system and its actors (users or external systems). They handle interactions and input/output operations.

- **Control objects**: These manage the flow of the application, coordinating between boundary and entity objects. They contain the business logic and control the sequence of operations.

- **Entity objects**: These represent the core business data and rules. They encapsulate the state and behavior of the domain entities.
