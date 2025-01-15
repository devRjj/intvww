# What is Spring Framework?

Spring  is a lightweight, loosely coupled and integrated framework for developing enterprise-level Java applications. It provides infrastructure support to develop Java applications, offering features such as dependency injection, transaction management, and aspect-oriented programming.

**Loose coupling:**

* Loose coupling is a design principle where components or classes have minimal dependencies on each other. In a loosely coupled system, one component can change without impacting others, making the system more flexible, easier to maintain, and testable.  
* **Example:** In Spring, loose coupling is achieved through **Dependency Injection** (DI). 

**Tightly Coupled:**

* In a tightly coupled system, components or classes are highly dependent on each other. Changes in one class can have a direct impact on others, making the system harder to maintain, test, or extend.   
* **Example** if a method in one class directly creates an instance of another class, these classes are tightly coupled.

### **What is the role of IOC containers in spring?**

* ### The IoC container in Spring is responsible for creating and managing the objects in your application, as well as injecting their dependencies. This promotes loose coupling, making your code more modular, testable, and maintainable.

* Manages their complete life cycle.

### **Inversion of Control (IoC) in Spring:**

It is the core principle of the Spring Framework that shifts the control of object creation and management from the application code to the Spring container. Instead of the application code creating and managing its dependencies, the Spring container is responsible for injecting the required dependencies into the objects.

**Example**: When you use Dependency Injection (DI) in Spring, the framework takes care of injecting the dependencies into a class, rather than the class creating them itself.

### **What is dependency injection?**

* Spring uses Dependency Injection to manage the dependencies between the classes instead of creating objects manually.  
* The process of injecting one class object into another class object is called DI.  
* There are three types of dependency injection: Setter based injection, Constructor based injection, and Field base injection.

### **Types of Dependency Injection in Spring?**

* **Constructor Injection:**   
  * Dependencies are injected through a class constructor. Dependencies are provided at the time of object creation.  
  * It does not allow for partial dependency injection, meaning all dependencies need to be injected at the time of object creation.  
  * Preferred for ensuring that all necessary dependencies are injected.

			**public class MyService {**  
	**private final MyRepository repository;**

	**public MyService(MyRepository repository) {**  
    		**this.repository \= repository;**  
	**}**  
	**// ... service methods**  
**}**

* **Setter Injection:**   
  * Dependencies are injected through setter methods. Objects are created first, and dependencies are set later.  
  * Allows for partial dependency injection, means not all dependencies need to be injected at the time of object creation.   
  * Less preferred when immutability is required.  
  * Dependencies are provided directly into fields using annotations like @Autowired  
    	**public class MyService {**

    	**private MyRepository repository;**  
      
    	**public void setRepository(MyRepository repository) {**  
        		**this.repository \= repository;**  
    	**}**  
    	**// ... service methods**  
    **}**  
* **Autowiring:**  
  * Autowiring is a Spring feature that automatically injects dependencies into a bean, reducing the need for explicit configuration.  
  * Example: suppose I  have two classes Employee and Address both are dependent on each other so in that case we should go for the autowiring concept.

    **public class MyService {**

    	**@Autowired**

    	**private MyRepository repository;**

    	**// ... service methods**

    **}**

### **What is a Spring Bean?**

A Spring Bean is an object managed by the Spring IoC container. Spring beans    are instantiated, configured, wired, and managed by the Spring IOC container. based on the configuration provided through XML, annotations.

**Scope of a Bean in Spring?**  
The **scope** of a bean in Spring defines the lifecycle and visibility of that bean within the Spring container. The scope determines how and when the bean is created, as well as how it is shared within the application. The most common scopes are:

* **Singleton :** It is the default scope. A single instance of the bean is created per Spring container, and this instance is shared across the entire application.  
* **Prototype :** A new instance of the bean is created each time when requested.  
* **Request :**A new bean instance is created per HTTP request.  
* **Session :** A new bean instance is created per HTTP session.  
* **GlobalSession :** A single instance of the bean is created for the global HTTP session (used in portlet applications).

