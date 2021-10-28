# Hexagonal Architecture

In the evolution of software architecture, [loose coupling](https://en.wikipedia.org/wiki/Loose_coupling) has been at the centre. There is an emphasis on breaking applications into components which can be switched, replaced or updated without affecting the dependent components.

Hexagonal architecture is another advancement in loosely coupled architectures. It originated around the beginning of the shift to domain-driven designs and formed a basis of further advancements in the field of software design. 

## Intoduction

A hexagonal architecture is divided into three parts and defines the strict roles that these parts play within the application.

![Hexagonal architecture layers - User Interfaces, Business Logic and Data sources](https://raw.githubusercontent.com/abh1navv/learning-notes/master/microservices/images/hexagonal-intro.jpg)

**User Interfaces**

There can be many user interfaces to a backend - mobile apps, web apps, desktop softwares, etc. They will all get their resources from the Business logic layer.

The important part is that the interfaces should only be concerned with presentation. The only logic they contain should be related to modifying the data received from the business logic layer and making it presentable to the end user.

User interfaces are in the driving seat of the application. 

**Business Logic**

It forms the core of the application. It's objective is to cater to the requests of user interfaces. Based on the request, it runs some custom logic, gets the resources needed to fulfil the request and answers back in an already agreed upon response format.

Below is a small word cloud of the responsibilities of a business logic layer. The responsibilities can vary from one use case to another.

![Components of Business Logic layer](https://raw.githubusercontent.com/abh1navv/learning-notes/master/microservices/images/business-logic-components.png)

**Backing services**

These are services which support the business logic. They each serve a specific purpose and provide data/services to the application. They interact with the business logic layer and are replaceable as long as the communication contract between the two layers is maintained. A few examples:
1. Data sources
2. Cache aside servers like Redis
3. Notification services
4. Another service like a payment gateway
5. In microservices context, another microservice.

**Note**: The terminology used for this layer is different across the internet but I like to use the term Backing Services to remain consistent with the terminology used by [12-factor app methodology.](https://12factor.net/backing-services)

### Principles



## Problems in traditional software architectures

1. Strong dependencies between layers
2. 



