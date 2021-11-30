### DDD Resources

[Awesome DDD Resources](https://github.com/kgrzybek/awesome-ddd)

[DDD Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process)

#### Example DDD Projects

[Modular Monolith with DDD](https://github.com/kgrzybek/modular-monolith-with-ddd)

- Uses CQRS by splitting [Read/Write](https://www.kamilgrzybek.com/design/simple-cqrs-implementation-with-raw-sql-and-ddd/)
- Example of [interface passed](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Domain/UserRegistrations/UserRegistration.cs) to domain object, from [command handler](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/UserRegistrations/RegisterNewUser/RegisterNewUserCommandHandler.cs)
- Generally in this project commands return no result, queries produce DTOs from Domain
  - Example of [Domain returning Dto](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/Users/GetAuthenticatedUser/GetAuthenticatedUserQueryHandler.cs) directly, return by [API](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/API/CompanyName.MyMeetings.API/Modules/UserAccess/AuthenticatedUserController.cs)

[Bounded Contexts from "Implementing Domain-Driven Design" by Vaughn Vernon](https://github.com/VaughnVernon/IDDD_Samples)

[Library Project](https://github.com/ddd-by-examples/library)

[Factory Project](https://github.com/ddd-by-examples/factory)

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