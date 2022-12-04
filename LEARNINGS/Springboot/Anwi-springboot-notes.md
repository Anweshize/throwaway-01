
# Building Microservices

## What are Micro services?

Microservices are independently releasable services that are modeled around a business domain. A service encapsulates functionality and makes it accessible to other services via networks—you construct a more complex system from these building blocks. Microservices are an architecture choice that is focused on giving you many options for solving the problems you might face.

A single microservice is treated as a black box(Internal implementation details such as way data is stored, code are hidden from outside world). It hosts business
functionality on one or more network endpoints over few protocols.
Microservice architectures avoid the use of shared databases in most circumstances; instead, each microservice encapsulates its own database where required.

SOA(Service oriented Architecture) and Microservices are different. SOA focus on large monolithic applications & promotes reusability of software. It doesn't split system, no communicaiton protocols(SOAP) etc. The microservice approach has emerged from real-world use, taking our better understanding of systems and architecture to do SOA well.

[A-microservice-exposing-its-functionality-over-a-REST-API-and-topic](C:\Users\ANWESH\HOME GIT\throwaway-01\throwaway-01\LEARNINGS\Springboot\Microservices1.PNG)

## Key concepts of Microservices

1. Indepandant Deployability

    Make sure our microservices are loosely coupled with stable interfaces else problems from sharing databases will cause problems. 

2. Modeled Around a Business Domain
    By modeling services around business domains, we can make it easier to roll out new functionality and to recombine microservices in different ways to deliver new functionality to our users.


