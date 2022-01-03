# REST APIs

#### What is REST API ? 

REST API is curd interface using HTTP and JSON. Total independence between client and server as all languages support HTTP. URL should contain a noun at the end point after the root.  

Eg. `hostname/employees?emp_id=1234` or `hostname/employees/1234`

GET : Select 
POST : Insert 
PUT: Update if exists, otherwise Insert
PATCH: Update if exists only. 



#### Types of java:

* Standard Edition of Java:  Desktop version 

* Micro Edition of Java: Devices with small capacity, embedded systems/

* Enterprise Edition Java: Standard configuration to run server side applications



#### What is Spring ?

* Spring runs in application server like Apache Tomcat, oracle application server etc. 

* Spring is a plugin to java EE to make it simpler for developing java application.
* **Spring** provides with standard model-view-controller implementation by configuring using xml file and adding model classes to demonstrate process. Provides dispatch controller and decides which code to call. 
* **Spring boot** is a evaluation of **spring** doesn't require to configure application as it comes with default configuration settings. Easier version of spring which allows rapid application development
* Spring uses aspect-oriented programming AspectJ technology. Calls method under specific circumstances by using notation. For example after or before. 



#### Spring @notations

`@RestController`-  identifier for HTTP request which are handled by a controller

`@ResponseStatus(code= HttpStatus.I_AM_A_TEAPOT)` - Set status code of a HTTP GET request. 

`@Autowired`- annotations-driven dependency injection. It allows spring to resolve and inject collaborating beans into our bean. 

##### GET

`@GetMapping(value = "noun for HTTP request")` - annotation for mapping HTTP GET requests onto specific handler methods

`@RequestParam` - annotation which indicates that a method parameter should be bound to a web request parameter.

`@PathVaraiable` - its same as `@RequestParam` however it doesn't require to specify parameter name in the web request URL.

`@ResponeBody` - 

##### POST

`@PostMapping(value = "noun for HTTP request")`- identifier for HTTP post request which needs to have `@RequestBody`. 

`@RequestBody` to interpret JSON body as java object. Allows to specify where the data should be stored as java object



#### What is Hibernate?

**Hibernate ORM** (or simply **Hibernate**) is an object–relational mapping tool for the java programming language. It provides a framework for mapping an object-oriented domain model to a relational database Hibernate handles object–relational impedance mismatch problems by replacing direct, persistent database accesses with high-level object handling functions.



