# Xmas topic 

### Index: 

1. [Threading](#Threading) 
2. [Shared state](#Shared-state)
3. [SOLID](#SOLID)
4. [Distributed systems](#Distributed-systems) 
5. [Horizontal scaling](#horizontal-scaling) 
6. [CAP theorem](#CAP-theorem)
7. [Algorithms and data structures](#Algorithms-and-data-structures)



### Topics:

* #### Threading

  Thread is a set of instruction in an application to perform specific task. An application can be composed of several threads and different threads can be executed **"at the same time."** 

  **Example of "at the same time"**: Writing a text document and running spell check as writing, printing elements of the documents and receiving emails.

  1 core CPU: slice CPU resource for each of the thread. Happens fast and creates illusion of multithreading. 

  2 cores CPU: cores are used to split different threads and run at the same time. 

  *Only on a multiple CPU are things happening "at the same time".*

  **Race condition**: accessing data concurrently can cause problems. For example, singleton pattern for instance variable. This issue can be prevented by using **synchronization**. 

  **Locks are Reentrant** : When a thread holds a lock, it can enter a block synchronized on the lock its 	holding

  **Deadlocks**: Both thread are waiting on each other to finish with their key. However the keys never get released. 

  ##### Synchronization : 

  * **Synchronization** needs a special,technical object that will hold key. Eg. Java Object 
  * Instance of a class can be synchronized
  * This key is also called monitor
  * Each thread will take key while operating on the method, other threads wait for the key

  **Runnable** pattern used to lunch threads in java. 

  A Thread executes a task: 

  1) Create an instance of Runnable 
  2) Create an instance of Thread with the task as a parameter 
  3) Lunch the tread. `thread.start()`
  4) *Stop thread : Don't !*  If have to use `interrupt()` to send signal to thread to stop task.

  **Wait / Notify pattern:** 

  * `wait()` and `notify()` are from Object class 
  * `wait()` releases the key held by this Thread. 
  * and puts that thread in WAIT state, 
  * `notify()` releases a Thread in WAIT state and puts it in RUNNABLE state
  * `notifyAll()` release all Threads

  **Thread state:**

  * `NEW` : new thread state

  * `RUNNABLE`: once called start method, thread is set in runnable. 

  * `TERMINATED`: Thread scheduler knows that thread is finished. 

  * `BLOCKED`: waiting at the entrance of synchronized block 

  * `WATING`: parked using wait call, waken by notify call 

  * `TIME_WATING`: parked using sleep(timeout) or wait(timeout) call 

    

  **Synchronization** guarantees the exclusive execution of a block of code 

  **Visibility** guarantees the consistency of the variables. 

  ***"Happens before" link** : exists between all synchronized operations.* `volatile` keyword on variable to create happens before link. 

  

  **How to write correct concurrent code ?** 

  1) Check for race conditions

     1) They occur on fields 
     2) 2 threads are reading/ writing a given field

  2) Check for the happens-before link between read and write operations

     1) Are the read/write volatile ? 
     2) Are they synchronized ? 

  3) Synchronized or volatile ? 

     1) Synchronized = atomicity(not interrupted. ) 

        

* #### Shared state

  A **shared state** is any variable, object, or memory space that exists in a shared scope. Any non-constant variable used by multiple separate scopes, including the global scope and closure scopes, is considered to be in a shared state. In functional programming, shared states should be avoided. A shared state prevents a function from being pure. When the shared state rule is violated and the program modifies a variable, a side effect is created. In OOP, shared states are often passed around as objects. OOP functions may modify the shared state. This is very much against functional programming rules.

  

