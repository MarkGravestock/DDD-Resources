### Example DDD Projects

[DDD Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process)

[Modular Monolith with DDD](https://github.com/kgrzybek/modular-monolith-with-ddd)

*Example of [interface passed](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Domain/UserRegistrations/UserRegistration.cs) to domain object, from [command handler](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/UserRegistrations/RegisterNewUser/RegisterNewUserCommandHandler.cs)
*Generally in this project commands return no result, queries produce DTOs from Domain
**Example of [Domain returning Dto](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/Modules/UserAccess/Application/Users/GetAuthenticatedUser/GetAuthenticatedUserQueryHandler.cs) directly, return by [API](https://github.com/kgrzybek/modular-monolith-with-ddd/blob/master/src/API/CompanyName.MyMeetings.API/Modules/UserAccess/AuthenticatedUserController.cs)

[These are the sample Bounded Contexts from the book "Implementing Domain-Driven Design" by Vaughn Vernon](https://github.com/VaughnVernon/IDDD_Samples)

[This is a project of a library, driven by real business requirements](https://github.com/ddd-by-examples/library)

[https://github.com/ddd-by-examples/factory](https://github.com/ddd-by-examples/factory)