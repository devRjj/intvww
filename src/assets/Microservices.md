# Microservices

---

**Microservices**, also called **Microservices Architecture**, is a software development approach that involves building large applications as a collection of small functional modules. This architectural approach is widely adopted due to its ease of maintenance and faster development process.

**Microservices with the Spring Boot** framework break down complex applications into **smaller services**, **loosely coupled services**, each focusing on a specific business capability. This architecture promotes **agility**, **scalability**, and **resilience**, leveraging technologies like Docker, Kubernetes, and **RESTful APIs** for seamless communication and deployment in distributed environments.

# What are Microservices?

Microservices is an architecture in which the application performs as a loosely coupled service that can be developed, deployed, and maintained independently. Each service in this architecture is called a Microservice.

* In Microservices, each service performs a different and unique function.  
* Through APIs it communicates with other services by focusing on the business strategies.  
* Different microservices can be used for different architecture and languages.

# When and Why to use Microservices?

For large or complex projects microservices are the best choice for scalability, flexibility, and faster development with evolving requirements. Microservices are useful when the application or our project needs to be more scalable and manageable or requires more resources.

* Microservices are ideal when the monolithic applications need to be optimized and modernized.  
* Each service can be independently developed, deployed, and maintained.  
* To reduce time, for scalability, fast development, low cost, and cloud-native development microservices are ideal.  
* We should not use microservices for simple applications which can be managed by monolithic architecture.

### **3\. Explain the workings of Java Microservices Architecture.**

In Java Microservices architecture, an application is divided into small processes or we can call them sub-processes. Each process runs on its functionality. All the sub-processes communicate with each other through small protocols. It manages better scalability and coordination between services.

Below is the Architectural diagram of Java Microservices:

![Java Microservices Architecture][image1]

### **4\. What are the Pros and Cons of Java Microservices?**

There are so many benefits and drawbacks in Java Microservices architecture.

**Pros:**

* We can use different technologies using microservices.  
* It takes care of the security of each service.  
* More than one service can be parallelly developed and deployed.  
* Services are independently managed.  
* Better scalability and agility.

**Cons:**

* Communication between microservices can be complex.  
* Large numbers of service management is difficult.  
* Handling microservices with different business requirements is a tough task.  
* So many configurations have to be done which increases efforts.  
* Network maintenance is difficult.  
* Complex development and Security issues.

### **5\. What are the main features of Java Microservices?**

There are so many features of Java Microservices. Some of the main features are listed below:

![Java Microservices Features][image2]

* **Deployment**: It breaks an application into small services, because of this it is possible to deploy and develop each of these services independently.  
* **Decentralization**: Data storage management is decentralized. Each of the services has its own data related to a particular business functionality.  
* **Loosely Coupled**: If a single process fails, it will not affect the other services and the entire system.  
* **Security**: It provides authentication and authorization based on the Role-based access model (RBAC).  
* **Scalable**: Based on the requirements, services can be scaled which results in better scalability.

### **6\. What is Monolithic architecture?**

A monolithic architecture-based application is built as a single unit, meaning inside a single code base, all the functionality and modules of the application are available.

* Before microservices, all modules were there in a single project.  
* It supports tightly coupled architecture.

![Monolithic Architecture][image3]

* Here, we have a server. The server can be Tomcat, jetty, or any type.  
* On this server, we have deployed our application.  
* Inside this web application, we need to deploy all the modules of an application.  
* The outcome will be a **WAR** file. Only if we deploy the war file, these modules will be available.

This is the **Monolithic Architecture**.

### **7\. Explain SOA.**

**SOA** refers to **Service-Oriented Architecture.**

* This SOA architecture is a collection of multiple services.  
* These multiple services do communicate with each other by using some standardized protocols.  
* Also in this design approach, applications are built as a collection of services that are loosely coupled.

![SOA Architecture][image4]

It communicates with each service over a network and then implements a specific business function. The communication could be the normal passing of data or more than two services sharing some common activity or any type of coordination.

### **8\. What is the difference between Monolithic, SOA, and Microservices Architecture?**

Below are the basic differences between the Monolithic, SOA, and Microservices Architecture.

| Features | Monolithic | SOA | Microservices |
| :---: | ----- | ----- | ----- |
| **Structure** | A single application where all software components are assembled and tightly coupled. | Collection of services and loosely coupled. | Collection of small services and services independently deployable. |
| **Communication** | Within the same application, components communicate with each other. | Using some standardized protocols, services communicate with each other. | Through some lightweight protocols, all the services communicate with each other. |
| **Scalability** | Scaling is required according to the needs of the entire application. | All services can be scaled independently. | All the services can be scaled independently according to the business requirement. |
| **Development and Deployment** | It maintains centralized development and components deployed as a single unit. | It also maintains centralized development and here the services are deployed as monolithic applications. | It maintains decentralized development and services deployed independently. |

### **9\. Explain the design patterns of Java Spring Boot Microservices.**

Spring Boot is a popular framework for building microservices in Java. Here are some key design patterns commonly used with Spring Boot for microservices architecture:

**1\. API Gateway**

* **What it is:** Acts as a single entry point for all client requests, routing them to the appropriate microservice. It can also handle cross-cutting concerns like authentication, authorization, and rate limiting.  
* **Why use it with Spring Boot?** Spring Cloud Gateway provides a powerful way to implement API gateways with Spring Boot.

**2\. Service Registry and Discovery**

* **What it is:** Microservices register themselves with a service registry (like Eureka or Consul), and clients can discover the location of services through the registry.  
* **Why use it with Spring Boot?** Spring Cloud Netflix Eureka and Spring Cloud Consul provide integrations for service registration and discovery.

**3\. Circuit Breaker**

