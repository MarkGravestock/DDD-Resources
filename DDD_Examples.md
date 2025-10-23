### DDD Resources

[Awesome DDD Resources](https://github.com/kgrzybek/awesome-ddd)

[DDD Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process)

[Virtual DDD]()

#### Example DDD Projects

##### Highly Recommended by DDD Experts

[eShop by Microsoft](https://github.com/dotnet/eShop)
- Reference microservices architecture using .NET and Docker (successor to eShopOnContainers)
- Implements DDD, CQRS, and Event Sourcing patterns
- Widely cited by industry experts and Microsoft's official .NET architecture guidance
- Demonstrates bounded contexts in a real-world e-commerce scenario

[DDD Sample - Cargo Shipping](https://github.com/citerus/dddsample-core)
- The original DDD sample application from Eric Evans' community
- Classic example frequently referenced in DDD literature
- Demonstrates core DDD concepts in a shipping/cargo tracking domain
- Java-based implementation with clear bounded context separation

[CQRS Journey by Microsoft Patterns & Practices](https://github.com/microsoftarchive/cqrs-journey)
- Comprehensive guide to CQRS and Event Sourcing with DDD
- Developed by Microsoft patterns & practices team
- Includes extensive documentation and real-world case study (conference management system)
- Highly educational with detailed exploration of design decisions

[Confab by DevMentors](https://github.com/devmentors/Confab)
- Conference management system built as a modular monolith in .NET
- Reference project demonstrating CQRS, Clean Architecture, and DDD
- Excellent example of module boundaries as bounded contexts
- Part of DevMentors' comprehensive modular monolith course

[Spring Modulith Examples](https://github.com/spring-projects/spring-modulith)
- Official Spring project for building modular monolithic applications
- Demonstrates DDD concepts within Spring ecosystem
- Strong support for domain events and bounded context verification
- Recommended by Spring team and DDD practitioners

[Axon Framework Reference Guide Examples](https://github.com/AxonFramework/AxonFramework)
- Leading event-driven microservices framework with DDD support
- Comprehensive examples of CQRS, Event Sourcing, and Saga patterns
- Strong community and endorsement from DDD practitioners
- Includes sample applications demonstrating complex business scenarios

##### Community-Vetted Examples

[Modular Monolith with DDD](https://github.com/kgrzybek/modular-monolith-with-ddd)

- Uses CQRS by splitting [Read/Write](https://www.kamilgrzybek.com/design/simple-cqrs-implementation-with-raw-sql-and-ddd/)
- Example of [interface passed](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Domain/UserRegistrations/UserRegistration.cs) to domain object, from [command handler](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/UserRegistrations/RegisterNewUser/RegisterNewUserCommandHandler.cs)
- Generally in this project commands return no result, queries produce DTOs from Domain
  - Example of [Domain returning Dto](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/Users/GetAuthenticatedUser/GetAuthenticatedUserQueryHandler.cs) directly, return by [API](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/API/CompanyName.MyMeetings.API/Modules/UserAccess/AuthenticatedUserController.cs)

[Bounded Contexts from "Implementing Domain-Driven Design" by Vaughn Vernon](https://github.com/VaughnVernon/IDDD_Samples)
- Companion code for Vernon's "Red Book" (IDDD)
- Authoritative examples from one of DDD's leading practitioners
- Demonstrates advanced tactical patterns and bounded context integration

[Library Project](https://github.com/ddd-by-examples/library)

[Factory Project](https://github.com/ddd-by-examples/factory)

[Spring RESTBucks by Oliver Drotbohm](https://github.com/odrotbohm/spring-restbucks)
- Created by Oliver Drotbohm (Spring Data lead and DDD advocate)
- Demonstrates DDD with REST APIs using Spring
- Excellent example of aggregates, repositories, and domain events
- Frequently referenced in conference talks and DDD workshops

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
