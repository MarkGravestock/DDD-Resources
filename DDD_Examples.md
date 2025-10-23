### DDD Resources

[Awesome DDD Resources](https://github.com/kgrzybek/awesome-ddd)

[DDD Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process)

[Virtual DDD]()

### Strategic Patterns

#### Bounded Context

- Some discusion [here](https://github.com/ddd-by-examples/library/blob/master/docs/big-picture.md) and [here](https://github.com/kgrzybek/modular-monolith-with-ddd#31-high-level-view)

### Examples Tactical Patterns

- Expressing Patterns in Code
 - [Type Based](https://github.com/xmolecules/jmolecules#using-the-type-based-model)
 - [Annotation Based](https://github.com/xmolecules/jmolecules#using-the-annotation-based-model)

#### Repository

See Blue Book pg 147

[Patron Profile](https://github.com/ddd-by-examples/library/blob/master/src/main/java/io/pillopl/library/lending/patronprofile/infrastructure/PatronProfileReadModel.java)
[Drinks](https://github.com/odrotbohm/spring-restbucks/blob/main/server/src/main/java/org/springsource/restbucks/drinks/Drinks.java)

#### Aggregate Root

See Blue Book pg 125
Red Book Ch 10

- [Post about Aggregate Root and Entity](http://scabl.blogspot.com/2015/03/aeddd-5.html)
- [Order](https://github.com/odrotbohm/spring-restbucks/blob/main/server/src/main/java/org/springsource/restbucks/order/Order.java)
  - Note also shows Jmolecules
- [Meeting Group](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/Meetings/Domain/MeetingGroups/MeetingGroup.cs)
- [User Registration](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Domain/UserRegistrations/UserRegistration.cs)
  - Note shows use of rule that uses query/view 
- [ProductDemand](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/ProductDemand.java)

#### Entity

See Blue Book pg 89

- [DailyDemand](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/DailyDemand.java)

#### Value Object

See Blue Book pg 97

- [Adjustment](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/Adjustment.java)

### Example Implementation Patterns

#### Read Model

- [AuthenticatedUserQueryHandle](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/Users/GetAuthenticatedUser/GetAuthenticatedUserQueryHandler.cs)

#### Module
- [MeetingsStartup](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/Meetings/Infrastructure/Configuration/MeetingsStartup.cs)
  - Includes Composition Root

#### Events
- [Domain/Integration](https://codeopinion.com/should-you-publish-domain-events-or-integration-events/)

### Example Architectural Patterns

#### Ports
- [Port](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/ProductDemandRepository.java)

#### Adapter
- [Adapter](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-adapters/src/main/java/io/dddbyexamples/factory/demand/forecasting/ProductDemandORMRepository.java)

#### Command

- [Command](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/API/CompanyName.MyMeetings.API/Modules/Meetings/MeetingGroups/MeetingGroupsController.cs)

#### Query

- [Query](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/API/CompanyName.MyMeetings.API/Modules/Meetings/MeetingGroups/MeetingGroupsController.cs)

#### Example DDD Projects

[eShop by Microsoft](https://github.com/dotnet/eShop)
- E-commerce microservices reference showcasing .NET with ordering service implementing 3 DDD layers (Application, Domain, Infrastructure)
- Demonstrates simplified CQRS approach separating commands/queries with same database, using Dapper for query performance
- Official .NET architecture guidance example with bounded contexts, aggregates, value objects, and domain events

[DDD Sample - Cargo Shipping](https://github.com/citerus/dddsample-core)
- Joint effort by Eric Evans' Domain Language and Citerus demonstrating practical implementation of DDD building block patterns
- Well-documented cargo tracking system illustrating aggregates, bounded contexts, and tactical patterns from the Blue Book
- One of few complete, non-trivial DDD examples with implementations in multiple languages (Java, .NET, PHP, Ruby)

[CQRS Journey by Microsoft Patterns & Practices](https://github.com/microsoftarchive/cqrs-journey)
- Learning journey documenting team's experience building conference management system with CQRS and Event Sourcing
- Complete working reference implementation with extensive guide covering design decisions, trade-offs, and implementation patterns
- Focuses on high scalability and availability using Azure Service Bus, includes case studies from other teams

[Confab by DevMentors](https://github.com/devmentors/Confab)
- Conference management modular monolith in .NET 5.0 with different architectural styles per module (CRUD, CQRS, Clean, DDD)
- Modules integrate via event-driven architecture using local contracts approach, demonstrating bounded context independence
- Uses PostgreSQL with EF Core, includes Blazor frontend, reference project for DevMentors' modular monolith course

[Spring Modulith](https://github.com/spring-projects/spring-modulith)
- Opinionated toolkit for domain-driven modular Spring Boot apps enforcing Vaughn Vernon's aggregate design rules (boundaries, events, identifiers)
- Provides module structure verification, integration testing, observability, and automatic documentation generation
- Supports asynchronous communication via domain events with explicit architectural concepts using jMolecules

[Axon Framework](https://github.com/AxonFramework/AxonFramework)
- JVM framework for event-driven microservices implementing DDD, CQRS, and Event Sourcing with minimal boilerplate code
- Provides APIs for commands, aggregates, events, queries, and sagas with Axon Server for event store and message routing
- Includes comprehensive documentation, whitepapers, academy courses, and sample applications for complex business scenarios

[Modular Monolith with DDD](https://github.com/kgrzybek/modular-monolith-with-ddd)
- Production-ready .NET application with DDD tactical patterns, Event Sourcing, and CQRS by splitting [Read/Write](https://www.kamilgrzybek.com/design/simple-cqrs-implementation-with-raw-sql-and-ddd/)
- Example of [interface passed](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Domain/UserRegistrations/UserRegistration.cs) to domain object, from [command handler](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/UserRegistrations/RegisterNewUser/RegisterNewUserCommandHandler.cs)
- Commands return no result, queries produce DTOs - [Domain returning Dto](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/Users/GetAuthenticatedUser/GetAuthenticatedUserQueryHandler.cs) returned by [API](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/API/CompanyName.MyMeetings.API/Modules/UserAccess/AuthenticatedUserController.cs)
- Extensive testing with [NetArchTest](https://github.com/kgrzybek/modular-monolith-with-ddd/tree/master/src/Tests/ArchTests) validating architecture, includes [C4 diagrams](https://github.com/kgrzybek/modular-monolith-with-ddd#31-high-level-view), Event Storming models, and [ADR docs](https://github.com/kgrzybek/modular-monolith-with-ddd/tree/master/docs/architecture-decision-log)

[Bounded Contexts from "Implementing Domain-Driven Design" by Vaughn Vernon](https://github.com/VaughnVernon/IDDD_Samples)
- Companion code for Vernon's "Red Book" (IDDD)
- Authoritative examples from one of DDD's leading practitioners
- Demonstrates advanced tactical patterns and bounded context integration

[Library Project](https://github.com/ddd-by-examples/library)
- Library management system with Event Storming, User Story Mapping, and BDD applied from inception - see [big picture documentation](https://github.com/ddd-by-examples/library/blob/master/docs/big-picture.md)
- Two bounded contexts: catalogue using CRUD, lending using domain model with hexagonal architecture
- Demonstrates mixed persistence strategies - [PatronProfile repository](https://github.com/ddd-by-examples/library/blob/master/src/main/java/io/pillopl/library/lending/patronprofile/infrastructure/PatronProfileReadModel.java) using plain SQL with JdbcTemplate and Spring Data JDBC

[Factory Project](https://github.com/ddd-by-examples/factory)
- Complete Spring-based enterprise application separating simple CRUD operations from complex domain logic in demand forecasting
- Implements hexagonal architecture - [ProductDemand aggregate](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/ProductDemand.java), [DailyDemand entity](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/DailyDemand.java), [Adjustment value object](https://github.com/ddd-by-examples/factory/blob/master/demand-forecasting-model/src/main/java/io/dddbyexamples/factory/demand/forecasting/Adjustment.java)
- Model Exploration Whirlpool approach building Ubiquitous Language with executable Domain Model and Domain Stories

[Spring RESTBucks by Oliver Drotbohm](https://github.com/odrotbohm/spring-restbucks)
- REST in Practice reference implementation showcasing hypermedia-based API with DDD patterns over a decade of evolution
- Demonstrates aggregates as REST resource boundaries - [Order aggregate](https://github.com/odrotbohm/spring-restbucks/blob/main/server/src/main/java/org/springsource/restbucks/order/Order.java), [Drinks repository](https://github.com/odrotbohm/spring-restbucks/blob/main/server/src/main/java/org/springsource/restbucks/drinks/Drinks.java) with consistency guarantees matching HTTP semantics
- Integrates jMolecules for expressing DDD building blocks in code, frequently referenced in Spring and DDD conferences
