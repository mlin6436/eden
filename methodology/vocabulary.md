# Vocabulary

There are always some self-declared rock star devs enjoy using a butt load of acronyms and jargons, it is easier to know what they are on about than to be left out.

### YAGNI

You Are Not Going To Need It – The issue hare is that far more code is written than necessary to solve or deliver application functionality.

Symptoms: Added unused finder methods to session beans in Java EE.

### DRY

Don't Repeat Yourself - writing code that has lot of duplication across methods, classes, packages and package object.

Symptoms: Copy & Paste coding in unit tests and repeated metadata in entity and the front end.

### KISS

Keep It Simple Silly [or Stupid] – a mantra to describe writing only code to solve the function problem instead of writing a less complicated codeAlso see Occam's Razor.

Symptoms: Too many abstract layers in a software application.

### WET

Write Every Time – the antithesis to DRY, where code is deliberately written that repeats lots and lots of time in different classes, packages, and functions.

Symptoms: Deciding to do things your way and instead of collaborating with the other developers and finding some common ground.

Antidote: DRY, Unit Tests and REFACTORING.

### WETTT

Write Everything Ten Thousand Times – the hyperbole colloquial version of WET.

### R3

Rules of Three – This is not the proprietary operating system of the same name, or the classic 1980's arcade game, or either the description of a maxed out pimp-my-ride Volkswagen Golf; but the idea that when ever you have three duplicated parts of code in a method, function or classes then it is time to refactor the duplication in to single method.Related to DRY and WET.

Symptoms: Ignoring the code repeats because of time pressures, or the SCRUM master says no, don't do it in this sprint.

### DBC

Design By Contract – the idea of building a service from a contract first. In Java you write the interface as simply as possible and then secondly worry about the implementation class.Interfaces are easier to refactor around and because you can plug different implementations into the interface you get higher cohesion and lower coupling.

Symptoms: JDBC specification since version 1.0. There are tons of implementations for different relational databases including MySQL, Postgres, H2, Derby etc. Every Java programmer knows how to code against JDBC because that they don't have to fight with an different implementation, which vary, because the DBC implied it will do the right thing most of the time. Also related to standardisation of application programming interfaces.

### BDUF or BUDF

Big Up-Front Design – a problem with many large corporate institutions that sometimes require a 100 – 1000 page document full of business requirement before any software construction gets the green lightSome poor architect or business analyst will have spent weeks investigating and chatting to the business about the requirement, only for the development team to say the document is practically worthless.

Antidote: Get the technical lead and some key developers talking with the business and the analysts and the customer. Ideation sessions everybody!

Symptoms: Waterfall methodology and aspects of the investment banking IT culture.

Antidote: Unknown, lots of people how tried to bring “Agile” with both a big A and small A to many of these institutions with some success and failure.

### Pink Book

Describes the book with a Pink Cover called Extreme Programming Installed by Ron Hendries et AlI do not recommend this for new starters unless for reference, since the Pink Book is now rather old, 2000, there are other more recent Agile development books and courses that help new Java developers.

### YOLO

You Only Load It Once [If Ever] – this is related to fact that you want to have a single source of truth in an application system. This is problem of mis-architecture, where someone has not thought the functional requirement through enough.

Symptoms: Shopping Cart Service EJB – you only ever want one implementation of the pay-point in an application, albeit you will have many pay-point providers (credit and debit card third parties and PayPal) The If-Ever part is YOLO and YAGNI added together. You are not sure of the another part of the system loads the data, so you decide to keep the component. (You probably want to put a logging client on the YOLOIF thing so that you can effectively decide to chuck the component if nobody has used the function in 12 or 18 months time.)

Digression: If you have find data that is constantly being uploaded to serve a web request then perhaps it really needs caching and not YOLO.

### Spike

A quick exploration of coding in Sprint in SCRUM methodology. In Spike you are probably are looking an new API, like a cloud service or user interface API like JavaFX or similar and basically you explore if the function can implemented relatively well in the new API. In short, you are trying to build some confidence in a new area before committing yourself and other resources to it. Spikes are usually contained and protected from the flow of the critical path and restricted to a time length. See SMART goals.

Symptoms: Adopting a build system – moving from Apache Ant to Maven; moving from Subversion to Git; Adopting a new open source library.

### TDD

Test Driven Development – often conflicted as not being fully explained as a change of discipline and mind. You are only ever doing one of these four things: writing unit tests, writing production code, refactoring unit tests, and refactoring production code; and never doing more than one at these previous at the same time.

### TFD

Test First Development – builds on the ideas of TDD and then extends the discipline to writing unit test code before any production code. Once you have a brand new unit test written completely, then you making sure that new unit test(s) actually fail in order to switch over to writing production code ensures the the new test passes. After you have done that you refactor the tests. Run all tests for all the green bars. Refactor the production code and runs the tests for all the green bar. Repeat: Go back to the start; write a new unit to that will check validate operation of the next function for the application. Repeat with the same formula as above.

