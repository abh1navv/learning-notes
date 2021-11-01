# Hexagonal Architecture

In the evolution of software architecture, [loose coupling](https://en.wikipedia.org/wiki/Loose_coupling) has been at the centre. There is an emphasis on breaking applications into components which can be switched, replaced or updated without affecting the dependent components.

Hexagonal architecture is another advancement in loosely coupled architectures. It originated around the beginning of the shift to domain-driven designs and formed a basis of further advancements in the field of software design. 

## Intoduction

A hexagonal architecture is divided into three parts and defines the strict roles that these parts play within the application.

![Hexagonal architecture layers - User Interfaces, Business Logic and Data sources](https://raw.githubusercontent.com/abh1navv/learning-notes/master/microservices/images/hexagonal-intro.jpg)

**User Interfaces**

There can be many user interfaces to a backend - mobile apps, web apps, desktop softwares, etc. They will all get their resources from the Business logic layer.

**Business Logic**

It forms the core of the application. It's objective is to cater to the requests of user interfaces. Based on the request, it runs some custom logic, gets the resources needed to fulfil the request and answers back in an agreed upon response format.

Below is a small word cloud of the responsibilities of a business logic layer. The responsibilities can vary from one use case to another.

![Components of Business Logic layer](https://raw.githubusercontent.com/abh1navv/learning-notes/master/microservices/images/business-logic-components.png)

**Backing services**

These are services which support the business logic. They each serve a specific purpose and provide data/services to the application. They interact with the business logic layer and are replaceable as long as the communication contract between the two layers is maintained. A few examples:
1. Data sources
2. Cache aside servers like Redis
3. Notification services
4. Another service like a payment gateway
5. In microservices context, another microservice.

### Intent and principles

The intent is to make the core of our application immune to changes in the communication with other layers. Those concerns are to be handled at the boundary of our hexagon.

![Ports and adapters](https://raw.githubusercontent.com/abh1navv/learning-notes/master/microservices/images/ports-and-adapters.jpg)

**Ports**

Ports are what our core application interacts with. Ports stay consistent for the inner application no matter what happens outside them. They are *interfaces* that the inner components interact with without knowing whats being plugged into them.

**Adapters**

Ports are staying consistent but we still want to be able to plug multiple applications to them when needed. These applications could have different needs and may not comply with the interface defined by the ports. This is where out adapters come in. Their purpose is to convert the data provided by the outer applications into a format digestible for the inner application.



**Note** - Hexagonal is just a term that has stuck with the architecture for simplicity. It is not to be misunderstood as the business logic layer having 6 ports. There can be many more sides to the polygon as per the services required to connect

## Example

Imagine a small application - a REST API which deals with user related details. One of its methods returns user details based on user id provided in the request.

### Code examples