* **What it is:** Prevents cascading failures by stopping requests to a failing service for a certain period. It monitors the service and, if it recovers, allows requests to flow again.  
* **Why use it with Spring Boot?** Spring Cloud Circuit Breaker (using Resilience 4j or Hystrix) helps implement this pattern.

**4\. Saga Pattern**

* **What it is:** Manages distributed transactions across multiple microservices. It's a sequence of local transactions, where each transaction updates data within a single service.  
* **Why use it with Spring Boot?** Spring Boot can be used to implement Sagas, often with messaging systems like Kafka to coordinate transactions.

**5\. Asynchronous Messaging**

* **What it is:** Microservices communicate with each other using asynchronous messages (e.g., with Kafka or RabbitMQ), which decouples them and improves resilience.  
* **Why use it with Spring Boot?** Spring for Apache Kafka and Spring AMQP provide excellent support for messaging.

**6\. Database per Service**

* **What it is:** Each microservice has its own database, ensuring loose coupling and data autonomy.  
* **Why use it with Spring Boot?** Spring Data JPA and Spring Data MongoDB can be used to connect to different databases for each service.

**7\. Bulkhead Pattern**

* **What it is:** Isolates different parts of the application into "bulkheads" to prevent failures in one part from affecting others.  
* **Why use it with Spring Boot?** Thread pools and circuit breakers in Spring Boot can help implement bulkheads.

**8\. CQRS (Command Query Responsibility Segregation)**

* **What it is:** Separates read and write operations into different models, allowing for optimization of each.  
* **Why use it with Spring Boot?** Spring Boot can be used to build separate services for commands and queries.

**9\. Sidecar Pattern**

* **What it is:** Deploys a helper process ("sidecar") alongside a microservice to provide additional functionalities like logging, monitoring, or security.  
* **Why use it with Spring Boot?** Spring Boot applications can be easily containerized and deployed with sidecars in environments like Kubernetes.

These patterns help you build resilient, scalable, and maintainable microservices with Spring Boot.

* 

### **10\. What are the Main Components of Java Spring Boot Microservices?**

The main components of Java Spring Boot Microservices include:

* Services  
* Service Registry  
* API Gateway  
* Cloud Infrastructure  
* Containerization and Orchestration  
* Message Broker  
* Security  
* Monitoring

### **11\. Name three commonly used tools for Java Spring Boot Microservices.**

There are different tools used for Java Spring Boot Microservices, some important tools are,

1. **Docker:** This is a containerization tool that allows developers to put applications and their dependencies in a lightweight container, and provide stability across multiple environments.  
2. **Kubernetes:** This is an open-source container orchestration tool and it automates the scaling, deployment, and management of containerized applications. It offers features like service discovery, load balancing etc.  
3. **Spring Cloud**: This is a framework in the Spring ecosystem for building microservice-based applications. It is used to develop cloud-native applications. It offers features like service discovery, configuration management, circuit breakers etc.

### **12\. How do Microservices Communicate with each other?**

In Microservices, multiple services run independently. Services communicate with each other through,

* **HTTP/REST:** These are light-weight protocols used to perform communication between two services.  
* **Message queues:** Message queues such as Kafka or RabbitMQ used to make connections.  
* **RPC (Remote Procedure Call) Framework:** RPC frameworks such as gRPC are used in services for communication purposes.

These methods of communication enable loosely coupled interaction, scalability, and flexibility in distributed systems.

