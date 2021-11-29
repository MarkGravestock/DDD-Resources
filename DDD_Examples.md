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

# Repository

[Patron Profile](https://github.com/ddd-by-examples/library/blob/master/src/main/java/io/pillopl/library/lending/patronprofile/infrastructure/PatronProfileReadModel.java)

# Aggregate Root
- [Order](https://github.com/odrotbohm/spring-restbucks/blob/main/server/src/main/java/org/springsource/restbucks/order/Order.java)
  - Note also shows Jmolecules