* #### SOLID

  [Wikipedia](https://en.wikipedia.org/wiki/SOLID)

  ##### ***S**ingle responsibility principle:* 

  Every module class, function should have responsibility over single part of the program functionality and it should encapsulate that part.  "A class should have only one reason to change" - developer should have only one motivation to change it. 

  *Advantage:* A class can be reused in other part of the program. 

  

  ##### ***O**pen closed principle:* 

  States "software entitles" (classes ,modules, functions etc.) should be open for extension but closed for modification. that is such an entity can allow its behavior to be extended without modifying source code. Class should be open to be subclasses to inherit.  Make class final when has to be final for technical reason. For security reason or used widely so behavior is constant. 

  

  ##### ***L**iskov substitution principle:* 

  Substitutability is a principle in [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming) stating that an [object](https://en.wikipedia.org/wiki/Object_(computer_science)) (such as a [class](https://en.wikipedia.org/wiki/Class_(computer_programming))) and a sub-object (such as a class that extends the first class) must be interchangeable without breaking the program. 

  Principle of least of astonishment - classes should be substitutable. Subclass should have similar behavior to superclass and should do what expected.

  

  ##### ***I**nterface segregation principle:* 

  The interface-segregation principle (ISP) states that no code should be forced to depend on methods it does not use. ISP splits [interfaces](https://en.wikipedia.org/wiki/Interface_(computing)) that are very large into smaller and more specific ones so that clients will only have to know about the methods that are of interest to them. Such shrunken interfaces are also called *role interface*s. ISP is intended to keep a system decoupled and thus easier to refactor, change, and redeploy.

  Eg. One interface for: Customer, Orders, Warehouse should be split into three different interfaces so when implementing customer class, it doesn't contain empty methods that are used in order classes. 

  *DON'T COMBINE INTERFACES TOGHETHER*

  

  ##### ***D**ependency inversion principle:*

  The dependency inversion principle is a specific form of [loosely coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming)) software [modules](https://en.wikipedia.org/wiki/Modular_programming). When following this principle, the conventional [dependency](https://en.wikipedia.org/wiki/Dependency_(computer_science)) relationships established from high-level, policy-setting modules to low-level, dependency modules are reversed, thus rendering high-level modules independent of the low-level module implementation details. The principle states:[[1\]](https://en.wikipedia.org/wiki/Dependency_inversion_principle#cite_note-Martin2003-1)

  1. High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).

  2. Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

     

* #### Distributed systems

  Simply put: Distributed system is a number of application that are all linked together via network like a microservices architecture. 

  A distributed system is a computing environment in which various components are spread across multiple computers (or other computing devices) on a network. These devices split up the work, coordinating their efforts to complete the job more efficiently than if a single device had been responsible for the task.

  Distributed systems are an important development for IT and computer science as an increasing number of related jobs are so massive and complex that it would be impossible for a single computer to handle them alone. But distributed computing also offers additional advantages over traditional computing environments. 

  Distributed systems **reduce** the risks involved with having a single point of failure, bolstering reliability and fault tolerance. Modern distributed systems are generally designed to be scalable in near real-time; also, you can spin up additional computing resources on the fly, increasing performance and further reducing time to completion.

  Historically, distributed computing was expensive, complex to configure and difficult to manage. But thanks to software as a service (SaaS) platforms that offer expanded functionality, distributed computing has become more streamlined and affordable for businesses large and small. As a result, all types of computing jobs — from database management to video games — use distributed computing. In fact, many types of software, such as cryptocurrency systems, scientific simulations, blockchain technologies and AI platforms, wouldn’t be possible at all without these platforms.

  

* #### Horizontal scaling

  Simply put: **Horizontal** scaling adds more machines to the resource pool where as vertical scaling adds more power CPU RAM to existing machines. 

  Horizontal scaling simply adds more instances of machines without first implementing improvements to existing specifications. By scaling out, you share the processing power and load balancing across multiple machines.

  Horizontal scaling means adding more machines to the resource pool, rather than simply adding resources by scaling vertically. Vertical scaling gives you the ability to zoom in to add more servers to your network, but it also requires you to zoom out by adding a bit more power, CPU, and RAM to the existing infrastructure. Scaling horizontally is the same as scaling by adding more machines to a pool or resources — but instead of adding more power, CPUs, or RAM, you scale back to existing infrastructure. Horizontal scaling allows you to scale your data with more resources than you can add resources using vertical scaling.

  

* #### Cap Theorem

  * **C**onsistency : All reads receive the most recent write or an error.
  * **A**vailability : All reads contain data, but it might not be the most recent 
  * **P**artition tolerance : The system continues to operate despite network failures (dropped partitions, slow network connections, or unavailable network connections between nodes ) 

  Normally, data stores provides all three functions, but the CAP theorem maintain that when distributed database experiences a network failure, you can provide either consistency or availability. 

  It’s a tradeoff. All other times, all three can be provided. But, in the event of a [network failure](https://www.bmc.com/blogs/mtbf-vs-mtff-vs-mttr-whats-difference/), a choice must be made.

  In the theorem, [partition tolerance is a must](https://codahale.com/you-cant-sacrifice-partition-tolerance/). The assumption is that the system operates on a distributed data store so the system, by nature, operates with network partitions. Network failures will happen, so to offer any kind of reliable service, partition tolerance is necessary—the P of CAP.

  When a network failure happens, one can choose to guarantee consistency or availability:

  - High consistency comes at the cost of lower availability.
  
  - High availability comes at the cost of lower consistency.
  
    

* #### Algorithms and Data structures: 

  Info: https://medium.com/techie-delight/top-algorithms-data-structures-concepts-every-computer-science-student-should-know-e0549c67b4ac