For more details please refer to this article: [How do Microservices Communicate With Each Other?](https://www.geeksforgeeks.org/how-do-microservices-communicate-with-each-other/)

### **13\. How to Process the Request and Response between Two Services?**

By establishing communication between the two services, microservices can handle requests and responses between any two services using XML (Extensible Mark-up Language) and JSON (JavaScript Object Notation).

* XML and JSON are data exchange formats and it helps to generate requests and responses between two services.  
* Most important thing is the data exchange format and both the services have to know the data exchange format to request and respond accordingly.  
* If we compare both formats, JSON is very simple to use in Microservices.

### **14\. What is WebClient and How Java Microservices Communicate using WebClient?**

An interface called WebClient represents the primary access point for web requests. It is also known as Reactive Web Client that was introduced in Spring 5\. The new client is a non-blocking, reactive solution that works over HTTP/1.1 protocol. Also, it is the replacement of classic RestTemplate. We can use the WebClient for Java Microservices Communication by the following approach.

Add this dependency to the pom.xml file:

\<dependency\>  
   \<groupId\>org.springframework.boot\</groupId\>  
   \<artifactId\>spring-boot-starter-webflux\</artifactId\>  
\</dependency\>

After adding this library, create a Bean for the WebClient in the configuration file like below:

@Bean  
public WebClient webClient() {  
 return WebClient.builder().baseUrl(addressBaseUrl).build();  
}

After creating Bean, it is ready for use in the Service Class file. We can refer the below code:

@Service  
public class EmployeeService {

   // More Code Here

   // \-------------

   @Autowired  
    private WebClient webClient;

   public EmployeeResponse getEmployeeById(int id) {  
     
     
    // More Code Here  
     
    // \--------------

       // Using WebClient  
        AddressResponse addressResponse \= webClient.get().uri("/address/" \+ id).retrieve().bodyToMono(AddressResponse.class).block();  
        employeeResponse.setAddressResponse(addressResponse);

       return employeeResponse;  
    }

}

For more details please refer to this article: [Spring Boot Microservices Communication using WebClient with Example](https://www.geeksforgeeks.org/spring-boot-microservices-communication-using-webclient-with-example/)

### **15\. What is RestTemplate and How Java Microservices Communicate using RestTemplate?**

The RestTemplate is a synchronous REST client that performs HTTP requests by using a simple API of template style.

* This is a synchronous client and it is designed to call the REST services.  
* RestTemplate class plays a very major in Spring Boot Microservices Communication.

We can use RestTemplate for Java Microservices Communication by the following approach:

Microservices can communicate using RestTemplate.getForObject() method. Syntax of RestTemplate.getForObject() method is given below.

@Nullable  
public \<T\> T getForObject(String url, Class\<T\> responseType, Object... uriVariables) throws RestClientException {  
       RequestCallback requestCallback \= this.acceptHeaderRequestCallback(responseType);  
       HttpMessageConverterExtractor\<T\> responseExtractor \= new HttpMessageConverterExtractor(responseType, this.getMessageConverters(), this.logger);  
       return this.execute(url, HttpMethod.GET, requestCallback, responseExtractor, (Object\[\])uriVariables);  
}

For more details please refer to this article: [Spring Boot Microservices Communication using RestTemplate with Example](https://www.geeksforgeeks.org/spring-boot-microservices-communication-using-resttemplate-with-example/)

### **16\. What is FeignClient and How Java Microservices Communicate using FeignClient?**

FeignClient is known as Spring Cloud OpenFeign.

* It is a declarative REST Client in Spring Boot Web Application. Declarative REST Client means to specify the client specification as an Interface and spring boot will take care of the implementation.  
* With the help of FeignClient, writing web services is very simple.  
* It is mostly used to consume REST API endpoints exposed by third parties or microservices.

We can use FeignClient for Java Microservices Communication by the following approach:

Add this dependency to the pom.xml file.

\<dependency\>  
   \<groupId\>org.springframework.cloud\</groupId\>  
   \<artifactId\>spring-cloud-starter-openfeign\</artifactId\>  
\</dependency\>

After adding the library, add this @EnableFeignClients annotation to the main Application file as below:  
@SpringBootApplication  
@EnableFeignClients  
public class Application {

   public static void main(String\[\] args) {  
        SpringApplication.run(Application.class, args);  
    }

}

Create an Interface and define it with @FeignClient annotation and declare calling method as below:

@FeignClient(name \= "giveHereServiceName", url \= "provideUrlHere", path \= "provideContextPathHere")  
public interface AddressClient {

   @GetMapping("/address/{id}")  
    public ResponseEntity\<AddressResponse\> getAddressByEmployeeId(@PathVariable("id") int id);

}

Now it is ready to be used in the service class file. You can see the below code:

@Service  
public class EmployeeService {

   // More Code Here

   // \-------------

   // Spring will create the implementation  
    // for this class  
    // and here it will insert the bean (proxy) .  
    @Autowired  
    private AddressClient addressClient;

   public EmployeeResponse getEmployeeById(int id) {  
     
        // More Code Here

       // Using FeignClient  
        ResponseEntity\<AddressResponse\> addressResponse \= addressClient.getAddressByEmployeeId(id);  
        employeeResponse.setAddressResponse(addressResponse.getBody());

       return employeeResponse;  
    }

}

For more details please refer to this article: [Spring Boot Microservices Communication using FeignClient with Example](https://www.geeksforgeeks.org/spring-boot-microservices-communication-using-feignclient-with-example/)

### **17\. How Client Side Load Balancing Happens in Java Spring Boot Microservices?**

When a load balancer is put on the client side along with assigning load balancing responsibilities to the client, this is called Client-Side Load Balancing. Spring Cloud LoadBalancer is one of the most popular client-side load balancers offered by Spring Cloud.

Spring Cloud LoadBalancer can be used for Client Side Load Balancing in Microservices by the following approach:

Add the following dependencies to pom.xml file.

\<dependency\>  
     \<groupId\>org.springframework.cloud\</groupId\>  
     \<artifactId\>spring-cloud-starter-loadbalancer\</artifactId\>  
\</dependency\>

Client Side Load Balancing can be done with the help of LoadBalancerClient. We need to write the following logic in our client microservice in the Service class.

@Autowired  
private RestTemplate restTemplate;

@Autowired  
private LoadBalancerClient loadBalancerClient;

// Get ServiceInstance list using serviceId  
ServiceInstance serviceInstance \= loadBalancerClient.choose("ADDRESS-SERVICE");

// Read URI and add the path that returns url  
String uri \= serviceInstance.getUri().toString();

// Get metadata  
String contextPath \= serviceInstance.getMetadata().get("configPath");

// HTTP call and got Response data  
AddressResponse addressResponse \= restTemplate.getForObject(uri \+ contextPath \+ "/address/{id}", AddressResponse.class, id);

For more details please refer to this article: [Java Spring Boot Microservices – Client Side Load Balancing with Spring Cloud LoadBalancer](https://www.geeksforgeeks.org/java-spring-boot-microservices-client-side-load-balancing-with-spring-cloud-loadbalancer/)

### **18\. How Load Balancing Happens in Java Spring Boot Microservices using Netflix’s Ribbon?**

Ribbon is a special load balancer provided by Netflix so that we do not have to create this load balancer or write any code to make this pattern possible. We can only use the Netflix Ribbon for having the client-side load balancing.

We can use Netflix’s Ribbon for Load Balancing in Microservices by the following approach

Add the following dependency in pom.xml file:

\<dependency\>  
   \<groupId\>org.springframework.cloud\</groupId\>  
   \<artifactId\>spring-cloud-starter-netflix-ribbon\</artifactId\>  
\</dependency\>

Annotate your Feign Client interface with @RibbonClient. Refer to the below code snippet.

@FeignClient(name \= "address-service", path \= "/address-service")  
**@RibbonClient(name \= "address-service")**  
public interface AddressClient {

   @GetMapping("/address/{id}")  
    public ResponseEntity\<AddressResponse\> getAddressByEmployeeId(@PathVariable("id") int id);

}

Make the following changes to the application.properties file.

address-service.ribbon.listOfServers=http://localhost:8081, http://localhost:8082

For more details please refer to this article: [Spring Boot Microservices – Load Balancing using Netflix’s Ribbon](https://www.geeksforgeeks.org/spring-boot-microservices-load-balancing-using-netflixs-ribbon/)

### **19\. How Eureka Server and Client Communicate with Each Other in Java Microservices?**

Service discovery is one of the key issues in microservices-based architecture. The Eureka is Netflix service discovery, consists of a discovery server and a client. The server can be configured and deployed to maximize performance, with each server copying the status of registered services to the others.

Suppose, our discovery service is running on the port number 5000,

server.port=5000

Now if we run our microservice then we may get the **"Connection refused"** error. To fix this, we have to add the following line in the application.properties file of microservice.

eureka.client.service-url.defaultZone=http://localhost:5000/eureka/

This will fix our issue.

For more details please refer to this article: [How Eureka Server and Client Communicate with Each Other in Microservices?](https://www.geeksforgeeks.org/how-eureka-server-and-client-communicate-with-each-other-in-microservices/)

### **20\. How to Develop API Gateway in Java Spring Boot Microservices?**

We can develop API Gateway in Java Spring Boot Microservices by using Spring Cloud Gateway. Spring Cloud Gateway provides a library for creating API gateways over Spring and Java. It provides a flexible way to submit standards-based requests, while focusing on contextual issues such as security, resiliency, and monitoring Spring Cloud Gateway features some of the most important ones are:

* It is Built on Spring Framework 5, Project Reactor, and Spring Boot 2.0  
* We can integrate the Circuit Breaker with the Spring Cloud Gateway.  
* We can integrate Spring Cloud DiscoveryClient.  
* Predicates and filters are specific to routes.  
* Path Rewriting.  
* It can match routes on any request attribute.

For more details please refer to this article: [Java Spring Boot Microservices – Develop API Gateway Using Spring Cloud Gateway](https://www.geeksforgeeks.org/java-spring-boot-microservices-develop-api-gateway-using-spring-cloud-gateway/)

## **Java Microservices Interview Questions for Experienced**

### **21\. How to Register Java Microservices Using Netflix Eureka?**

The Eureka is the Netflix service discovery, consisting of a discovery server and a client. The server can be configured and deployed to maximize performance, with each server copying the status of registered services to others. To Register and Discover Microservices Using Netflix Eureka we have to develop one Service Discovery and one Microservice.

* Developing Microservice or Eureka Client  
* Developing Service Discovery or Eureka Server

For more details please refer to this article: [How to Register Microservices Using Netflix Eureka?](https://www.geeksforgeeks.org/spring-cloud-how-to-register-microservices-using-netflix-eureka/)

### **22\. What is Client Side Service Discovery in Java Microservices and Provide Some Examples of It?**

In microservices, Service discovery refers to the process of dynamically locating and connecting to available services within a distributed system.

* In a microservice system, applications perform multiple tasks and that are composed of many independently deployable services.  
* Service discovery is critical to facilitate communication between these different services.  
* If we put Service Discovery in **client side** then we called it as Client Side Service Discovery.

**Example:**

* Netflix Eureka  
* Zookeeper  
* Consul

For more details please refer to this article: [Client Side Service Discovery in Microservices](https://www.geeksforgeeks.org/client-side-service-discovery-in-microservices/)

### **23\. What is Server Side Service Discovery in Java Microservices and Provide Some Examples of It?**

In microservices, Service discovery refers to the process of dynamically locating and connecting to available services within a distributed system.

* In a microservice system, applications perform multiple tasks and that are composed of many independently deployable services.  
* Service discovery is critical to facilitate communication between these different services.  
* If we put Service Discovery in **server side** then we called it as Server Side Service Discovery.

**Example:**

* NGNIX  
* AWS ELB

For more details please refer to this article: [Server Side Service Discovery in Microservices](https://www.geeksforgeeks.org/server-side-service-discovery-in-microservices/)

### **24\. Why Use Spring Cloud for Microservices Development?**

Spring Cloud is a project under which we have many sub-projects. We can solve all these problems with those sub-projects.

* Spring Cloud Config Server  
* Service registration and discovery using Eureka  
* Spring Cloud LoadBalancer  
* resilience4j-ratelimiter  
* Circuit Breakers Pattern

For more details please refer to this article: [Why Use Spring Cloud for Microservices Development?](https://www.geeksforgeeks.org/why-use-spring-cloud-for-microservices-development/)

### **25\. Explain 5 Major Challenges and Solutions of Java Spring Boot Microservices Architecture.**

There are 5 challenges mentioned below with solutions that we might face while developing microservices applications.

* **Challenge 1:** Service Configuration Management  
  * **Solution:** Spring Cloud Config Server centralizes configuration management for microservices.  
* **Challenge 2:** Service Discovery and Registration  
  * **Solution:** Eureka enables dynamic service discovery and registration.  
* **Challenge 3:** Load Balancing Across Microservices  
  * **Solution:** Spring Cloud LoadBalancer distributes traffic evenly among microservice instances.  
* **Challenge 4:** Resilience and Fault Tolerance  
  * **Solution:** resilience4j-ratelimiter implements rate limiting to maintain stability under heavy load.  
* **Challenge 5:** Handling Failures and Circuit Breakers  
  * **Solution:** Circuit Breaker pattern with tools like Hystrix provides fault isolation and fallback mechanisms.

For more details please refer to this article: [5 Major Challenges and Solutions of Microservices Architecture](https://www.geeksforgeeks.org/challenges-and-solutions-of-microservices-architecture/)

### **26\. Tell Some Major Reasons to Choose Spring Boot For Microservices Development.**

Here are some major reasons to Choose Spring Boot For Microservices Development.

* Embedded Server  
* Support Load Balancer  
* Auto Configuration  
* Minimal Code using Annotations  
* Loose Coupling  
* Dependency Management  
* Open Source

For more details please refer to this article: [Major Reasons to Choose Spring Boot For Microservices Development](https://www.geeksforgeeks.org/why-to-choose-spring-boot-for-microservices-development/)

### **27\. What is Circuit Breaker Pattern in Java Microservices?**

Circuit Breaker pattern in microservices follows fault-tolerance mechanism. It monitors and controls the interaction between different services. It dynamically manages service availability by temporarily canceling requests for failed services, prevents system overloading, and ensures graceful degradation in distributed environments. Circuit Breaker pattern typically operates in three basic states: Closed, Open, and Half-Open.

Here are some Characteristics of Circuit Breaker pattern:

* **Fault Tolerance**  
* **Resilience**  
* **Monitoring**  
* **Failure Isolation**  
* **Fallback Mechanism**  
* **Automatic Recovery**

### **28\. Explain Different Deployment Techniques to Deploy Java Microservices.**

There are different ways to deploy Microservices. Some of them are mentioned below:

* **Single Machine, Multiple Services:** Buy a server and run microservices as services.  
* **Multiple Machines, Multiple Services:** When application exceeds the capacity of the server, we can upgrade the server by scaling up (Add more Servers).  
* **Containerization:** Each microservices runs independently by enabling flexibility and scaling as per demand.  
* **Orchestrators:** It distributes the workload of a container over a group of servers. (Ex: Kubernetes)  
* **Serverless Deployment:** Processes or containers use cloud to run code on demand.

### **29\. What is the Main role of Docker in Microservices and How to deploy microservices in Docker?**

The main role of Docker in microservices is to provide containerization, which allows each microservice with its dependencies to coordinate with the runtime environment, ensuring stability in unique environments.

Steps to deploy microservices in Docker:

* **Step 1:** Containerize each microservice by creating a Dockerfile specifying the application's dependencies and runtime configuration.  
* **Step 2**: Build Docker images for each microservice using the `docker build` command.  
* **Step 3:** Push the built Docker images to a Docker registry such as Docker Hub or a private registry.  
* **Step 4:** Create Docker Compose or Kubernetes manifests defining the configuration for deploying and orchestrating the microservices.  
* **Step 5:** Deploy the Dockerized microservices using Docker Compose or Kubernetes by running `docker-compose up` or applying the Kubernetes manifests respectively.  
* **Step 6:** Monitor and manage the deployed microservices using Docker CLI commands or Kubernetes dashboard.

### **30\. How to Deploy Java Spring Boot Microservices in AWS?**

To deploy our microservices application in AWS (Amazon Web Services), we need to follow the below steps.

* **Step 1:** In the first step, open the AWS Management Console and then go to [EC2.](https://www.geeksforgeeks.org/amazon-ec2-creating-an-elastic-cloud-compute-instance/)  
* **Step 2:** After that, **click on the [Load Balancers](https://www.geeksforgeeks.org/elastic-load-balancer-in-aws/)** and create a new Application Load Balancer. Also, create a new target group associated with that load balancer. Then define the target group targets (ECS instances) and health checks.  
* **Step 3:** Now, in the AWS Management Console, go to ECS and create a new ECS cluster.  
* **Step 4:** Then choose the networking options and click on next.  
  * Configure the cluster and give the name to the cluster.  
  * Then create an ECS Task and click on the repository.  
  * Now, configure the repository and make sure it is private.  
  * Lastly, create the Task Definitions.  
* **Step 5:** Now update the ECS Task.

For more details please refer to this article: [Deploy a Microservices Architecture with AWS](https://www.geeksforgeeks.org/deploy-a-microservices-architecture-with-aws/)

## **Conclusion**

**Microservices** are also highly beneficial for modern software development methods like [DevOps](https://www.geeksforgeeks.org/courses/devops-live) and [Agile](https://www.geeksforgeeks.org/software-engineering-agile-software-development/). Adopting this approach helps in delivering large, complex applications promptly, frequently, and reliably.

Many companies such as Netflix, Amazon, Ebay, Uber, and Spotify adopt microservices in order to manage complex systems in large-scale operations. With a booming demand for Microservices Developers, now is the perfect time to gear up for interviews and capitalize on this dynamic market.

## **Microservices Interview Questions \- FAQs**

### **What is the typical salary range for a microservices developer in USA?**

In the USA, microservices developers typically earn between $90,000 to $150,000 annually, depending on experience, location, and the specific sector they work in.

### **What is the salary of microservices developer in India?**

In India, the salary range for microservices developers is generally between INR 8 lakhs to INR 30 lakhs per year, with variations based on similar factors.

### **What does Microservices Developer do?**

A Microservices Developer specializes in designing, building, and maintaining small, independent, and loosely coupled services. They work on developing applications where each microservice runs a unique process and communicates through a well-defined, lightweight mechanism to serve a business goal. Developers handle the full lifecycle of these services, from design through development, testing, deployment, and support.

### **What are the essential skills required for a Microservices developer?**

Essential skills for a Microservices developer include:

* Proficiency in programming languages  
* Understanding of containerization technologies  
* Familiarity with CI/CD tools  
* Experience with RESTful services and APIs  
* Knowledge of database management  
* Understanding of cloud platforms  
* Strong debugging and troubleshooting skills

### **How can I stand out in a Microservices interview?**

Showcase specific projects where you successfully implemented microservices, discuss the unique challenges you overcame, and highlight your familiarity with modern tools like Docker, Kubernetes, and cloud platforms.

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,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VO5yjIsva9j8POObO2v4XB5zdbt6T+7y35G0Xn8b37iqupzbRb71nW/F5tb2zGuFKJdc2N5gEj1ZE+aW+wFnjZYNeHsi2KC3JtEaMJUzb/bkcOva8kxyJ1Ih7XYm07bR9k+xlenE8M3hnnvuGbVnr732yunCmgZGz+8vs9dUB31m9Z0n/ydI3jnJGj1b7svE0nY5w+EbpjhZA+Xk9p3po+9cTKIqaTbRtdE3o3GyH2H7ynR8vrH1jzGTSczUlrjvEcbJjputM9f2x9WVozT2bDz60vjVOIbWHHroodEfvPvuu6+cffbZsmTJErvKdto7FxYil9s0P9iyuPyisrktrszmwSST6LbT3zOZRN2uW49usfu37e5oZcqFOwpMoqckk+gbOxtwTs5QuYC1dbqA9uty6/p/balc8Prb6r/1p982e/L4gW6PJdd2u3a49W3d/uxjeynpxLjssstk9913324OVTvvvLN89rOflZtvvrnDdcstt8T+zCa7fqbtfjXwp7Jo3YKgz3zp69H25lV8qIOksZfpFX0avyd1/U+58cYbpXfv3tKrVy/p2bOn/PrXv5YePXpI9+7d5aqrrpJf/vKX0q1bt+i8v+SSS+TCCy+Url27yvnnny/nnXeenHvuuZGZOvPMM+X000+XU089VU455RQ5+eST5aSTTpITTjhBfvCDH8h3v/td+fa3vy3HHXecHHvssXLMMcfI0UcfLUcddZR07txZvvrVr8qRRx4pRxxxhHz5y1+WL37xi/KFL3xBPve5z8khhxwiBx10kHzyk5+UAw44QD7xiU/Ixz/+cfnoRz8q++yzT3Qt0muSzgJ+5CMfkZ122im6Ju2yyy6R4dt7770j0/exj31M9ttvP9l///3lwAMPlE996lNy8MEHR/WrOfz85z8vhx12WFSPf33Wel588UV7KWz3XFio7GSEy21JExq67tTap2PzrpPNczanxuVRu42dnEnKrXbfHa2kXLgjwSR6ssbKLc/0V4kvLbdmywa0H6y2zO3PD27dt9Z37+hB0U/fpNkToRCTmNTuUjSJij+TqDOI2qZKmknsX32NLGleHPSZr5tqR8oeI84IkjdCO0IaexqDNi6dNH41jtPK+++/L++++678/e9/lz//+c/y9ttvy1tvvSVvvPGG/PGPf5TNmzfLhg0bZP369fLqq69KU1OTvPzyyzJmzJjIULrrsppMNc26vaW9c2Fb5fKFm4RIMolaPmHqhNi862TznDWF9ve4baxJdOsk5dZSUaZcuKPAJHqyfwX5sn+B2HIbsLY8KVjdyeTLD1Z/f/YksidCJpOYa7uzmUSVO/Ft/xVL+ZwYzjTqDEAl0HdKN1mxsTHoM6tdq7oEyRuhHSGNPRuPvjR+NY7hXwwcOHD7R8233XabvPfee3aVVrR3LixEcRMRNr/Ycpfr4vKgzZlWtu5cTKIqLifa3FoqyicXtheYxCLLmq1iyAZ82lUKJ0apkss5MG7l0/m/aQWhIurWhQ8Ecck5XjxyuQ6g7Cr13FoK5wkmscgqtkm0M4K2PI0qhROjVMnlHLhyzj2y07BTg8SN0I6Qxp7GoI1LzvHikct1AGVWOeTWUjhPMImo5FQKJ0ap0m/albJsw9Kgz3yNfmGy7DnyzCB5I7QjpLGns9k2Lp00fjWOoXDIhZWhUsiFmERUciqFE6NUuefZXlnvblZ9bvzFQfIuqvTRKP53hOzjZ+yjZ/xHwrhH2xTweJXUKJ9HDZWZNPZsPPrS+NU4hsIhF1aGSiEXYhJRyakUToxS5f7Zt8r8l58L+szXjFfmySEPXhgk76LKmkT7PEH7jEP73ECUWn2mJfaeeXluEJdOGr8ax1A45MLKUCnkQkwiKjmVwolRquTyxpXpa+fJXiP0tXxhAi+anEk84bB/PazZvrVDjeHZR4Ym0c4k2reCxJnPuAc/xz1Q28p/G4p9sHTcOn77rdx6SfvTunt8K3Odup3fB/5MYi79kK1tmY5TlfT2mCJKY09j0MalE29caTvkwspQKeTCsjKJ/at7SEPzwqAjUXqk46vjDPHk+u7mG2tHBsm7qHImUc2LMy5qTNRAOYOiHznHvXLPN4lx7zlW6b/9bXxj5s9aZnrjiv+WE92Pv68ks2S3sctdm+La4mQNYNwx5rKO26/fD7m0za/LrrsDpLFn49EX725uO+TC9KtUcmFZmcSJi4fI0yseCToTpUc6vjrOEM+y5loZU3tX0G9WQxsfC5J3UeWbRGdKVFf8x7/+rcsLNYlWSWYw0/ZxZfZjcGvy7HcprbS+pLbY/ebSB9lMopVtj22bM4T2OFX2WNtJGns2Hn1p/GocQ+GQC9OvUsmFZWUSlcnLxuaUJFH5ScdVxxeSeftvb8qA6dcGfWfVbfZd7fsYHN8k6u/WlLjlmQySNUdx5s8ZpiRjlrRclTQr6Mu1xbUvl20y7dPJHff/PaC1YbT7jTOJmfohW9sySffpj0M7SGNOY8/Goy+NX41jaBvkwvSqlHJh2ZlEx5rNyyOXrdOx+rk9Kl/pGJbCX0zlgn7pv2Zt5ptXZjXNl689ckWQxIsmaxJ94+SbmGwmUX/3DZJV3PcOrTHzy6z8/Wb6rp4/y5ZpNlHNWqa2+P3j78uuZ01irv2QrW1x+/bVzrOJ//7IL+W5puS77zVuuWmluJAL0yGXB3U8S4myNYkAlcqkhiqZ9sKkIAFbXTX33iCJF03WJPrGxDc+uZhEVZzR8w1NLsbMzmb67fBljVZcfdaw+cY3l7aoMs1KxplEW3dcP2Rrmy97nCq7TpGlMWfj0JfGrcYvAJQHmESAMmP1pkYZPq9fkICt7mgY15K4Tw0SOULtpd8uHhvEoS+NW41fACgPMIkAZcaf/r5V7qzuHiRgq36LH5R9Rp0dJHKE2kMaaxpzNg59adxq/AJAeYBJBChDHq0fmtNHzl1n3C6dqsKEjlCxdfHM/kH8+dJ41bgFgPIBkwhQhmx4q0kGzewdJOI4HT7x0iChI1RMaYzZuLPSeNW4BYDyAZMIUKb0r75G6pvrgmTsq/61JXLgmJ8GSR2hYur/jP6JLF7fEMSfU0NLnGq8AkB5gUkEKFOWrJub03PSfj3vftljxJlBYkeoGNqzJbY0xmzc+dI41XgFgPICkwhQxlTN7Rsk5DgNb3wySO4IFUMaWzberDROAaD8wCQClDFzV08JEnKSPjX2/CDBI9QWfXLMT4M4i5PGKQCUH5hEgDJnzkvPBEk5Tsc90SNI8gi1RRpTNs6sND4BoDzBJAKUObk8M9Gpf8NDQaJHqBBpLNn4ipPGJwCUJ5hEgDJnTO1AqV75RJCck/SZB7sGCR+hfKQxZOMqThqXGp8AUJ5gEgFSgD5epG5dTZCk43T+jH6y6/AuQeJHKBdp7GgM2biy0njksTcA5Q0mESAFzFg5SSbWDwsSdZxmvDJPdq7inc6oMGnsaAzZuLLSeNS4BIDyBZMIkBL0lWdPLRsfJOskXfrcwMAAIJRJGjM2juKkccgr+ADKH0wiQIoYWztQpq54NEjacaprrg9MAEJJ2qXqNKltXhzEkZXGn8YhAJQ/mESAFLF6U6MMnnVjkLiTtPdI3sSCclP3eYOD+ImTxp/GIQCUP5hEgJSxZvNyGTSzd5C8k/T9p64LDAFCvjRGbNzESeNO4w8A0gEmESCFvPrGGhkw/VpZsbExSORWC5oXy85VpwXGACGV3qhS8+rCIG58aZxpvGncAUB6wCQCpJQnlz4gjzaMCBJ6nK5fUCX7PnB2YBBQZUtjQmPDxouVxpnGGwCkC0wiQIqpWTNNRi/I7Y5UVY+a+wKjgCpTGgs2PuKk8aVxBgDpA5MIkHJeen2F3DX9Omnc+HyQ4ON0wYzbZc8RZwSmAVWGdOx/PP23QVxYaTxpXGl8AUA6wSQCVABTGsfJhEW5zQypDh1/UWAeUGVIx97GQ5w0njSuACC9YBIBKoRVG5fK3TN6yrLXlgYJP0lnVfcJTARKp3Ss7fjHSeNH40jjCQDSDSYRoMKomtNXJjdOCJJ/ks6YdqvsM/KswFSgdEjHVsfYjnucNG40fgCgMsAkAlQYG7Y2SZ/Jl0rN2ucCE5Ck4x7vIXtjFFOnfUadHY2tHe84abxo3Gj8AEBlgEkEqFCmLn8oMALZNLzxiei5edZsoPKSjqGOpR3fTJra+JANIQBIOZhEgApmUsPIwAxkUuPG5dL50SsC04HKS0c+fLk0bsj+oHUnjRMAqDwwiQAVTPObL0vfKZfL7NXTAmOQSbXNi2XfUXz8XG66uW5UNHZ2PJOkcaHxoXECAJUHJhEApL5pttwzs5fUN9cFRiGTbqobKfuOPFs6DQ0NCSoRtYyNjtENObw5xUnjIIqHlrgAgMoFkwgAEfrWjPtm3yLPv9YQmIZMumhm/+gGiMCcoBLQKdHY6BjZcUuSjr/GAW9RAQBMIgC0YsbKSTJsbt+8nqfo1HfRaG5sKQHt3CIdCzs+maTjreOu4w8AoGASASCWWauejGaU8v0IWnXlnHvko6PObTEsGMYdqf1G/zjqezsemaTjq+Os4w0A4INJBIBE9CNH/W7agrVzAnORTXPX1cnAJRNk/9HnBWYGFVfax9rXNa8uDMYhk3RcdXz5aBkA4sAkAkBWVm5oiO5ynbZiUmA0ctH9yybJQQ9eIHuPPDMwOKgADf1R1Jfap9q3tr+zScdRx1PHFQAgCUwiAOTMn/6+VcYsGCBj6+4OjEc++sOaWcJH0fnryxN/EfWd7c9cpeOm46fjCACQDUwiAOSNvn0jn9f6xelLE34u+446h8fn5Cjtq2HLHg/6MVfpeOlbdgAAcgWTCAAFoe/wrZrTVx6sG1TQndBWV827F9PopM82bOmLK+a0bcZWx0XHR8eJdy4DQL5gEgGgzazauFTufvZ6mbDoPmnc+HxgVvLVsg2NMr95kfxPzf1ywJifhiYqZdq/5Rj1WPWY9dWHtj/ykfa/joOOh44LAEChYBIBoCi89/67MqVxnNw1/TqpXvlEYF4K0YoWw3TbojFy5MPdZPfhp8snHvhJYLDKVXosekx6bHqMeqz2+POV9rv2v46DjgcAQFvAJAJAu6CPVdE7aB9tGNFigBoDQ9MW/aZ2uHxj0lXy6Qe7ynGPXyO7VnUJTFipSNumbTx0/EVRmxetz++NNpmk/ar9q/3MY2wAoNhgEgGg3dj61y3y5NIHZMD0a2Vy44TA5LRVbvZtxablct2CobJL1Wmyz6iz5GMPnBOYtR2ljz9wbtQGbUuPmiFR2/y2Fkvan9qv2r/azwAAxQaTCAA7jDWbl8vo+f1l8KwbA9PTnpq3bqGMX/n09sfH6Pf/vjLxUjl47AVy0pTecsOCqhZDd5986/Ee283efzx2dbRMy3709I3RurqNfm9Q65jy0uyoTq3b7q+9pP2m/af9CADQ3mASAaBDaNryojxaP1Run3aVTKwfJnXragJTVMnS/tB+0f7RftL+AgDYkWASAaBDeePPm2XGyknSv/oaGVlzR9FueilX6fFrP2h/aL9o/wAAdASYRAAoOdQYzV39tNw/+1a5e0ZPmbB4qMxeUx0YqnKWHo8elx6fHqceL4YQAEoJTCIAlA1b/7JFlqybG82yDZrZWx5aOESmvTBJ6prmBSasFKTt0vZpO7W92m5tvx4HAECpg0kEgLJkw1tNUrf22ej7ejobd2d1dxk+r1/0PT41ZvoaumUb2v4mmFyk+9H96X51/9oObY+2S9un7dT2AgCUE5hEAEg1b//tzeimj2XNtVKzZmr03mm9Q1g/4r3n2V7R7F6/aVdK3yndpM/kS7dLf9flWq7r6fq6XfTe6pZ6tD6tV+sHAEgjmEQAAAAACMAkAgAAAEAAJhEAAAAAAjCJAAAAABCASQQAAACAAEwiAAAAAARgEgEAAAAgAJMIAAAAAAGYRAAAAAAIwCQCAAAAQAAmEQAAAAACtptEhBBCCCGEfP1/3aiuXG2KVncAAAAASUVORK5CYII=>

[image3]: <data:image/png;base64,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>

[image4]: <data:image/png;base64,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YxvXL32RPmn/bL8R4zDO+pBlqA9MinxIJTwIiBFQDY+5QURErDd5zE14EBAjgICIiIgYvwTE8CAgRgABERERMX4JiOFBQIwAAiIiImL8EhDDg4AYAfX+KWZERMRKyKeYw4OAGAEERERExPglIIYHATECCIiIiIjxS0AMDwJiBBAQERER45eAGB4ExAjgQdmIiIjxy4Oyw4OAGAF8ihkRETF++RRzeBAQI4CAiIiIGL8ExPAgIEYAARERETF+CYjhQUCMAAIiIiJi/BIQw4OAGAF8SAURETF++ZBKeBAQI4DH3CAiIsYvj7kJDwJiBBAQERER45eAGB4ExAggICIiIsYvATE8CIgRQEBERESMXwJieBAQI4BPMSMiIsYvn2IODwJiBBAQERER45eAGB4ExAggICIiIsYvATE8CIgRQEBERESMXwJieBAQI4CAiIiIGL8ExPAgIAJAYmndurX75z//aV8GAIACEBABILF06tTJffnll/ZlAAAoAAERABLLxhtv7P72t7/ZlwEAoAAERABILD169HB//OMf7csAAFAAAiIAJJY+ffq41157zb4MAAAFICACQGIZNGiQe+aZZ+zLAABQAAIiACSWIUOGuEWLFtmXAQCgAAREAEgshx56qLv33nvtywAAUAACIgAklpEjR7qbb77ZvgwAAAUgIAJAYhk/fry7/vrr7csAAFAAAiIAJJbJkye7K6+80r4MAAAFICACQGK54IILvAAAUBoERABILJdeeqmbMmWKfRkAAApAQASAxDJ37lw3ceJE+zIAABSAgAgAiUU+wSyfZAYAgNIgIAJAYrnjjjvc8OHD7csAAFAAAiIAJJaHHnrIHXjggfZlAAAoAAERABLLM88847+PGQAASoOACACJ4YwzznDdunVzDz74oPe1115zffr0cX/729+88uDsVq1auccff9wLAADZISACQGKQO4ZrrbWW69Spk1fC4nrrreeaN2/ulXC43Xbb2cUAAMBAQASARPH666/7kCimUqkmbrHFFnZ2AADIAgERABLHBx984G3RooUPhp07d/YCAEBxEBABILFMmDDBtWzZ0s2cOdMLAADFQUAEgIqxatUq99FHH7mlS5d67733Xjd//nx34YUXeuVbUI4aMcLtNXSot0///q57z55u05/+1Lt+ly6ubfv2bq111vG2aNXK/61hs2bNvHL3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>