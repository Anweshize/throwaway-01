
# Building Microservices

## What are Micro services?

Microservices are independently releasable services that are modeled around a business domain. A service encapsulates functionality and makes it accessible to other services via networks—you construct a more complex system from these building blocks. Microservices are an architecture choice that is focused on giving you many options for solving the problems you might face.

A single microservice is treated as a black box(Internal implementation details such as way data is stored, code are hidden from outside world). It hosts business
functionality on one or more network endpoints over few protocols.
Microservice architectures avoid the use of shared databases in most circumstances; instead, each microservice encapsulates its own database where required.

SOA(Service oriented Architecture) and Microservices are different. SOA focus on large monolithic applications & promotes reusability of software. It doesn't split system, no communicaiton protocols(SOAP) etc. The microservice approach has emerged from real-world use, taking our better understanding of systems and architecture to do SOA well.
A-microservice-exposing-its-functionality-over-a-REST-API-and-topic

[Microservices1](C:\Users\ANWESH\HOME GIT\throwaway-01\throwaway-01\LEARNINGS\Springboot\Microservices1.PNG)

## Key concepts of Microservices

1. Indepandant Deployability

    Make sure our microservices are loosely coupled with stable interfaces else problems from sharing databases will cause problems. 

2. Modeled Around a Business Domain
    By modeling services around business domains, we can make it easier to roll out new functionality and to recombine microservices in different ways to deliver new functionality to our users, our code better represent the real world domain.
    Each layer in architecture represent a different service boundary.
    With microservices we have made a decision to prioritize high cohesion of business functionality over high cohesion of technical functionality. 

3. Owning their own State
   We want to think of our services as end-to-end slices of business functionality that, where appropriate, encapsulate user interface (UI), business logic, and data. This is because we want to reduce the effort needed to change business-related functionality. This gives us high cohesion of business functionality, reduce coupling.

4. Size
    How many microservices can you handle? more services - more complexity of system.
    How do you define microservice boundaries to get most out of them without mess?

5. Flexibility
    Finding a balance between keeping your options open and bearing the cost of architectures like this can be a real art.

6. Alignment of Architecture and Organization
    [3tier-architecture-changes](LEARNINGS\Springboot\3tier-architecture-changes.PNG)
    


