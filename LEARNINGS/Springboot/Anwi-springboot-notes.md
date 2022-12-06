
# Building Microservices

## What are Micro services?

Microservices are independently releasable services that are modeled around a business domain. A service encapsulates functionality and makes it accessible to other services via networks—you construct a more complex system from these building blocks. Microservices are an architecture choice that is focused on giving you many options for solving the problems you might face.

A single microservice is treated as a black box(Internal implementation details such as way data is stored, code are hidden from outside world). It hosts business
functionality on one or more network endpoints over few protocols.
Microservice architectures avoid the use of shared databases in most circumstances; instead, each microservice encapsulates its own database where required.

SOA(Service oriented Architecture) and Microservices are different. SOA focus on large monolithic applications & promotes reusability of software. It doesn't split system, no communicaiton protocols(SOAP) etc. The microservice approach has emerged from real-world use, taking our better understanding of systems and architecture to do SOA well.
A-microservice-exposing-its-functionality-over-a-REST-API-and-topic

[Microservices1](C:\Users\ANWESH\HOME GIT\throwaway-01\throwaway-01\LEARNINGS\Springboot\Microservices1.PNG)

## KEY CONCEPTS OF MICROSERVICES

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

    ![Capture](https://user-images.githubusercontent.com/110244625/205536751-6b8aab1a-ff7c-408f-93dc-605c9df0c3fc.jpg)

    3tier architecture is old method and changes will need to be managed by each team and deployed in the correct order, as outlined in figure. This architecture has high cohesion of related technology but low cohesion of business functionality.

    We organize them in terms of the way we break our systems apart as there is need to ship software much more quickly these days. A single dedicated team that has full-end-to-end responsibility for making changes to aspects of the customer profile.

    This could be achieved through a single microservice owned by the profile team that exposes a UI to allow customers to update their information, with state of the customer also stored within this microservice. This is a vertical approach.
    
    ![DedicatedMicroservice](https://user-images.githubusercontent.com/110244625/205544497-1060791f-ba01-4e41-a522-dad68c72ab76.PNG)


## THE MONOLITH

1. The Single-Process Monolith

    A system in which all of the code is deployed as a single process, an architecture which makes sense for smaller organizations. Processes such as reading data from or storing data into a database, or pretending information to web or mobile applications.

2. The Modular Monolith

    Each module can be worked on independently, but all still need to be combined together for deployment.

    ![modular-monolith](https://user-images.githubusercontent.com/110244625/205802845-b0b019dd-c756-4590-893e-acdd071647c8.PNG)

    Shopify uses modular monolith. If the module boundaries are well defined, it can allow for a high degree of parallel work, while avoiding the challenges of the more distributed microservice architecture by having a much simpler deployment topology. Databases tend to lack decomposition in code level, pulling apart the monolith is challenge, some tried with database decomposition(having seperate databases for different modules).

3. The Distributed Monolith

    A system with multiple services but entire system must be deployed together which is a disadvantage. This architecture is used in information hiding, cohesion of business functionality.

Monoliths and Delivery Contention

    Delivery contention is many developers wanting to push functionality live at different times and confusion around who owns what and who makes decisions. A microservice architecture does give you more concrete boundaries around which ownership lines can be drawn in a system.


## Advantages of Monoliths


## Enabling Technology

Microservices require an understanding of the supporting technology to such a degree that previous distinctions
between logical and physical architecture can be problematic.

### Log Aggregation and Distributed Tracing

Log aggregation tool is so essential in understanding how system is behaving, that you should consider it a prerequisite for adopting microservices. These systems allow you to collect and aggregate logs from across all your services, providing you a central place from which logs can be analyzed, and even made part of an active alerting mechanism.
Implementing correlation IDs, in which a single ID is used for a related set of service calls. By logging this ID as part of each log entry, isolating the logs associated with a given flow of calls becomes much easier, which in turn makes troubleshooting much easier.
Ex - Jaeger, Lightstep, Honeycomb etc.

### Containers and Kubernetes

Normal virtualization techniques used for microservice instance isolation can be quite heavy when we consider the size of our microservices.
Containers, on the other hand, provide a much more lightweight way to provision isolated execution for service instances, resulting in faster spin-up times for new container instances, along with being much more cost effective for many architectures.
Container orchestration platforms like Kubernetes provide the robustness and throughput your service needs while allowing you to manage underlying containers and use them efficiently. Deploying kubernetes is complex, there is a tradeoff of their adoption.

### Streaming

Organizations are wanting to move away from batch reporting operations and toward more real-time feedback, allowing them to react more quickly. Apache Kafka is choice for straming data in a microservice environment. Kafka has started adding stream-processing capabilities in the form of KSQLDB, but you can also use it with dedicated stream-processing solutions like Apache Flink.

### Public Cloud and Serverless

Google Cloud, Microsoft Azure, and Amazon Web Services (AWS).
Public cloud providers offer a host of managed services, from managed database instances or Kubernetes clusters to message brokers or distributed filesystems.
Function as a Service (FaaS) platforms are of special interest because they provide a nice abstraction around the deployment of code.


## Advantages of Microservices

By combining the concepts of information hiding and domain-driven design with the power of distributed systems, microservices can help deliver gains over other distributed architectures.

### Technology Heterogeneity

For performance, we might decide to use a different technology stack that is better able to achieve the required performance levels. For data, different data tech used to achieve inter-connectedness, profiling etc.
With a system consisting of multiple services, I have multiple new places to try out a new piece of technology. It is easier to manage the risk of upgrades with microservices.

### Robustness

With microservices we can remove problem of bulkheads. A component of a system may fail, but as long as that failure doesn’t cascade, you can isolate the problem, and the rest of the system can carry on working. Service boundaries become your obvious bulkheads.

### Scaling

With smaller services, we can scale just those services that need scaling, allowing us to run other parts of the system on smaller, less powerful hardware & resources.

### Ease of Deployment

With microservices, we can make a change to a single service and deploy it independently of the rest of the system. This allows us to get our code deployed more quickly. If a problem does occur, it can be quickly isolated to an individual service, making fast rollback easy to achieve. It also means that we can get our new functionality out to customers more quickly. This is why Amazon and Netflix use these architectures.

### Organizational Alignment

Microservices also allow us to change ownership of services as the organization changes—enabling us to maintain the alignment between architecture and organization in the future.

### Composability

With microservices, we allow for our functionality to be consumed in different ways for different purposes like web, native application, mobile web, tablet app, or wearable device for customer engagement.


## Microservice Pain Points

Complexity in adopting.

### Developer Experience

More resource-intensive runtimes like the JVM can limit the number of microservices that can be run on a single developer machine. In cloud, feedback cycles can suffer greatly. Limiting the scope of developer is straightforward approach, but collective ownership for one developer who is expected to work on any part of system is problem.

### Technology Overload

Microservices may well give you the option for each microservice to be written in a different programming language, to run on a different runtime, or to use a different database—but these are options, not requirements. You’ll need to spend a lot of time understanding issues around data consistency, latency, service modeling, and the like.

### Cost

You’ll likely need to run more things—more processes, more computers, more network, more storage, and more supporting software & licences fee. A direct slowdown in delivery of new functionality or the need to add more people to offset this cost.

### Reporting

Reporting carried out directly on the database of a monolith. With a microservice architecture, we’ve just made reporting much more difficult, because now our data is scattered across multiple logically isolated schemas. 

Real-time reporting on large volumes of data, can work well with a microservice architecture but typically require the adoption of new ideas and associated technology. 


### Monitoring and Troubleshooting

With a microservice architecture, do we understand the impact if just a single instance of a service goes down?

With a microservice architecture with tens or hundreds of processes, can we say that a single process CPU stuck at 100% and there'll be a problem?

### Security

more information flows over networks between our services which makes data vulnerable. You might need to direct more care to protecting data in transit and to ensuring that your microservice endpoints are protected so that only authorized parties are able to make use of them.

### Testing

In Microservices the scope of our end-to-end tests becomes very large.The testing will cost more but won’t manage to give you the same level of confidence.

### Latency

Information that previously flowed within only a single process now needs to be serialized, transmitted, and deserialized over networks that you might be exercising more than ever before. Latency issue comes out.

### Data Consistency

Whereas in the past you might have relied on database transactions to manage state changes in single database systems, you’ll need to understand that similar safety cannot easily be provided in a distributed system. Adopting an incremental approach to decomposition, so that you are able to assess the impact of changes to your architecture in production, is really important.


## Should I use Microservices?

You need to assess your own problem space, skills, and technology landscape and understand what you are trying to achieve before deciding whether microservices are right for you.

### Whom They Might Not Work For

for brand-new products or startups. This shift in domain models will, in turn, result in more changes being made to service boundaries, and coordinating changes across service boundaries is an expensive undertaking. 

The process of finding product market fit means that you might end up with a very different product at the end than the one you thought you’d build when you started.

It’s much easier to move to microservices later, after you understand where the constraints are in your architecture

### Where they work well

Probably the single biggest reason that organizations adopt microservices is to allow for more developers to work on the same system without getting in each other’s way. Get your architecture and organizational boundaries right, and you allow more people to work independently of each other, reducing delivery contention.

Software as a Service (SaaS) applications are, in general, also a good fit for a microservice architecture. 

These products are typically expected to operate 24-7, which creates challenges when it comes to rolling out changes. The independent releasability of microservice architectures is a huge boon in this area. Furthermore, the microservices can be scaled up or down as required. This means that as you establish a sensible baseline for your system’s load characteristics, you get more control over ensuring that you can scale your system in the most cost-effective way possible.
you might decide to deploy one service as a set of functions, another as a managed virtual machine (VM), and another on a managed Platform as a Service (PaaS) platform.

Microservices provides huge flexibility as you grow, organizing becomes easy, you can get most out of cloud platforms.