## **What is Spring Boot?**

* Spring Boot is a framework that simplifies the development of Spring applications by providing default configurations, an embedded server and a variety of tools for microservices, web applications, and RESTful services.  
* It eliminates the need for boilerplate code and configuration, making development faster and easier.

### **Main features of Spring Boot?**

* **Auto-Configuration:** Automatically configures Spring components based on the classpath contents.  
* **Spring Boot Starters:** Pre-built configurations for commonly used libraries to streamline dependency management.  
* **Embedded Servers:** Integrates embedded servers like Tomcat, Jetty, and Undertow.  
* **Actuator:** Provides built-in tools for monitoring and managing the application, such as health checks and metrics.  
* **Spring Boot CLI:** A command-line tool for quickly developing Spring applications.  
* **Rapid Application Development** : Spring boot provides Rapid Application Development (RAD) features to the spring framework for faster application development.

### **Difference between Spring and Spring Boot?**

| Spring | Spring Boot |
| ----- | ----- |
| Spring is an open-source lightweight framework mainly used to develop java enterprise applications. | Spring Boot is built on top of the spring framework, mainly used to develop RESTful  APIs and microservices. |
| The most important feature of the Spring Framework is dependency injection. | The most important feature of the Spring Boot is Autoconfiguration. |
| It helps to create a loosely coupled application. | It helps to create a stand-alone application. |
| To run the Spring application, we need to set the server explicitly. | Spring Boot provides embedded servers such as Tomcat and Jetty etc. |
| To run the Spring application, a deployment descriptor is required. | There is no requirement for a deployment descriptor. |
| Spring framework requires too many lines of code(boilerplate code) even for minimal tasks. | It reduces the lines of code. |
| It doesn’t provide support for the in-memory database. | It provides support for the in-memory database such as H2. |
| Developers need to write boilerplate code for smaller tasks. | In Spring Boot, there is reduction in boilerplate code. |
| Developers have to define dependencies manually in the pom.xml file. | pom.xml file internally handles the required dependencies. |

### **What are Spring Boot starters? Name a few commonly used starters.**