### Velocity

A very basic measurement on the Return-on-Investment for SCRUM software development and it has nothing at all to do with financial budgets and reporting. Velocity is the number of story points completed per team per iteration. To the SCRUM experienced: Velocity is equal to the aggregated units of work completed over aggregated time intervals, which implies you measure each progress of tasks in two or more sprints.

### Story Point

For each user story in the sprint or task, predict how hard it is to implement by using unit of reference. Story points are usually written in Fibonacci numbers: 0, 1, 1, 3, 5, 8, 13, 21, 34, 55, 89, 144. Every agile team in the world has a definition of a user story unit point. Teams decide on the backlog items in order to come up with predictions and these joint predictions every member of team go to decide what should applied to the next sprint.

### DTSTTCPW

Do The Simplest Thing That Could Possibly Work – Related to Spike and KISS in many ways. If you are pressed for time and some trading systems developers in investment bank are then this is your working life. DTSTTCPW certainly invites team collaboration and effective sound-boarding from other developers and members of the team, otherwise you are asking for trouble.

### VoC

Voice of the Customer – This is a term from SCRUM methodology, but I am about 20% unsure about this one; I believe 80% of the time to mean a proxy, a placeholder, for the real customer, the person who understands the business requirement and will of the customer. Because the true user is unavailable for some reason due to authority, culture or organisation, or even geo-location. Some people have amusing called this abbreviation, the Voice of Reason, especially when they do not enjoy working with the customer directly.

### Unit Test

In Java programming, a Unit Test is a Java JUnit framework test class or TestNG framework test class that specifically verified and validates a single function of work in an applicationA unit test requires a target, which can be a Java Class, a Service Bean, Managed Bean or something implements the said functionality. Unit test are often seen as low-level fast and efficient tests.

### Functional Test

A functional test is a larger test, which can also be a unit test, designed to test packages of classes or sub part of the overall application infrastructure. Functional test validates if the application meets one of the customer's external requirements on performance, results and efficiency.

Symptoms: a functional test is not necessarily a unit test, and not all functional tests are acceptance tests.

### Acceptance Test

An acceptance test is the same as a functional test in name only. Acceptance tests are those where the customer wants to see the validation pass in order they sign of the implementation.

Symptoms: If the customer is dissatisfied with the application at demonstration time, then at least the one of the acceptance test is broken. Add one in the next sprint.

### SOLID

A set of five principles: Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation and Dependency Inversion.

### Single Responsibility Principle

An object class, a service bean, web service, a function or procedure should have only one single responsibility.

Symptoms: It is hard to write unit test for complex object, because it doing WETTT

### Open Closed Principle

Open for extension and closed for modificationIt means you can subclass the object, but the object is encapsulated by not allowing an outside object to gainfully change the internals.

Symptoms: leakage in object implementation, hard code dependency, and not working with Java interfaces (or interface like constructs i.e. Scala traits and mix-ins)

### Liskov Substitution Principle

Idea of swap-ability and is expressed as a Design By Contract (DBC). I can swap in another object X which is an implementation of T if that objects is a type of T and the overall application works. This is the basis of mocking objects, mocking implementation frameworks; testing in general; proxy remote objects, persistence capable objects; application server and lifecycle monitoring situations; plug-and-play and restartable applications. I could go on, but I won't.

### Interface Segregation Principle

A service interface that does only single specific functional thing is better than a service interface that does several different things.

Symptoms: Failure to adhere to the KISS principle. In days gone, the non standard C++ String libraries where everybody threw in the kitchen sink of methods for any operation that one would want to write that manipulated a C/C++ String (char*).

### Dependency Inversion Principle

Idea of not hard-wiring a direct relationship to a dependent into object. In Java EE world, you would use a dependency injection container such as CDI to inject different managed beans into a service bean. Dependency inversion also should mean in my humble opinion given up on managing the life-cycle of service components and beans. The lifecycle is managed by the application container, the cloud provider or whatever it is you are using. In another school of thought: every application is managed these days, whether it is the operating system, a virtual machine or web container or mobile platform (iOS and Android). This is the way forward.

### Design Patterns

A classic book on Design Patterns by Erich Gamma et Al.Ask your local technical leader to lend you his or her copy of the book; and if they don't have a copy then that really sucks. Tell them to give a training budget and buy the book yourself!

### ACID

ACID (Atomicity, Consistency, Isolation, Durability) is a set of properties that guarantee that database transactions are processed reliably.

### 1NF

First normal form (1NF) is a property of a relation in a relational database. A relation is in first normal form if the domain of each attribute contains only atomic values, and the value of each attribute contains only a single value from that domain.

### 2NF

Second normal form (2NF) is a normal form used in database normalisation. A table is in 2NF if and only if it is in 1NF and every non-prime attribute of the table is dependent on the whole of every candidate key.