*  Spring Boot Starters are dependency descriptors that aggregate commonly used dependencies into a single one. For example, \`spring-boot-starter-web\` includes dependencies for Spring MVC, embedded Tomcat, and more, simplifying the setup process.  
* Common starters include:  
  * spring-boot-starter-web for building web applications.  
  * spring-boot-starter-data-jpa for working with JPA and relational databases.  
  * spring-boot-starter-security for adding security to applications.  
  * spring-boot-starter-test for testing support.

### **How does Spring Boot handle dependency management?**

* Spring Boot manages dependencies using a parent pom.xml file.

### **What is the purpose of the application.properties or application.yml file in Spring Boot?**

* The application.properties or application.yml file is used to externalize configuration in a Spring Boot application. It allows developers to define settings such as database connections, server ports, logging levels, and custom application properties.

### **How do you configure a Spring Boot application?**

* A Spring Boot application can be configured using:  
  * **Properties/YAML Files**: application.properties or application.yml files.  
  * **Command-Line Arguments:** Pass key-value pairs as command-line arguments.  
  * **Environment Variables:** Define properties as environment variables.  
  * **Java Configuration:** Use @Configuration classes to define beans and settings programmatically.

### **How can you define different profiles in Spring Boot, and why would you use them?**

* Profiles in Spring Boot are used to define different configurations for different environments (e.g., development, testing, production). You can define profiles using the @Profile annotation or by setting spring.profiles.active in application.properties or via environment variables.

### **What is Spring Boot Actuator, and what is it used for?**

* Actuator provides built-in tools for monitoring and managing the application, such as health checks and metrics.  
* It helps in monitoring and managing a Spring Boot application via endpoints like \`/actuator/health\`.

### **What is Spring Boot dependency management?**

* Spring Boot manages dependencies and configuration automatically. You don't need to specify a version for any of those dependencies.  
* Spring Boot upgrades all dependencies automatically when you upgrade Spring Boot.

### **How to connect Spring Boot to the database using JPA?**

* Spring Boot provides spring-boot-starter-data-jpa to connect Spring applications with relational databases efficiently.

### **How does Spring Boot handle externalized configuration?**

* Spring Boot supports externalized configuration through properties and YAML files, environment variables, command-line arguments, and more.  
* These configurations can be specified in \`application.properties\` or \`application.yml\` files

### **What is the difference between \`@RestController\` and \`@Controller\`?**

* @RestController is a stereotype and class-level annotation. It is used to define a class as a RESTful controller.  
* @RestController is a specialized version of @Controller that combines @Controller and @ResponseBody.  
* It is used to create RESTful web services and returns data directly from the method rather than rendering a view.

### **What are the benefits of using Spring Boot DevTools?**

* Spring Boot DevTools provides features like automatic restarts, live reload, and configurations specific to the development environment,

### **What is the use of Spring Boot Profiles?**

* Spring Boot Profiles allow you to segregate parts of your application configuration and make it environment-specific.   
* For example, you can have different configurations for development, testing, and production environments.

### **How do you implement exception handling in Spring Boot?**

*  Exception handling in Spring Boot can be implemented using @ControllerAdvice and @ExceptionHandler annotations.   
* @ControllerAdvice is used to define global exception handlers, and  it is class level annotation  
* while @ExceptionHandler is used for handling specific exceptions and it is a method level annotation.  
* First of all I created an ErrorDetails class with some fields like error msg, error details and timestamp.  
* After that I create a GlobalExceptionHandler class annotated with @ControllerAdvice annotation,  this class will act as a catch block.   
* Then I extended this class with ResponseEntityExceptionHandler class, this class comes in the spring framework.  
* Then I created a method in this class which is annotated with @ExceptionHandler annotation which is used for handling specific exceptions.  
* And the return type of this method should always be ResponseEntity.

### **What is Spring Boot's auto-configuration?**

* Auto-configuration automatically configures your Spring application based on the dependencies present on the classpath.  
* It reduces the need for explicit bean configuration, allowing the developer to focus on writing business logic.

### **How does Spring Boot support database operations?**

* Spring Boot supports database operations through Spring Data JPA, JDBC, and other data access technologies.

### **What is the significance of \`application.properties\` and \`application.yml\`?**

* \`application.properties\` and \`application.yml\` are used to externalize configuration parameters in a Spring Boot application.   
* These files contain key-value pairs or YAML-based configurations that can be used to configure the application’s behavior.

### **Annotations used in Controller Class.**

**@RestController**

* @RestController is a stereotype and class-level annotation. It is used to define a class as a RESTful controller.  
* It is a specialized version of \`@Controller\` used in RESTful web services. It combines \`@Controller\` and \`@ResponseBody\`,   
* It is used to create RESTful web services and returns data directly from the method rather than rendering a view.

**@RequestMapping**

* Used to map web requests to specific handler classes or methods. It can be applied at the class level to specify a base URL, and at the method level to handle specific HTTP methods (e.g., GET, POST).  
* @GetMapping\`, \`@PostMapping\`, \`@PutMapping\`, \`@DeleteMapping\`, \`@PatchMapping\`These are shortcuts for \`@RequestMapping\` with specific HTTP methods:  
  * @GetMapping\` for GET requests.  
    * The @GetMapping annotation in Spring is used to map HTTP GET requests onto specific handler methods in a controller. It is a specialized version of the @RequestMapping annotation, which is typically used for retrieving data.  
  * @PostMapping\` for POST requests.  
    * The @PostMapping annotation in Spring is used to map HTTP POST requests to specific handler methods in a controller. It is a specialized version of the @RequestMapping annotation, which is typically used for creating or submitting data.  
  * @PutMapping\` for PUT requests.  
    * The @PutMapping annotation in Spring is used to map HTTP PUT requests to specific handler methods in a controller. It is typically used to update existing resources.  
  * @DeleteMapping\` for DELETE requests.  
    * The @DeleteMapping annotation in Spring is used to map HTTP DELETE requests to specific handler methods in a controller. It is typically used to delete resources.  
  * @PatchMapping\` for PATCH requests.  
    * The @PatchMapping annotation in Spring is used to map HTTP PATCH requests to specific handler methods in a controller. It is typically used to partially update an existing resource.

**@PathVariable**

* Used to extract values from the URL path and map them to method parameters.

**@RequestParam**

*  Used to extract query parameters from the URL. It maps the value of a request parameter to a method parameter. 

**@RequestBody**

* @RequestBody is an annotation in Spring Boot used to bind the HTTP request body to a method parameter.   
* It is commonly used in RESTful APIs to map the incoming JSON request payload to a Java object.

### **PUT vs. PATCH:**

* **@PutMapping:**   
  * Used to update or replace an entire resource. When a PUT request is made, the entire resource is replaced with the data provided in the request.  
  * PUT operations are idempotent, meaning multiple identical requests will have the same effect.  
* **@PatchMapping:**   
  * Used to partially update a resource. PATCH requests modify only specific fields of a resource.  
  * PATCH is not necessarily idempotent; repeated requests may yield different results.

### **What is the difference between application.properties file and applications.yml file?**

* application.properties: Uses a simple key-value pair format  
* application.yml: Uses YAML format, which is more hierarchical and human-readable.

### **Annotations**

**@Autowired**

* The @Autowired annotation in Spring is used for dependency injection.  
* It allows spring to automatically inject the required bean into a class, either through fields, methods, or constructors. 

**@Component**

* It is a stereotype annotation and class level annotation.  
* The @Component annotation in Spring is used to define a class as a Spring bean.  
* It enables spring to automatically detect and manage instances of this class and makes them available for Dependency injection.  
* It is defined as a class as a spring bean for spring ioc container for dependency injection.

**@Service**

* A specialization of @Component used to mark a class as a service provider. It indicates that the class contains business logic and should be managed by Spring's IoC container.

**@Repository**

*  A specialization of \`@Component\` used to indicate that the class is a data access object (DAO) and responsible for interacting with the database.

**@Configuration**

* @Configuration is a class level annotation indicating that an object is a source of bean definition.  
* This is often used to define custom configurations.

**@Bean**

* The @Bean annotation in Spring is used to declare a method that returns a Spring bean and is used for manual bean creation and configuration.  
* It is a Method level annotation.

**@Transactional**

* The @Transactional annotation in Spring is used to manage transaction boundaries in a method or class.   
* The @Transactional annotation in Spring manages transaction boundaries automatically, ensuring that a series of database operations are executed in a single transaction.  
*  If any operation within the transaction fails, the entire transaction is rolled back to maintain data integrity, so it maintains data consistency.

**@ControllerAdvice**

* It is a class level annotation.  
* The @ControllerAdvice annotation in Spring is used to handle exceptions globally across the entire application.

**@ExceptionHandler** 

* It is a method level annotation.  
* It is used to handles exceptions for specific controllers or methods

**@Value** 

* We can use @Value annotation at the field level to inject values into fields, method level to inject values into method parameters and constructor level to inject values into constructor parameters.

**@Query** 

* The @Query annotation is a method-level annotation.  
* The @Query annotation in Spring Data JPA is used to create custom queries for repository methods.

**@Qualifier** 

* The @Qualifier annotation in Spring is used to resolve ambiguity when multiple beans of the same type are available for dependency injection.   
1. It allows you to specify one bean name in @Qualifier then that bean will be injected.

**@Primary**

* When multiple beans of the same type are present, @Primary marks one bean as the default choice to be injected.  
* It helps to resolve ambiguity by marking one bean as the default choice for injection.

### **What is @PathVariable and @RequestParam used for?**

* @PathVariable is used to extract values from the URI path (e.g., /resource/{id}),  
* while @RequestParam is used to extract query parameters from the URL (e.g., /resource?id=123).  
* Both annotations help in capturing request data and passing it to the controller methods.

### **What are Idempotent operations and why are they important in REST?**

* Idempotent operations are those that produce the same result no matter how many times they are performed.  
* In REST, HTTP methods like GET, PUT, and DELETE are considered idempotent, meaning multiple identical requests should have the same effect as a single request.

### **How do you handle pagination in Spring Boot RESTful services?**

* Pagination in Spring Boot can be handled using Spring Data JPA’s Pageable and Page interfaces.  
* By passing Pageable parameters to repository methods, you can retrieve paginated results and return them to the client with metadata like total pages and current page.

### **How do you implement security in RESTful web services using Spring Boot?**

* Security in RESTful web services can be implemented using Spring Security. Common practices include :  
* Basic Authentication: Simple authentication using username and password.  
* OAuth2/JWT: Token-based authentication for stateless security.  
* Role-Based Access Control (RBAC): Restricting access based on user roles and authorities.

### **What is @RequestMapping and how does it differ from @GetMapping and similar annotations?**

*  @RequestMapping is a versatile annotation used to map HTTP requests to handler methods of MVC and REST controllers.  
* It can handle all HTTP methods, while @GetMapping, @PostMapping, @PutMapping, and similar annotations are more specific and map only to the corresponding HTTP methods (GET, POST, PUT, etc.).

### **How do you handle exceptions in a RESTful web service using Spring Boot?**

* Exception handling in Spring Boot RESTful services can be managed using @ControllerAdvice and @ExceptionHandler.  
* @ControllerAdvice allows you to define global exception handlers,  
* while @ExceptionHandler handles exceptions for specific controllers or methods.  
* OR

To handle exceptions in a RESTful web service using Spring Boot, follow these steps:

1. Use @ControllerAdvice: Create a class annotated with @ControllerAdvice to handle exceptions globally across all controllers.  
2. Define Exception Handlers: Implement methods annotated with @ExceptionHandler to handle specific exceptions and return appropriate responses.  
3. Return Custom Responses: Use ResponseEntity to return custom error messages and appropriate HTTP status codes.

### **What is ResponseEntity and when would you use it?**

* ResponseEntity is a class in Spring used to represent the entire HTTP response, including the status code, headers, and response body.

### **What are HTTP status codes, and how do you return them in Spring Boot?**

HTTP status codes are standardized codes that indicate the result of an HTTP request. Common status codes include. In Spring Boot, we can return status codes using ResponseEntity or by annotating controller methods with @ResponseStatus.

* **200 OK:** The request was successful.  
* **201 Created:**  The resource was successfully created.  
* **204 No content** : The documents contains no data  
* **400 Bad Request:** The request was invalid or cannot be processed.  
* **404 Not Found:** The requested resource does not exist.  
* **401 Unauthorized:** Authentication is required and has failed or has not yet been provided.  
* 408  Request timeout  
* **403 Forbidden:** The client does not have access rights to the content.  
* **500 Internal Server Error:** An error occurred on the server.  
* **502** Bad Gateway  
* **503 Service Unavailable**

### **What is REST and what are its principles?**

* REST (Representational State Transfer) is an architectural style for building web services. It is based on stateless communication, where each request from a client contains all the necessary information.  
* Rest is a protocol to communicate 2 applications with each other in a stateless manner. REST principles include:  
* **Statelessness**: In Restful API, requests are not stored on the server side.  
* **Client-Server Architecture:** The client and server are separated, allowing them to evolve independently.  
* Uniform Interface: Resources are identified by URIs, and standard HTTP methods (GET, POST, PUT, DELETE) are used for operations.  
* Cacheability:Responses can be cached to improve performance.  
* Layered System: The architecture is composed of layers like proxies and gateways, where each layer has a specific responsibility.

### **What is the role of @EnableAutoConfiguration in Spring Boot?**

* Answer: @EnableAutoConfiguration is an annotation that tells Spring Boot to automatically configure your application based on the dependencies present on the classpath.

### **What is the purpose of the @SpringBootApplication annotation?**

* It is a class level annotation.  
* The @SpringBootApplication annotation is a convenience annotation that is the combination of three annotations: @Configuration, @EnableAutoConfiguration, and @ComponentScan.   
* It marks the main class of a Spring Boot application and triggers auto-configuration, component scanning, and allows for custom configurations.

### **What is @SpringBootApplication in Spring Boot?**

* @SpringBootApplication is a single annotation in Spring Boot that combines three essential annotations:  
* @SpringBootConfiguration: Marks the class as a source of Spring configuration.  
* @EnableAutoConfiguration: Automatically configures Spring components based on the classpath.  
* @ComponentScan: @ComponentScan is an annotation in Spring used to scan  the package for Spring components such as @Component, @Service, @Repository, and @Controller. 

### **Spring Boot stereotype annotations** 

* (@Component, @Service, @Repository, @Controller, and @RestController) are used to automatically register classes as Spring beans in the application context. 

###  **Configure Spring Security**

1. Create a Security Configuration Class: Create a class that extends WebSecurityConfigurerAdapter. This class will define your security configuration.

What is API?

* An API, or Application Programming Interface, is a contract that defines how different software programs can communicate with each other.  
*  It provides a set of methods and protocols that enable one application to access the functionalities or data of another, without need to know the internal workings of that system.

### **What is a REST template?**

* RestTemplate in Java is a class provided by Spring Framework to simplify making HTTP requests to RESTful services.   
* It allows you to send HTTP requests (GET, POST, PUT, DELETE, etc.) and handle the responses in a straightforward way.  
* It's often used to communicate between microservices.  
* RestTemplate is deprecated and  considered a legacy approach ,and for new projects spring recommends using WebClient, which supports both synchronous and asynchronous operations.  
* Key feature of RestTemplate :   
1. HTTP Methods:  
* RestTemplate supports the standard HTTP methods such as GET, POST, PUT, DELETE, HEAD, OPTIONS, and PATCH.  
2. Simplified API Consumption:  
* It simplifies API consumption and it is widely used in microservice  architecture to communicate between different services.   
* **Automatic Serialization and Deserialization:** RestTemplate automatically converts Java objects to JSON and vice versa.  
* **Handling Responses:** Responses can be handled as ResponseEntity, which includes the HTTP status code, headers, and body.  
* **Error Handling:** RestTemplate provides default error handling through RestTemplateResponseErrorHandler.

### **Differences between RestTemplate and WebClient?**

* RestTemplate is synchronous and blocking, while WebClient supports both synchronous and asynchronous calls with a non-blocking I/O model.   
* WebClient is recommended for new applications due to its flexibility and modern design.

### **What is REST API?**

* **Representational State Transfer Application Programming Interface** is a protocol to communicate two applications with each other and allows them to exchange data in a stateless manner.

### **What is Application Context?**

* The ApplicationContext in Spring is the central interface for providing configuration information to the application.  
* It's an advanced version of the BeanFactory and is responsible for managing the complete lifecycle of beans in a Spring application.  
* Some common implementation includes :   
* AnnotationConfigApplicationContext: For Java-based configuration.  
* ClassPathXmlApplicationContext: For XML-based configuration.  
* The ApplicationContext acts as an IoC container, which is responsible for creating, instantiating, and deleting objects.

### **Life cycle of beans?**

* The lifecycle of beans in Spring refers to the series of stages a bean goes through from its creation to its destruction.

1\. **Instantiation:**

* Spring creates an instance of the bean using the constructor or a static factory method.

2\. **Dependency Injection:**

* After instantiation, Spring injects the required dependencies (e.g., other beans, properties) into the bean via setter methods or constructor injection.

3\. **Initialization** : 

* BeanNameAware: The bean is made aware of its name in the Spring context.  
* BeanFactoryAware: The bean is made aware of the Spring BeanFactory that created it.  
* ApplicationContextAware: The bean is made aware of the Spring ApplicationContext it belongs to.  
* InitializingBean interface: The afterPropertiesSet() method is called.

4\. **Usage:** The bean is ready for use in the application.  
5\. **Destruction**  : @PreDestroy or destroy() is invoked before destroy or remove bean.

