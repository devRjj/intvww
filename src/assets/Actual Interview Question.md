# Actual Interview Question

# How do you optimize the performance of your application?

* **Use caching**: Implement caching (e.g., Redis, Ehcache) to reduce database load.  
* **Connection pooling**: Configure efficient database connection pooling (e.g., HikariCP).  
* **Profile-specific configs:** Use profiles for environment-specific optimizations (e.g., dev vs. prod).  
* **Asynchronous processing:** Utilize async methods to handle non-blocking requests.  
* **Database indexing:** Ensure proper indexing on frequently queried columns.  
* **Lazy loading:** Use lazy fetching in Hibernate where appropriate.

# How do you optimize the performance of your REST APIs in your Spring Boot application?

* **Limit payloads:** Send only necessary data in responses, avoid large payloads.  
* **Compression:** Enable GZIP compression to reduce response size.  
* **Pagination:** Implement pagination for large datasets.  
* **Caching:** Use @Cacheable and HTTP caching headers (e.g., ETags) for frequent requests.  
* **Pooling and timeout configs:** Configure thread pools and timeouts to handle API load efficiently.  
* **Minimize database calls:** Reduce redundant database calls with batching or aggregation.

# What are the types of Unit testing in SpringBoot?

There are two main types of unit testing in a Spring Boot application:

1\. Standard Unit Tests

* Focus on testing individual components (e.g., services, controllers) in isolation.  
* Mock external dependencies (e.g., repositories, services) using Mockito or other mocking frameworks.  
* Example: Testing a service method by mocking the repository layer.

2\. Spring Context Unit Tests

* Tests components within the Spring context, ensuring Spring-specific configurations (e.g., dependency injection) work properly.  
* Use @SpringBootTest to load the full application context or @WebMvcTest for controller-specific tests.  
* Example: Testing a controller with Spring’s MockMvc.

These types ensure that both individual logic and Spring-specific behavior are tested effectively.

# @SpringBootApplication annotation how internally works describe in detail.

* **@SpringBootApplication** is a combination of three annotations:  
  * **@Configuration:** Marks the class as a source of bean definitions.  
  * **@EnableAutoConfiguration:** Enables automatic configuration of beans based on classpath dependencies.  
  * **@ComponentScan:** Scans for Spring components (e.g., @Controller, @Service) in the package and its sub-packages.

The \`@SpringBootApplication\` annotation is a fundamental component of Spring Boot that simplifies the configuration and setup of a Spring application. It serves as a meta-annotation, encapsulating several other important annotations, and plays a crucial role in bootstrapping the application. Here’s a detailed breakdown of how it works internally.

**What Does \`@SpringBootApplication\` Do?**  
The \`@SpringBootApplication\` annotation is a composite annotation that combines three essential annotations:  
**\`@SpringBootConfiguration\`:**

* This is a specialization of the \`@Configuration\` annotation. It indicates that the class provides Spring configuration. It allows you to define beans and configuration settings directly in the application class.  
* Internally, it enables the registration of additional beans in the application context.

**\`@EnableAutoConfiguration\`**:

* This annotation tells Spring Boot to automatically configure your application based on the dependencies present on the classpath.   
* For example, if you include the Spring Web dependency, it automatically configures a web server (like Tomcat) and sets up Spring MVC.  
* It uses various conditions to determine what to configure, making it flexible and reducing boilerplate code.

**\`@ComponentScan\`:**

* This annotation instructs Spring to scan for components (like \`@Component\`, \`@Service\`, \`@Repository\`, etc.) within the package where the application class resides and its sub-packages.  
* This automatic scanning allows Spring to find and register beans without requiring explicit configuration.

Here’s how you typically use the \`@SpringBootApplication\` annotation:  
\`\`\`java  
import org.springframework.boot.SpringApplication;  
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication  
public class MyApplication {  
	public static void main(String\[\] args) {  
    	SpringApplication.run(MyApplication.class, args);  
	}  
}  
\`\`\`  
In this example:

* The class \`MyApplication\` is marked with \`@SpringBootApplication\`, indicating it's the main entry point for the Spring Boot application.  
* The \`main\` method uses \`SpringApplication.run(...)\` to bootstrap the application.

**How It Works Internally**

* Class Initialization: When you start your Spring Boot application, the JVM initializes the class annotated with \`@SpringBootApplication\`. This triggers the processing of all annotations on that class.  
* Configuration Loading: The \`@SpringBootConfiguration\` part ensures that any beans defined in this class or imported configuration classes are registered in the application context.  
* Auto-Configuration: The \`@EnableAutoConfiguration\` scans the classpath for available libraries and applies configuration based on what it finds. For instance:  
  * If you have included a database driver, it will configure a DataSource bean automatically.  
  * If you have included Spring MVC dependencies, it will set up an embedded web server.

* Component Scanning: The \`@ComponentScan\` annotation activates scanning for components in the specified package (the package of your main application class) and registers them as beans in the context.  
* Running the Application: The method \`SpringApplication.run(...)\` initializes the Spring context, loads all beans, and starts the embedded server (if applicable). It also handles any command-line arguments passed to the application.

Benefits of Using \`@SpringBootApplication\`

* **Simplified Configuration**: Reduces boilerplate code by combining multiple configurations into one annotation.  
* **Automatic Setup**: Automatically configures beans based on dependencies, allowing developers to focus on writing business logic rather than configuration.  
* **Clear Entry Point**: Clearly indicates where your application starts, improving readability and maintainability.

Conclusion  
The \`@SpringBootApplication\` annotation is a powerful tool in Spring Boot that streamlines application setup by combining essential configurations into one concise annotation. By leveraging this annotation, developers can create robust applications with minimal manual configuration while benefiting from Spring Boot's auto-configuration capabilities. Understanding its internal workings helps developers make better architectural decisions and troubleshoot issues effectively.

# Do you have any experience in Code review?

Yes, I have experience reviewing code for adherence to coding standards, readability, performance, and security best practices. I also focus on identifying potential bugs, ensuring proper test coverage, and reviewing logic and architectural decisions.

# How would you change the Tomcat server to any other server in your spring boot application.

Spring Boot uses Tomcat by default. To switch to another server (e.g., Jetty or Undertow), exclude the default Tomcat dependency in pom.xml or build.gradle and add the desired server dependency:

* For Jetty

  \<dependency\>

    \<groupId\>org.springframework.boot\</groupId\>

    \<artifactId\>spring-boot-starter-jetty\</artifactId\>

  \</dependency\>

* For Undertow

  \<dependency\>

    \<groupId\>org.springframework.boot\</groupId\>

    \<artifactId\>spring-boot-starter-undertow\</artifactId\>

  \</dependency\>

# What are the ACID properties of mysql?

The ACID properties in MySQL are a set of principles that ensure reliable processing of database transactions. These properties are crucial for maintaining data integrity and consistency, especially in systems that handle critical data. Here's a detailed explanation of each ACID property:

**Atomicity:** Atomicity ensures that a transaction is treated as a single unit of work, which means that either all operations within the transaction are completed successfully, or none of them are applied at all.

* Implementation in MySQL: In MySQL, atomicity is primarily managed through the use of transactions. If an error occurs during the execution of a transaction, any changes made during that transaction can be rolled back to maintain the initial state.  
* Key Features\*\*:  
  * The \`COMMIT\` statement is used to save changes made during a transaction.  
  * The \`ROLLBACK\` statement is used to undo changes if an error occurs.  
  * The \`autocommit\` setting controls whether each individual SQL statement is treated as a transaction.

**Consistency:** Consistency ensures that a transaction brings the database from one valid state to another valid state, maintaining all predefined rules, including constraints and triggers.

* Implementation in MySQL: MySQL uses various mechanisms to ensure consistency, such as foreign key constraints and unique indexes.  
* Key Features:  
  * When a transaction is committed, it must leave the database in a consistent state.  
  * Any integrity constraints defined on the database must be adhered to before and after the transaction.  
  * InnoDB's doublewrite buffer helps protect data from corruption during crashes.

**Isolation:** Isolation ensures that concurrently executed transactions do not affect each other’s execution. Each transaction should operate independently and transparently from others.

* Implementation in MySQL\*\*: MySQL supports different isolation levels that define how transaction integrity is visible to other transactions. These levels include Read Uncommitted, Read Committed, Repeatable Read (default), and Serializable.  
* Key Features:  
  * The \`SET TRANSACTION\` statement allows you to specify the isolation level for a transaction.  
  * Isolation prevents phenomena such as dirty reads (reading uncommitted data), non-repeatable reads (changes made by another transaction), and phantom reads (new rows added by another transaction).

**Durability:** Durability guarantees that once a transaction has been committed, it will remain so, even in the event of a system failure or crash.

* Implementation in MySQL\*\*: Durability is achieved through various features that ensure data is written to persistent storage.  
* Key Features:  
  * The InnoDB storage engine uses a write-ahead log (WAL) mechanism to ensure durability.  
  * The \`innodb\_flush\_log\_at\_trx\_commit\` variable controls how often logs are flushed to disk, impacting performance and durability trade-offs.  
  * Backups and recovery strategies also play a role in ensuring durability.

Summary  
The ACID properties—Atomicity, Consistency, Isolation, and Durability—are fundamental principles that underpin reliable transaction processing in MySQL. They ensure that databases can handle transactions safely and efficiently while maintaining data integrity even under adverse conditions such as system failures or concurrent access.

By adhering to these principles, MySQL provides robust support for applications requiring reliable data management, making it suitable for mission-critical environments.

# How would you implement spring security in your application?

**Step 1: Add Spring Security Dependency:**

* In pom.xml:

  \<dependency\>

    \<groupId\>org.springframework.boot\</groupId\>

    \<artifactId\>spring-boot-starter-security\</artifactId\>

  \</dependency\>

**Step 2: Create a Security Configuration Class:**

* Annotate with @EnableWebSecurity and extend WebSecurityConfigurerAdapter (if Spring Boot 2.x). In Spring Boot 3.x, implement SecurityFilterChain.  
* Override the configure(HttpSecurity http) method to define security rules.

  @Configuration

  @EnableWebSecurity

  public class SecurityConfig extends WebSecurityConfigurerAdapter {

  	@Override

  	protected void configure(HttpSecurity http) throws Exception {

      	http

          	.authorizeRequests()

              	.antMatchers("/public/\*\*").permitAll()  // Allow public endpoints

              	.anyRequest().authenticated()  // Secure other endpoints

          	.and()

          	.formLogin()  // Enable form-based login

          	.and()

          	.httpBasic();  // Enable HTTP basic authentication

  	}

  }

**Step 3: User Authentication:**

* In-memory authentication for simple cases or database-based authentication using UserDetailsService for custom user handling.  
* Example of in-memory authentication:

  @Override

  protected void configure(AuthenticationManagerBuilder auth) throws Exception {

  	auth.inMemoryAuthentication()

      	.withUser("user").password("{noop}password").roles("USER");

  }

**Step 4: Define Password Encoding (Optional):**

* Use a password encoder like BCryptPasswordEncoder.

  @Bean

  public PasswordEncoder passwordEncoder() {

  	return new BCryptPasswordEncoder();

  }

This will add basic security to the application with form login and basic authentication.

# How do you implement pagination, filtering and sorting?

1. **Pagination:**  
* Use Pageable in repository methods to return paginated data.  
* Example using a Spring Data JPA repository:

  @Repository

  public interface ProductRepository extends JpaRepository\<Product, Long\> {

  	Page\<Product\> findAll(Pageable pageable);

  }

* In the service/controller, pass Pageable to get paginated results:

  @GetMapping("/products")

  public Page\<Product\> getProducts(@RequestParam int page, @RequestParam int size) {

  	Pageable pageable \= PageRequest.of(page, size);

  	return productRepository.findAll(pageable);

  }

2. **Sorting:**  
* Use Sort with Pageable to sort the results by fields.  
* Example with sorting:

  @GetMapping("/products")

  public Page\<Product\> getProducts(@RequestParam int page, @RequestParam int size, @RequestParam String sortBy) {

  	Pageable pageable \= PageRequest.of(page, size, Sort.by(sortBy));

  	return productRepository.findAll(pageable);

  }

3. **Filtering:**  
* Add filtering criteria to the repository method, using @Query or dynamic queries with Specifications (for complex filters).  
* Example of filtering by product name:

  @Query("SELECT p FROM Product p WHERE p.name LIKE %:name%")

  Page\<Product\> findByNameContaining(@Param("name") String name, Pageable pageable);

This approach allows you to paginate, sort, and filter efficiently with Spring Data JPA.

# How do you implement validation?

Validation in Spring Boot ensures that incoming data, typically from user inputs in API requests, meets specific constraints. This helps prevent invalid or harmful data from being processed.

How to Implement Validation in a Spring Boot Application (Java 8):  
**Add Validation Dependencies:** In pom.xml, include the hibernate-validator dependency (usually auto-included with Spring Boot Web starter):  
\<dependency\>  
	\<groupId\>org.springframework.boot\</groupId\>  
	\<artifactId\>spring-boot-starter-validation\</artifactId\>  
\</dependency\>

**Use Validation Annotations:** Add annotations from javax.validation.constraints on the model fields. Example:  
public class User {  
	@NotNull  
	@Size(min \= 2, max \= 30\)  
	private String name;

	@Email  
	private String email;

	@Min(18)  
	private Integer age;

	// Getters and Setters  
}  
**Trigger Validation in Controllers:** Use @Valid or @Validated in the controller method to trigger validation. Example:  
@PostMapping("/users")  
public ResponseEntity\<String\> createUser(@Valid @RequestBody User user, BindingResult result) {  
	if (result.hasErrors()) {  
    	return ResponseEntity.badRequest().body(result.getFieldError().getDefaultMessage());  
	}  
	// Proceed with user creation  
	return ResponseEntity.ok("User created successfully");  
}

**Handling Validation Errors:** You can handle validation errors using BindingResult (as in the example above) or using global exception handling with @ControllerAdvice.

Common Annotations:

* **@NotNull**: Field cannot be null.  
* **@Size(min, max)**: Restricts the size (e.g., string length).  
* **@Email:** Validates email format.  
* **@Min and @Max:** Restricts the numeric values.

This ensures that the API only processes valid data, with easy-to-read constraints directly on model fields.

# How would you handle exceptions, global exceptions? Both for spring boot and java application?

To handle exceptions and global exceptions in both Spring Boot and Java applications, you can use structured approaches for clean and maintainable error handling.

## Spring Boot Applications:

**Local Exception Handling:**

* Use try-catch blocks in your methods to handle specific exceptions.

  @GetMapping("/product/{id}")

  public ResponseEntity\<Product\> getProductById(@PathVariable Long id) {

  	try {

      	Product product \= productService.findById(id);

      	return ResponseEntity.ok(product);

  	} catch (ProductNotFoundException e) {

      		return ResponseEntity.status(HttpStatus.NOT\_FOUND).body(null);

  	}

  }

**Global Exception Handling:**

* Use @ControllerAdvice to define a global exception handler.  
  @ControllerAdvice  
  public class GlobalExceptionHandler {  
  	@ExceptionHandler(ProductNotFoundException.class)  
  	public ResponseEntity\<String\> handleProductNotFound(ProductNotFoundException ex) {  
      		return ResponseEntity.status(HttpStatus.NOT\_FOUND).body(ex.getMessage());  
  	}  
    
  	@ExceptionHandler(Exception.class)  
  	public ResponseEntity\<String\> handleGenericException(Exception ex) {  
      		return ResponseEntity.status(HttpStatus.INTERNAL\_SERVER\_ERROR)

  .body("An error occurred");

  	}  
  }

**Custom Exception Class:**

* You can create custom exceptions to provide meaningful error messages.

  public class ProductNotFoundException extends RuntimeException {

  	public ProductNotFoundException(String message) {

      	super(message);

  	}

  }

## Plain Java Applications:

**Local Exception Handling:**

* Use try-catch blocks for handling specific exceptions.  
  public void readFile(String filePath) {  
  	try {

      	BufferedReader reader \= new BufferedReader(new FileReader(filePath));  
      	// process the file

  	} catch (FileNotFoundException e) {  
      		System.out.println("File not found: " \+ e.getMessage());  
  	} catch (IOException e) {  
      		System.out.println("Error reading file: " \+ e.getMessage());  
  	}  
  }

**Custom Exceptions:** 

* You can create custom exception classes to handle application-specific errors.

  public class InvalidUserInputException extends Exception {

  	public InvalidUserInputException(String message) {

      		super(message);

  	}

  }

* Throw and handle custom exceptions.

  public void processInput(String input) throws InvalidUserInputException {

  	if (input \== null || input.isEmpty()) {

      		throw new InvalidUserInputException("Input cannot be empty");

  	}

  }

Summary:

* **Spring Boot:** Use @ControllerAdvice and @ExceptionHandler for global exception handling.  
* **Java Applications:** Use try-catch blocks locally and create custom exception classes for better error management.

# How do you communicate between two microservices?

There are several ways to communicate between two microservices in a Spring Boot application. The most common methods are REST API, Message Queues, and gRPC. Here’s how you can implement these:

**1\. REST API Communication:** Use HTTP-based communication where one microservice acts as a client and another as a server.

Example using RestTemplate (for synchronous calls in Spring Boot):  
@Service  
public class ConsumerService {  
	private final RestTemplate restTemplate;

	public ConsumerService(RestTemplate restTemplate) {  
    		this.restTemplate \= restTemplate;  
	}

	public Product getProductById(Long id) {  
    	return restTemplate.getForObject("http://product-service/products/" \+ id, Product.class);  
	}  
}

For asynchronous calls, use WebClient (part of Spring WebFlux):  
@Service  
public class ConsumerService {  
	private final WebClient webClient \= WebClient.create();

	public Mono\<Product\> getProductById(Long id) {  
    	return webClient.get()  
        	.uri("http://product-service/products/{id}", id)  
        	.retrieve()  
        	.bodyToMono(Product.class);  
	}  
}

Service Discovery with Eureka (Optional):

* Use Eureka for service discovery instead of hardcoding URLs.  
* Register services with Eureka, and then use the service name in the URL for load balancing and dynamic discovery.

**2\. Message Queues (Asynchronous Communication):** Use messaging systems like RabbitMQ, Kafka, or ActiveMQ to exchange messages between microservices asynchronously.

Example using RabbitMQ:

* Producer Service:  
  @Service  
  public class ProducerService {  
  	@Autowired  
  	private RabbitTemplate rabbitTemplate;  
    
  	public void sendMessage(String message) {  
      		rabbitTemplate.convertAndSend("exchange", "routingKey", message);  
  	}  
  }  
* Consumer Service:

  @Service

  public class ConsumerService {

  	@RabbitListener(queues \= "queueName")

  	public void receiveMessage(String message) {

      		System.out.println("Received: " \+ message);

  	}

  }

**3\. gRPC (High-performance Communication):** Use gRPC for binary communication between microservices, which is more efficient than REST for high-throughput scenarios.

* Example with Spring Boot:  
  * Define the gRPC service in a .proto file.  
  * Implement gRPC server and client using the generated code.

**4\. Event-Driven Architecture:** Use events to propagate changes between microservices using an event bus like Spring Cloud Stream with Kafka or RabbitMQ.  
**Example with Kafka:**

* Producer:

  @Service

  public class OrderService {

  	@Autowired

  	private KafkaTemplate\<String, Order\> kafkaTemplate;


  	public void createOrder(Order order) {

      		kafkaTemplate.send("order-topic", order);

  	}

  }

* Consumer:

  @KafkaListener(topics \= "order-topic")

  public void listen(Order order) {

  	System.out.println("Received order: " \+ order);

  }

Summary:

* **REST API (Synchronous):** Use RestTemplate or WebClient for HTTP calls.  
* **Message Queues (Asynchronous):** Use RabbitMQ, Kafka, or ActiveMQ for messaging.  
* **gRPC (High-performance):** Use gRPC for efficient binary communication.  
* **Event-Driven Architecture:** Use Kafka or RabbitMQ with Spring Cloud Stream for event-based communication.

# How do you expose your end points?

In Spring Boot, you expose your endpoints (APIs) by defining controller methods and mapping them to specific HTTP routes using annotations like @GetMapping, @PostMapping, etc. Here’s how you can expose them:

Use of @RestController and Mapping Annotations:

* @RestController is used to indicate that the class will handle RESTful web requests and automatically serializes responses to JSON.  
* Use @RequestMapping, @GetMapping, @PostMapping, @PutMapping, @DeleteMapping to map HTTP methods to specific endpoints. Example:

  @RestController

  @RequestMapping("/api/products")

  public class ProductController {


  	// GET endpoint to retrieve all products

  	@GetMapping

  	public List\<Product\> getAllProducts() {

      	return productService.getAllProducts();

  	}


  	// GET endpoint to retrieve a product by ID

  	@GetMapping("/{id}")

  	public Product getProductById(@PathVariable Long id) {

      	return productService.getProductById(id);

  	}


  	// POST endpoint to create a new product

  	@PostMapping

  	public Product createProduct(@RequestBody Product product) {

      	return productService.saveProduct(product);

  	}


  	// PUT endpoint to update a product

  	@PutMapping("/{id}")

  	public Product updateProduct(@PathVariable Long id, @RequestBody Product product) {

      	return productService.updateProduct(id, product);

  	}


  	// DELETE endpoint to delete a product by ID

  	@DeleteMapping("/{id}")

  	public void deleteProduct(@PathVariable Long id) {

      	productService.deleteProduct(id);

  	}

  }

2\. OpenAPI/Swagger for Documentation and Testing:

* Use Swagger to automatically generate and expose documentation for your REST API endpoints.  
* Add the following dependencies to pom.xml:

  \<dependency\>

  	\<groupId\>org.springdoc\</groupId\>

  	\<artifactId\>springdoc-openapi-ui\</artifactId\>

  	\<version\>1.6.14\</version\>

  \</dependency\>

* Swagger UI will be exposed at /swagger-ui.html, where you can see and test your API endpoints.

3\. Customizing Endpoint Paths:

* You can customize your endpoints by using @RequestMapping at both the class and method levels to group and define specific paths.  
* Example:

  @RequestMapping("/api/v1/users")

  public class UserController {

  	@GetMapping("/all") // Exposes GET /api/v1/users/all

  	public List\<User\> getAllUsers() { ... }


  	@PostMapping("/create") // Exposes POST /api/v1/users/create

  	public User createUser(@RequestBody User user) { ... }

  }

4\. Versioning Endpoints (Optional):

* You can version your API endpoints by adding version numbers in the URL (e.g., /api/v1/users), using custom headers, or request parameters.

Summary:

* Use @RestController and @Mapping annotations to expose endpoints.  
* For detailed endpoint management, consider Swagger/OpenAPI for auto-generated documentation and testing.  
* You can customize endpoints with paths and version them for different API versions.

# SOLID principles in design pattern.

Yes, the SOLID principles are indeed applicable and widely followed in Java programming. These principles provide a framework for designing software that is more maintainable, scalable, and understandable. Here’s how each of the SOLID principles can be implemented in Java:

**Single Responsibility Principle (SRP)**: A class should have only one reason to change, meaning it should have only one responsibility.

* **Java Implementation**: In Java, you can achieve SRP by ensuring that each class focuses on a single task or functionality. For example, if you have a class that handles both user data and user authentication, you should separate these concerns into two distinct classes.

**Open-Closed Principle (OCP):** Software entities should be open for extension but closed for modification.

* **Java Implementation:** You can implement OCP in Java by using interfaces or abstract classes. For instance, if you have a class that calculates areas of different shapes, instead of modifying this class every time a new shape is added, you can create new subclasses that extend the base class without changing the existing code.

**Liskov Substitution Principle (LSP):** Objects of a superclass should be replaceable with objects of a subclass without affecting the correctness of the program.

* **Java Implementation**: In Java, this principle can be enforced by ensuring that subclasses adhere to the behavior expected from their parent classes. For example, if a method accepts a parent class type, it should work correctly with any subclass instances.

**Interface Segregation Principle (ISP):** Clients should not be forced to depend on interfaces they do not use.

* **Java Implementation**: This principle can be implemented by creating small, specific interfaces instead of large, general-purpose ones. For example, if you have an interface with multiple methods that not all implementing classes need, consider splitting it into smaller interfaces tailored to specific functionalities.

**Dependency Inversion Principle (DIP):** High-level modules should not depend on low-level modules; both should depend on abstractions.

* **Java Implementation:** In Java, you can apply DIP by using dependency injection frameworks like Spring. Instead of a class instantiating its dependencies directly, it receives them through constructors or setters, which promotes loose coupling and makes testing easier.

Conclusion  
The SOLID principles are not exclusive to any programming language but are particularly well-suited for object-oriented languages like Java. By adhering to these principles, Java developers can create systems that are easier to manage and extend over time. Following SOLID principles leads to better software design and improved code quality, making it easier to adapt to changing requirements and maintain the application in the long run.

# Java 8 interview question

Here are some important Java 8 interview questions that are commonly asked, along with brief explanations of their topics:

**What are the key features of Java 8?**

* Java 8 introduced several significant features including:  
  * **Lambda Expressions**: Allow for more concise code by enabling functional programming.  
  * **Stream API:** Facilitates functional-style operations on streams of data.  
  * **Functional Interfaces:** Interfaces with a single abstract method, allowing for behavior parameterization.  
  * **Optional Class:** Helps in handling null values more gracefully.  
  * **New Date and Time API:** A comprehensive API for date and time manipulation.

**What is a Lambda Expression?**

* A lambda expression is a concise way to represent an anonymous function (a function without a name) that can be passed around as if it were an object.

**Explain the Stream API.**

* The Stream API allows for functional-style operations on collections of objects, enabling operations like filtering, mapping, and reducing in a more readable manner.

**What is the purpose of the Optional class?**

* The Optional class is used to represent a value that may or may not be present, helping to avoid \`NullPointerExceptions\` and making the code clearer.

**What are method references?**

* Method references provide a way to refer to methods or constructors without invoking them, improving code readability and reducing boilerplate.

**How do you create a functional interface?**

* A functional interface can be created by defining an interface with a single abstract method. An example is \`Runnable\`.

**What is the difference between \`map()\` and \`flatMap()\` in Streams?**

* \`map()\` transforms each element of the stream into another object, while \`flatMap()\` flattens nested structures into a single stream.

**What are default methods in interfaces?**

* Default methods allow you to add new methods to interfaces without breaking existing implementations, providing a way to evolve interfaces.

**Explain the significance of the \`forEach\` method in Streams.**

* The \`forEach\` method performs an action for each element of the stream, often used for side effects like printing elements.

**How does the \`reduce()\` method work in Streams?**

* The \`reduce()\` method combines elements of a stream into a single result using an associative accumulation function.

**What are some common functional interfaces provided in Java 8?**

* Common functional interfaces include:  
  * **Predicate**: Represents a boolean-valued function.  
  * **Consumer**: Represents an operation that accepts a single input argument.  
  * **Function**: Represents a function that accepts one argument and produces a result.  
  * **Supplier**: Represents a supplier of results.

Java 8 introduced several common functional interfaces that facilitate functional programming. These interfaces are part of the `java.util.function` package and are designed to be used with lambda expressions. Here’s a detailed explanation of some of the most important ones:

**Predicate:** A `Predicate<T>` is a functional interface that represents a single argument function that returns a boolean value. It is often used for filtering collections. 

Key Methods:

* boolean **test(T t):** Evaluates the predicate on the given argument.  
* default Predicate\<T\> and(Predicate\<? super T\> other): Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another.  
* default Predicate\<T\> or(Predicate\<? super T\> other): Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another.  
* default Predicate\<T\> **negate():** Returns a predicate that is the logical negation of this predicate.

  java

  import java.util.function.Predicate;


  public class PredicateExample {

      public static void main(String\[\] args) {

          Predicate\<Integer\> isEven \= num \-\> num % 2 \== 0;

          System.out.println(isEven.test(4)); *// true*

          System.out.println(isEven.test(5)); *// false*

      }

  }

Use Cases:

* Filtering collections using the filter() method in streams.  
* Combining predicates using logical operations.

**Consumer:** A Consumer\<T\> is a functional interface that represents an operation that accepts a single input argument and returns no result. It's mainly used for operations that perform actions rather than return values.   
Key Methods:

* void **accept(T t):** Performs the operation on the given argument.  
* default Consumer\<T\> **andThen**(Consumer\<? super T\> after): Returns a composed consumer that performs, in sequence, this operation followed by the after operation.  
  import java.util.function.Consumer;


  public class ConsumerExample {  
      public static void main(String\[\] args) {  
          Consumer\<String\> print \= s \-\> System.out.println(s);  
          print.accept("Hello, World\!"); // Outputs: Hello, World\!  
      }  
  }

Use Cases:

* Iterating over collections to perform actions like printing or modifying elements.

**Function:** A Function\<T, R\> is a functional interface that represents a function that accepts one argument and produces a result. It can be used for transforming data. Key Methods:

* R **apply(T t):** Applies this function to the given argument.  
* default \<V\> Function\<T, V\> andThen(Function\<? super R, ? extends V\> after): Returns a composed function that first applies this function to its input, and then applies the after function to the result.

  import java.util.function.Function;


  public class FunctionExample {

      public static void main(String\[\] args) {

          Function\<Integer, String\> intToString \= Object::toString;

          System.out.println(intToString.apply(123)); // Outputs: "123"

      }

  }

Use Cases: Mapping values in collections using the map() method in streams.

**Supplier:** A Supplier\<T\> is a functional interface that represents a supplier of results. It does not take any arguments but returns a value. Key Methods:

* T **get()**: Gets a result.

  import java.util.function.Supplier;


  public class SupplierExample {

      public static void main(String\[\] args) {

          Supplier\<String\> stringSupplier \= () \-\> "Hello, Supplier\!";

          System.out.println(stringSupplier.get()); // Outputs: Hello, Supplier\!

      }

  }

Use Cases: Generating values on demand, such as creating new instances or providing configuration values.

**Summary**  
These functional interfaces provide powerful tools for writing clean and efficient code in Java 8\. They enable developers to leverage lambda expressions effectively, making code more concise and expressive. By understanding how to use these interfaces, you can enhance your ability to work with streams and functional programming paradigms in Java.

**What improvements were made to concurrency in Java 8?**

* Java 8 introduced \`CompletableFuture\` for easier asynchronous programming and enhancements to existing concurrency utilities.

**How do you handle exceptions in lambda expressions?**

* Since lambda expressions cannot throw checked exceptions directly, you typically wrap them in runtime exceptions or use helper methods.

**What is the Date-Time API introduced in Java 8?**

* The new Date-Time API provides classes like \`LocalDate\`, \`LocalTime\`, and \`LocalDateTime\` for better handling of date and time compared to the old \`java.util.Date\` and \`java.util.Calendar\` classes.

These questions cover fundamental concepts introduced in Java 8 and are essential for developers preparing for interviews focused on this version of Java.

# Stream and parallel Stream.

In Java 8, the concept of \*\*streams\*\* and \*\*parallel streams\*\* was introduced to facilitate functional-style operations on collections. Here’s a detailed explanation of both:

**What is a Stream?**  
A Stream in Java is a sequence of elements that can be processed in a functional style. It allows developers to express complex data processing queries in a more readable and concise manner. Streams are not data structures; rather, they provide a view of data stored in collections, arrays, or I/O channels.

Characteristics of Streams:

* **No Storage**: Streams do not store data. They operate on the data source (like collections) and provide a pipeline for processing.  
* **Laziness:** Stream operations are lazy; they are not executed until a terminal operation is invoked.  
* **Functional in Nature:** Streams support functional programming features, allowing operations like map, filter, and reduce.  
* **Possibly Unbounded:** Streams can represent finite or infinite sequences of elements.

**Creating Streams:** Streams can be created from various sources:

* **From Collections:** Using the \`stream()\` method.

     \`\`\`java

     List\<String\> list \= Arrays.asList("a", "b", "c");

     Stream\<String\> stream \= list.stream();

     \`\`\`

* **From Arrays:** Using \`Arrays.stream()\`.

     \`\`\`java

     String\[\] array \= {"a", "b", "c"};

     Stream\<String\> stream \= Arrays.stream(array);

     \`\`\`

* **From Values**: Using \`Stream.of()\`.

     \`\`\`java

     Stream\<String\> stream \= Stream.of("a", "b", "c");

     \`\`\`

Stream Operations: Streams support two types of operations:

* **Intermediate Operations:** These return a new stream and are lazy (e.g., \`filter\`, \`map\`, \`sorted\`).  
* **Terminal Operations:** These produce a result or side-effect and terminate the stream (e.g., \`forEach\`, \`collect\`, \`reduce\`).

**What is a Parallel Stream?**

* A Parallel Stream is an extension of the Stream API that enables concurrent processing of elements using multiple threads. This feature is designed to take advantage of multi-core processors, allowing for potentially improved performance when processing large datasets.

Characteristics of Parallel Streams:

* **Multi-threaded Execution**: Parallel streams utilize multiple threads to process elements concurrently.  
* **Fork/Join Framework**: They leverage the Fork/Join framework for managing parallel tasks efficiently.  
* **Order of Execution**: The order of execution is not guaranteed; thus, parallel streams should be used when the order does not affect the outcome.

Creating Parallel Streams:

* Using \`parallelStream()\` Method on Collections\*\*:

     \`\`\`java

     List\<String\> list \= Arrays.asList("a", "b", "c");

     Stream\<String\> parallelStream \= list.parallelStream();

     \`\`\`

* Using \`parallel()\` Method on an Existing Stream\*\*:

     \`\`\`java

     Stream\<String\> stream \= list.stream().parallel();

     \`\`\`

**Performance Considerations:** While parallel streams can improve performance, they are not always faster than sequential streams due to overhead from thread management and context switching. It is essential to consider:

* The size of the dataset: Larger datasets benefit more from parallel processing.  
* The nature of operations: CPU-bound tasks are better suited for parallel execution than I/O-bound tasks.  
* Thread contention and shared resources: Care must be taken with shared mutable data to avoid concurrency issues.  
  \`\`\`java  
  import java.util.Arrays;  
  import java.util.List;  
    
  public class StreamExample {  
  	public static void main(String\[\] args) {  
      	List\<Integer\> numbers \= Arrays.asList(1, 2, 3, 4, 5);  
    
      	// Sequential stream  
      	numbers.stream()  
             	.filter(n \-\> n % 2 \== 0\)  
             	.forEach(System.out::println); // Outputs even numbers  
    
      	// Parallel stream  
      	numbers.parallelStream()  
             	.filter(n \-\> n % 2 \== 0\)  
             	.forEach(System.out::println); // Outputs even numbers in no specific order  
  	}  
  }  
  \`\`\`

In summary, streams provide a powerful way to process collections in Java 8 using functional programming paradigms, while parallel streams enhance this capability by allowing concurrent processing across multiple CPU cores. When used appropriately, they can significantly simplify code and improve performance.

# OOPs, JDBC, Serialisation, Threads, Collection, Map, How internally HashSet.

Let's delve into the internal workings of `HashMap` and `HashSet` in Java's Collection Framework. Since `HashSet` is implemented using `HashMap` internally, understanding `HashMap` is crucial.

**HashMap Internal Working:** `HashMap` stores data in key-value pairs. It uses a technique called *hashing* to efficiently store and retrieve elements.

1. **Hashing:**  
   * When you put a key-value pair into a `HashMap`, the key's `hashCode()` method is called to generate an integer hash code.  
   * This hash code is then used to determine the *bucket* (index in an internal array) where the entry will be stored.  
2. **Internal Array (Bucket Array or Table):**  
   * `HashMap` maintains an internal array of `Node` objects (before Java 8\) or `Entry` objects (in older versions) or now `Node<K,V>` (from Java 8). This array is often referred to as the "bucket array" or "table". Each index in this array is a "bucket."  
3. **Collision Handling (Chaining or Separate Chaining):**  
   * It's possible for different keys to produce the same hash code (a *collision*). `HashMap` handles collisions using *chaining* (also known as *separate chaining*).  
   * Each bucket in the array actually holds a linked list of `Node` objects. If two keys hash to the same bucket, both entries are stored in the same linked list at that bucket's index.  
4. **Node Structure (Java 8 and later):**  
   * In Java 8, a significant optimization was introduced. When a bucket's linked list becomes too long (reaches a threshold, typically 8), it is converted into a *balanced tree* (specifically, a *red-black tree*). This improves performance in worst-case scenarios where many keys hash to the same bucket.  
   * The `Node` class (or `Entry` in older versions) stores the key, value, hash code, and a pointer to the next `Node` in the linked list (or tree node).  
5. **Putting an Element:**  
   * Calculate the hash code of the key.  
   * Determine the bucket index using `index = hash & (table.length - 1)` (this is a fast way to get the index within the array bounds).  
   * If the bucket is empty, create a new `Node` and place it in the bucket.  
   * If the bucket is not empty (collision):  
     * Iterate through the linked list (or tree) at that bucket.  
     * If a key with the same `equals()` method already exists, update the value.  
     * Otherwise, add a new `Node` to the end of the list (or insert into the tree).  
6. **Getting an Element:**  
   * Calculate the hash code of the key.  
   * Determine the bucket index.  
   * Iterate through the linked list (or tree) at that bucket.  
   * Use the `equals()` method to compare the keys.  
   * If a match is found, return the corresponding value.  
7. **Resizing:**  
   * As more elements are added, the `HashMap` may become too full, leading to increased collisions and slower performance.  
   * When the *load factor* (default 0.75) is reached, the `HashMap` is *resized*. A new array with double the capacity is created, and all existing entries are rehashed and redistributed into the new buckets. This is a relatively expensive operation.

**HashSet Internal Working:** HashSet is implemented using HashMap internally.

1. **Internal HashMap:**  
   * `HashSet` maintains a `HashMap` instance as a private member.  
2. **Storing Elements:**  
   * When you add an element to a `HashSet`, it is actually stored as a *key* in the internal `HashMap`.  
   * A dummy `Object` instance (called `PRESENT`) is used as the *value* associated with each key.  
3. **Uniqueness:**  
   * Because `HashMap` only allows unique keys, `HashSet` automatically enforces uniqueness of its elements. If you try to add a duplicate element, the `put()` method of the internal `HashMap` will simply return the old value (which is `PRESENT`), and the `add()` method of `HashSet` will return `false`, indicating that the element was not added.  
4. **Operations:**  
   * All operations on `HashSet` (add, remove, contains, etc.) are delegated to the internal `HashMap`.

**Key Differences and Summary:**

| Feature | HashMap | HashSet |
| ----- | ----- | ----- |
| Purpose | Stores key-value pairs | Stores unique elements |
| Internal | Uses an array of linked lists/trees (buckets) | Uses a HashMap internally |
| Element Storage | Stores key-value pairs in `Node` objects | Stores elements as keys in the internal HashMap, with a dummy value |
| Uniqueness | Keys must be unique | Elements must be unique |

In essence, `HashSet` is a simplified wrapper around `HashMap` that leverages its key uniqueness feature to store a set of unique elements. Both rely on hashing for efficient performance. Understanding `HashMap` is essential for understanding how `HashSet` works.

# Stored procedure and trigger.

Both \*\*stored procedures\*\* and \*\*triggers\*\* are essential components of SQL databases, allowing for the encapsulation of business logic and automation of tasks. Here’s a detailed explanation of each:

**Stored Procedures:** A stored procedure is a precompiled collection of one or more SQL statements that can be executed as a single unit. Stored procedures are stored in the database and can be invoked by applications or other procedures.

Key Features

* **Modularity**: Stored procedures allow for modular programming, enabling code reuse.  
* **Performance**: They are precompiled, which can lead to performance improvements since the execution plan is cached.  
* **Security**: Stored procedures can restrict direct access to the underlying tables, allowing users to execute operations without exposing the data structure.  
* **Parameters**: They can accept input parameters and return output parameters or result sets.

Syntax  
The basic syntax for creating a stored procedure is as follows:  
\`\`\`sql  
CREATE PROCEDURE procedure\_name (parameter1 datatype, parameter2 datatype)  
AS  
BEGIN  
	\-- SQL statements  
END;  
\`\`\`  
Here’s an example of a simple stored procedure that retrieves employee details based on their ID:  
\`\`\`sql  
CREATE PROCEDURE GetEmployeeDetails (@EmployeeID INT)  
AS  
BEGIN  
	SELECT \* FROM Employees WHERE EmployeeID \= @EmployeeID;  
END;  
\`\`\`

Invocation: To execute the stored procedure:  
\`\`\`sql  
EXEC GetEmployeeDetails @EmployeeID \= 1;  
\`\`\`  
**Triggers:** A trigger is a special type of stored procedure that automatically executes (or "fires") in response to specific events on a particular table or view, such as INSERT, UPDATE, or DELETE operations.

Key Features

* **Automatic Execution**: Triggers run automatically in response to changes in the database.  
* **Data Integrity**: They help maintain data integrity by enforcing rules and constraints.  
* **Audit Trails**: Triggers can be used to create audit trails by logging changes made to data.

Syntax: The basic syntax for creating a trigger is as follows:  
\`\`\`sql  
CREATE TRIGGER trigger\_name  
ON table\_name  
AFTER INSERT | UPDATE | DELETE  
AS  
BEGIN  
	\-- SQL statements  
END;  
\`\`\`  
Here’s an example of a trigger that logs changes to an employee's salary:  
\`\`\`sql  
CREATE TRIGGER LogSalaryChange  
ON Employees  
AFTER UPDATE  
AS  
BEGIN  
	INSERT INTO SalaryChangeLog (EmployeeID, OldSalary, NewSalary, ChangeDate)  
	SELECT  
    	inserted.EmployeeID,  
    	deleted.Salary AS OldSalary,  
    	inserted.Salary AS NewSalary,  
    	GETDATE() AS ChangeDate  
	FROM  
    	inserted  
	JOIN  
    	deleted ON inserted.EmployeeID \= deleted.EmployeeID;  
END;  
\`\`\`  
Execution Context: Triggers do not require explicit invocation; they are automatically executed when the specified event occurs on the associated table.

Summary  
**Stored Procedures:** Used for encapsulating business logic and performing complex operations with improved performance and security.  
**Triggers**: Automatically execute in response to data modifications, ensuring data integrity and enabling auditing capabilities.

Understanding these concepts is essential for database management and application development.

# Index in Sql.

An index in SQL is a database object that improves the speed of data retrieval operations on a table at the cost of additional storage space and maintenance overhead. Here’s a detailed explanation of what an index is, its types, advantages, disadvantages, and how to create and manage indexes.

**What is an Index?**  
An index is similar to an index in a book, which helps you quickly locate information without having to read through every page. In SQL databases, an index allows the database management system (DBMS) to find rows more efficiently based on the values in one or more columns.

Key Features:

* **Lookup Table:** Indexes act as lookup tables that point to the actual data in a table.  
* **Performance Improvement**: They significantly speed up SELECT queries, especially when searching for specific rows.  
* **Storage Requirement**: Indexes require additional storage space because they maintain a separate structure that holds pointers to the data.

**Single-Column Index:** An index created on a single column of a table.  
 	\`\`\`sql  
 	CREATE INDEX idx\_column\_name ON table\_name(column\_name);  
 	\`\`\`  
**Composite Index:** An index created on two or more columns of a table.  
 	\`\`\`sql  
 	CREATE INDEX idx\_multiple\_columns ON table\_name(column1, column2);  
 	\`\`\`  
**Unique Index**: Ensures that all values in the indexed column are unique. It prevents duplicate entries.  
 	\`\`\`sql  
 	CREATE UNIQUE INDEX idx\_unique\_column ON table\_name(column\_name);  
 	\`\`\`  
**Clustered Index**: Determines the physical order of data in a table. There can be only one clustered index per table.

* Automatically created when you define a primary key.

**Non-Clustered Index**: A separate structure from the data that holds pointers back to the original rows. You can have multiple non-clustered indexes on a table.

**Full-Text Index**: Used for full-text searches on large text columns.

**Advantages of Using Indexes**

* **Faster Query Performance**: Significantly speeds up data retrieval operations, especially for large datasets.  
* **Improved Sorting and Filtering**: Enhances performance for sorting and filtering operations in queries.  
* **Data Integrity**: Unique indexes help maintain data integrity by preventing duplicate values.

**Disadvantages of Using Indexes**

* **Increased Storage Space:** Requires additional disk space to store the index structure.  
* **Slower Data Modification Operations:** Can slow down INSERT, UPDATE, and DELETE operations because the index must also be updated whenever data changes.  
* **Maintenance Overhead**: Requires periodic maintenance to optimize performance, especially after large data modifications.

**Creating and Managing Indexes**

* Creating an Index: To create an index, you use the \`CREATE INDEX\` statement:

  \`\`\`sql

  CREATE INDEX index\_name ON table\_name(column1, column2);

  \`\`\`

* Dropping an Index: To remove an index when it is no longer needed:

  \`\`\`sql

  DROP INDEX index\_name ON table\_name;

  \`\`\`

**Renaming an Index:** While SQL does not have a direct command for renaming indexes, you can drop and recreate them with the new name.

**When to Avoid Using Indexes:** Indexes should be avoided in certain scenarios:

* On small tables where full scans are fast enough.  
* On columns with high update frequency or many NULL values.  
* When there are frequent bulk updates or inserts.

In summary, indexes are powerful tools for optimizing query performance in SQL databases. Understanding how to effectively use and manage them is crucial for database design and performance tuning.

# What is JPA Repository and CRUDRepository?

In Spring Data JPA, both JpaRepository and CrudRepository are interfaces used to interact with the underlying database by providing common CRUD operations. However, they have some differences in the additional functionality they provide.

**CrudRepository:**

* It is the base interface for generic CRUD (Create, Read, Update, Delete) operations in Spring Data.  
* Provides basic CRUD functionalities like saving, finding, deleting, and updating entities.  
* Key Methods in CrudRepository:

  public interface CrudRepository\<T, ID\> extends Repository\<T, ID\> {

  	\<S extends T\> S save(S entity);      	// Save an entity

  	Optional\<T\> findById(ID id);         	// Find an entity by ID

  	Iterable\<T\> findAll();               	// Find all entities

  	long count();                        	// Count total entities

  	void deleteById(ID id);              	// Delete entity by ID

  	void delete(T entity);               	// Delete an entity

  }

Use Case:

* When you only need basic CRUD operations, CrudRepository is sufficient.

  public interface UserRepository extends CrudRepository\<User, Long\> {

  }

**JpaRepository:**

* It extends CrudRepository and adds more functionality specific to JPA (Java Persistence API).  
* Provides more JPA-specific operations like batch operations, pagination, and sorting.

Key Methods in JpaRepository:  
public interface JpaRepository\<T, ID\> extends PagingAndSortingRepository\<T, ID\> {  
	List\<T\> findAll();                            	// Find all entities  
	List\<T\> findAll(Sort sort);                   	// Find all with sorting  
	Page\<T\> findAll(Pageable pageable);           	// Find all with pagination  
	void flush();                                 	// Flush changes to the database  
	\<S extends T\> List\<S\> saveAll(Iterable\<S\> entities);  // Save multiple entities  
	void deleteInBatch(Iterable\<T\> entities);     	// Batch delete entities  
}

Use Case:

* Use JpaRepository when you need advanced database operations, including pagination, sorting, and batch processing.

  public interface ProductRepository extends JpaRepository\<Product, Long\> {

  }

| Feature | CrudRepository | JpaRepository |
| :---- | :---- | :---- |
| Basic CRUD operations | Yes | Yes |
| Pagination & Sorting | No | Yes |
| Batch Operations | No | Yes |
| JPA-specific features | No | Yes(e.g., flushing, batch deletes) |

Conclusion:

* Use CrudRepository if you need simple CRUD operations without pagination or sorting.  
* Use JpaRepository if you need additional JPA-specific functionalities like pagination, sorting, and batch operations. It extends CrudRepository, so it includes all the basic CRUD features.

# What is Optional Class?

* **Purpose:** The `Optional` class, introduced in Java 8, is a container object that may or may not hold a non-null value.  
* **Motivation:**  
  * **Handling NullPointerExceptions:** Before `Optional`, dealing with null values often led to `NullPointerExceptions`, which can be difficult to debug and make code less robust.  
  * **Improved Code Readability:** `Optional` provides a more concise and expressive way to handle potential null values, making the code easier to read and understand.

**Key Methods:**

* **`of(T value)`:** Creates an `Optional` instance containing the specified non-null value.  
* **`ofNullable(T value)`:** Creates an `Optional` instance containing the specified value if it's not null; otherwise, returns an empty `Optional`.  
* **`empty()`:** Creates an empty `Optional` instance.  
* **`isPresent()`:** Returns `true` if the `Optional` instance contains a value, `false` otherwise.  
* **`get()`:** Returns the value if present; otherwise, throws a `NoSuchElementException`.  
* **`orElse(T other)`:** Returns the value if present; otherwise, returns the specified default value.1  
* **`orElseGet(Supplier<? extends T> other)`:** Returns the value if present; otherwise, returns the result produced by the provided supplier function.  
* **`ifPresent(Consumer<? super T> action)`:** Performs the given action if a value is present.2  
* **`ifPresentOrElse(Consumer<? super T> action, Runnable emptyAction)`:** Performs the given action if a value is present, or the empty action otherwise.3  
* **`map(Function<? super T, ? extends U> mapper)`:** If a value is present, applies the provided mapping function to it, and if the result is non-null, returns an `Optional`4 containing the result.  
* **`flatMap(Function<? super T, Optional<U>> mapper)`:** If a value is present, applies the provided mapping function to it, and returns the result of the mapping; otherwise, returns an empty `Optional`.  
* **`filter(Predicate<? super T> predicate)`:** If a value is present and the value matches the given predicate, returns an `Optional`5 containing the value, otherwise returns an empty `Optional`.

  import java.util.Optional;


  public class OptionalExample {


      public static void main(String\[\] args) {

          String name \= "John Doe";

          Optional\<String\> optionalName \= Optional.ofNullable(name);


          if (optionalName.isPresent()) {

              System.out.println("Name: " \+ optionalName.get());

          } else {

              System.out.println("Name is not present.");

          }


          String defaultName \= optionalName.orElse("Unknown");

          System.out.println("Default Name: " \+ defaultName); 

      }

  }

**Benefits**

* **Reduced Null Checks:** Eliminates the need for explicit null checks, making the code more concise and readable.6  
* **Improved Error Handling:** Helps prevent `NullPointerExceptions` by providing a safe way to handle potential null values.  
* **Enhanced Code Maintainability:** Makes code more maintainable by clearly indicating the possibility of null values.

# D/f b/w Serialisation and Externalizable?

The key difference between Serializable and Externalizable interfaces lies in how they handle the serialization and deserialization process of an object’s state. While both are used for the same purpose (converting an object to a stream of bytes for storage or transmission), they differ in control and implementation.

Serializable Interface:

* **Purpose**: Serializable is a marker interface (has no methods) that provides automatic serialization functionality. It tells the JVM that the object can be serialized using the default serialization process.  
* **Serialization Control**:   
  * Automatic and handled by the JVM. You have little to no control over the serialization process.  
  * The JVM serializes all non-transient and non-static fields of the object by default.  
* **Deserialization:** Similarly, deserialization is handled by the JVM, and it reconstructs the object from the serialized byte stream.  
* **Usage**: Typically used when you want a simple and straightforward serialization process.  
* **Performance:** Can be slower compared to Externalizable because it serializes all the non-transient fields automatically.

  public class Employee implements Serializable {

  	private static final long serialVersionUID \= 1L;

  	private String name;

  	private int age;


  	// Getters and setters

  }

Pros:

* Simple to use.  
* Requires minimal code.  
* Default behavior is sufficient for most cases.

Cons:

* Lack of control over what gets serialized.  
* Not optimized for performance when fine-grained control is needed.

**Externalizable Interface:**

* **Purpose:** Externalizable is a more customizable interface that gives you complete control over the serialization and deserialization process by requiring the implementation of writeExternal() and readExternal() methods.  
* **Serialization Control: Manual**. You explicitly define which fields get serialized and how they are serialized in the writeExternal() method.  
* You can choose to only serialize specific fields, exclude others, or even modify the data before serialization.  
* **Deserialization**: You also need to manually implement the readExternal() method to handle the deserialization process, giving you complete control over how the object’s state is restored.  
* **Usage**: Use when you need fine-grained control over what gets serialized, for optimization purposes, or when dealing with complex object states.  
* Performance: Better performance in cases where you need optimized serialization, as you can serialize only essential data and skip unnecessary fields.

  public class Employee implements Externalizable {

  	private String name;

  	private int age;


  	// Mandatory no-arg constructor

  	public Employee() {}


  	@Override

  	public void writeExternal(ObjectOutput out) throws IOException {

      	out.writeObject(name);

      	out.writeInt(age);

  	}


  	@Override

  	public void readExternal(ObjectInput in) throws IOException, ClassNotFoundException {

      	name \= (String) in.readObject();

      	age \= in.readInt();

  	}

  }

Pros:

* Complete control over serialization and deserialization.  
* Potentially better performance when optimized properly.

Cons:

* Requires more code to implement.  
* More error-prone since you have to manually handle serialization.

Key Differences:

| Feature | Serializable | Externalizable |
| :---- | :---- | :---- |
| Type | Marker Interface(no methods) | Customizable Interface(2 methods) |
| Serialization | Automatic(JVM handles it) | Manual(you define what to serialize) |
| Control | Little to no control over process | Full control over Ser/Des |
| Implementation | Simple and requires minimal code | Requires more code, but offers flexibility. |
| Performance | Slower(because JVM serializes everything by default.) | Faster(if optimized correctly) |
| Default Behavior | Serializes all non-transient fields | You choose what to serialize |
| Use case | For simple objects with default behavior. | For custom, optimized, or complex objects. |

**When to Use Which in Spring Boot:**

* **Serializable**: Use when you don’t need special control over how the object is serialized and deserialized. Ideal for simple use cases, where the default serialization provided by the JVM is sufficient.  
* **Externalizable**: Use when performance optimization is necessary, or when you need more fine-grained control over which fields are serialized or how the serialization process is done (e.g., serializing only necessary parts of a large object).

Both interfaces can be used in Spring Boot applications for serializing data between services, caching objects, or for storing data in databases like Redis, depending on the specific requirements of your application.

# D/f b/w Hashtable and ConcurrentHashMap(segment).

The main difference between Hashtable and ConcurrentHashMap in Java lies in their synchronization mechanisms and their performance in concurrent environments. Here’s a breakdown of the key differences:

**Thread-Safety Mechanism:**  
Hashtable: 

* **Thread-safe:** Every method in Hashtable is synchronized, meaning the entire object is locked whenever any thread performs a read or write operation.  
* This means that only one thread can access or modify the Hashtable at a time, which ensures thread safety but leads to poor scalability in a highly concurrent environment.

**ConcurrentHashMap:**

* **Thread-safe with better concurrency**: Instead of locking the entire map, ConcurrentHashMap uses a mechanism called lock stripping. This means that only certain portions (or “buckets”) of the map are locked during updates, allowing multiple threads to read and write to different parts of the map concurrently.  
* This results in higher performance in multi-threaded applications.

**Performance:**

* **Hashtable:**  
  * Because the entire object is locked for every operation, it leads to significant contention between threads, resulting in lower performance when many threads are trying to access or modify the map concurrently.  
* **ConcurrentHashMap:**  
  * Provides better performance in highly concurrent scenarios by allowing multiple threads to perform operations on the map without blocking each other, as it only locks certain portions of the map.

**Null Keys and Values:**

* **Hashtable:**  
  * Does not allow null keys or values. If you try to insert null as a key or value, it will throw a NullPointerException.  
* **ConcurrentHashMap:**  
  * Also does not allow null keys or values. Similar to Hashtable, it will throw a NullPointerException if you attempt to use null as a key or value.

**Locking Granularity:**

* **Hashtable:**  
  * Uses a single lock for the entire table. This leads to a high degree of contention when multiple threads attempt to access or modify it, as only one thread can hold the lock at a time.  
* **ConcurrentHashMap:**  
  * Uses multiple locks (via lock striping) to allow higher concurrency. By default, the map is divided into 16 segments (in older versions) or internally uses fine-grained locking (in newer versions), allowing multiple threads to operate on different segments concurrently, significantly improving throughput.

**Iteration:**

* **Hashtable:**  
  * The iteration over the Hashtable is not fail-safe. This means that if the map is modified during iteration (e.g., by another thread), it throws a ConcurrentModificationException.  
* **ConcurrentHashMap:**  
  * The iteration is fail-safe, meaning that it does not throw ConcurrentModificationException if the map is modified during iteration. It provides a weakly consistent iterator that reflects some (but not necessarily all) changes made to the map during iteration.

**Concurrent Reads:**

* **Hashtable:**  
  * Since every method is synchronized, even read operations are blocked if another thread is performing a write operation. This can lead to poor performance even when reads dominate writes.  
* **ConcurrentHashMap:**  
  * In ConcurrentHashMap, read operations are not locked. Multiple threads can read from the map concurrently without blocking each other, which leads to better performance in read-heavy environments.

**Use Cases:**

* **Hashtable**:  
  * Generally not recommended for new development due to its poor scalability in concurrent environments.  
  * Suitable only in cases where you have very low concurrency and need a simple, thread-safe map.  
* **ConcurrentHashMap:**  
  * Preferred in highly concurrent environments where multiple threads need to access and update a shared map.  
  * Ideal for use cases such as caching, where read and write operations are frequent and occur concurrently.

| Feature | Hashtable | ConcurrentHashMap |
| :---- | :---- | :---- |
| **Thread-Safety** | Yes, but uses global synchronization | Yes, but uses fine-grained locks |
| **Locking Mechanism** | Entire table is locked | Uses segment locks (lock striping) |
| **Performance** | Poor in concurrent scenarios | High performance in concurrent environments |
| **Null Keys/Values** | Does not allow null keys or values | Does not allow null keys or values |
| **Iteration** | Not fail-safe (throws ConcurrentModificationException) | Fail-safe (weakly consistent) |
| **Read Concurrency** | Blocked by write operations | Multiple threads can read concurrently |
| **Write Concurrency** | Entire table locked | Allows concurrent writes to different segments |
| **Use Case** | Suitable for low concurrency scenarios | Ideal for highly concurrent environments |

* Hashtable is an older, synchronized class that locks the entire map, leading to poor performance in multi-threaded environments. It is generally not recommended for modern applications.  
* ConcurrentHashMap is a modern, highly optimized thread-safe map that provides significantly better performance by using finer-grained locking, making it the preferred choice in concurrent applications.

# D/f b/w get() and load() method in Hibernate?Lazy and Eager loading in Hibernate?

Here’s a brief and concise comparison of the get() and load() methods in Hibernate, along with an explanation of Lazy and Eager loading:

**get() vs load() Method in Hibernate**

| Feature | get() Method | load() Method |
| :---- | :---- | :---- |
| Object Fetching | Immediately hits the database to fetch the object | Returns a proxy object; the database is hit only when data is accessed (Lazy Loading) |
| Return Type | Returns the actual entity or null if not found | Returns a proxy, throws an exception (ObjectNotFoundException) if the entity is not found |
| When to Use | Use when you need to ensure the object exists in the database | Use when you are sure the object exists, or you want to defer loading (lazy loading) |
| Performance | Slower, as it always hits the database immediately | More efficient when you just need a reference and may not access the full data |
| Null Handling | Returns null if the object is not found | Throws an excp. (ObjectNotFoundException) if the object is not found |
| Use Case | When you need to fetch the object immediately and work with its data | When you want to delay fetching until the object is actually needed (lazy loading) |

// get() example  
Student student \= session.get(Student.class, studentId); // Hits database immediately

// load() example  
Student student \= session.load(Student.class, studentId); // Returns proxy, lazy loads when accessed

**Lazy Loading vs Eager Loading in Hibernate**

**Lazy Loading:** 

* **Definition:** In lazy loading, the associated objects are not loaded from the database until they are explicitly accessed.  
* **Behavior**: The related data is fetched on demand. Hibernate uses proxies to implement lazy loading.  
* **Performance**: Can improve performance by loading data only when needed, but may lead to LazyInitializationException if accessed after session closure.

Example:

* One-to-many associations (e.g., loading a list of orders for a customer) are often lazy by default.

  @OneToMany(fetch \= FetchType.LAZY)

  private List\<Order\> orders;

**Eager Loading:**

* **Definition**: In eager loading, the associated objects are immediately loaded along with the main entity, meaning all related data is fetched in a single query.  
* **Behavior**: The entire object graph is loaded, even if some parts of the data are not needed immediately.  
* **Performance**: Can lead to performance issues if large object graphs are loaded unnecessarily.

Example:

* To load the associated entities eagerly:

  @OneToMany(fetch \= FetchType.EAGER)

  private List\<Order\> orders;

| Feature | Lazy Loading | Eager Loading |
| :---- | :---- | :---- |
| When Data is Loaded | Only when accessed (on demand) | Immediately when the main entity is loaded |
| Performance | More efficient if related data is not always needed | Can degrade performance due to unnecessary data loading |
| Default Behavior | Hibernate associations are lazy by default | Needs to be explicitly configured using FetchType.EAGER |
| Risk | Can cause LazyInitializationException if the session is closed before data is accessed | Loads unnecessary data, leading to possible memory and performance issues |

In Conclusion:

* Use get() when you want to immediately fetch an object from the database and be sure it exists.  
* Use load() when you want to delay loading and are fine working with a proxy.  
* Choose Lazy Loading when you want to improve performance by fetching data only when it’s actually needed, and Eager Loading when you know you’ll need the related data immediately.

# AutoClosable Interface.

The AutoCloseable interface in Java is used to automatically release resources when they are no longer needed. It is part of the java.lang package and introduced in Java 7 to support the try-with-resources feature. This interface provides a method to ensure that resources like streams, files, sockets, or database connections are closed properly after their usage, even in the event of an exception.

Key Points about AutoCloseable:

* **Method:**  
  * It contains one method: void close() throws Exception.  
  * This method is invoked automatically when the object goes out of scope (usually at the end of a try-with-resources block), ensuring that the resource is properly closed.  
* **try-with-resources:**  
  * The try-with-resources statement ensures that any resource that implements AutoCloseable is closed automatically after the try block is finished, reducing boilerplate code and the risk of resource leaks.  
  * Any class that implements AutoCloseable (or its subinterface Closeable) can be used inside a try-with-resources block.  
* **Usage**:	  
  * Commonly used with resources like I/O streams (InputStream, OutputStream), database connections (Connection), and files.

Difference Between AutoCloseable and Closeable:

* **AutoCloseable**: It is a more generic interface and its close() method can throw any exception.  
* **Closeable**: A subinterface of AutoCloseable that is specific to I/O resources. It only allows an IOException to be thrown.

  class MyResource implements AutoCloseable {


  	public void doSomething() {

      	System.out.println("Doing something with the resource");

  	}


  	@Override

  	public void close() throws Exception {

      	System.out.println("Resource is closed");

  	}

  }


  public class Main {

  	public static void main(String\[\] args) {

      	try (MyResource resource \= new MyResource()) {

          	resource.doSomething();

      	} catch (Exception e) {

          	e.printStackTrace();

      	}

  	}

  }

	**Output:**  
		Doing something with the resource  
Resource is closed

**How it works:** When the try block finishes (whether normally or due to an exception), the close() method of MyResource is automatically called, ensuring proper cleanup of the resource.

Conclusion:  
The AutoCloseable interface **simplifies resource management** in Java by ensuring that resources are automatically closed when they are no longer needed, improving code safety and reducing the risk of resource leaks.

# What is Microservice and its design pattern?

Microservices architecture is a modern software development approach where applications are composed of small, independent services that communicate through well-defined APIs. Each service is designed to handle a specific business function, allowing for greater flexibility, scalability, and ease of deployment compared to traditional monolithic architectures.

Key Concepts of Microservices

* **Independence**: Each microservice operates independently, allowing for separate development, deployment, and scaling.  
* **Decentralized Data Management**: Microservices typically manage their own data, often using a database per service pattern, which enhances data isolation and reduces coupling between services.  
* **Communication**: Services communicate over networks using lightweight protocols, commonly HTTP/REST or messaging queues.

**Design Patterns in Microservices with Java Spring Boot**

**Service Registry Pattern**

* **Purpose**: Facilitates service discovery by maintaining a registry of available services.  
* **Implementation**\*\*: Tools like Eureka or Consul can be used to register and discover services dynamically.  
  * Example: A service registers itself upon startup and deregisters when it shuts down.

**API Gateway Pattern**

* **Purpose**: Acts as a single entry point for clients, routing requests to appropriate microservices.  
* **Benefits**: Simplifies client interactions by consolidating multiple service endpoints into one.  
  * **Implementation**: Spring Cloud Gateway or Zuul can be utilized to create an API gateway in a Spring Boot application.

**Circuit Breaker Pattern**

* **Purpose**: Enhances system resilience by preventing cascading failures when a service becomes unavailable.  
* **Implementation**: Libraries like Hystrix can be integrated into Spring Boot applications to manage circuit breaking.  
  * Functionality: If a service fails repeatedly, the circuit breaker trips, allowing the system to recover before retrying.

**Event-Driven Architecture**

* **Purpose**: Promotes asynchronous communication between services through events.  
* **Benefits**: Reduces tight coupling and increases responsiveness.  
  * Implementation: Technologies like Apache Kafka can be used for event streaming in Spring Boot applications.

**Saga Pattern**

* **Purpose**: Manages distributed transactions across multiple services without requiring a centralized transaction manager.  
* **Implementation**: Each service executes its local transaction and publishes an event; if one fails, compensating transactions are invoked.  
  * Benefits: Ensures data consistency in a distributed environment.

**Database per Service Pattern**

* **Purpose**: Each microservice has its own database schema to ensure loose coupling.  
* **Benefits**: Allows for independent scaling and optimization of databases based on service needs.

**Bulkhead Pattern**

* **Purpose**: Isolates different parts of the system to prevent failures from propagating.  
* **Implementation**: Services are grouped into pools; if one pool fails, others remain operational.

**Command Query Responsibility Segregation (CQRS)**

* **Purpose**: Separates read and write operations for better performance and scalability.  
* **Implementation**: Different models are used for reading (query) and writing (command) data.

**Conclusion**  
Microservices architecture offers significant advantages in terms of scalability, flexibility, and resilience. By leveraging design patterns such as those supported by Java Spring Boot, developers can effectively address common challenges associated with building distributed systems. These patterns not only enhance the maintainability of microservices but also improve their performance and reliability in production environments.

# How to handle transactions in Spring Boot?

# What is the transaction propagation type?What is Mandatory

# “@Qualifier”, “@Required”, “@ConfigurationProperties” and “@Value” annotation?

Here is a detailed explanation of the Spring Boot annotations: @Qualifier, @Required, @RequiresNew, @ConfigurationProperties, and @Value.

**@Qualifier:**

* Purpose: @Qualifier is used to resolve ambiguity when you have multiple beans of the same type and need to specify which one to inject.

* Usage: Spring automatically injects dependencies by type, but when there are multiple beans of the same type, @Qualifier allows you to specify the exact bean to inject.

  @Service

  public class PaymentService {

  	@Autowired

  	@Qualifier("creditCardPayment")

  	private PaymentProcessor paymentProcessor;

  }


  @Component("creditCardPayment")

  public class CreditCardPaymentProcessor implements PaymentProcessor {

  	// Implementation

  }


  @Component("paypalPayment")

  public class PaypalPaymentProcessor implements PaymentProcessor {

  	// Implementation

  }

In this example, there are two beans of type PaymentProcessor, so @Qualifier("creditCardPayment") is used to specify which one to inject.

**@Required:**

* Purpose: @Required is used to mark a bean property as mandatory, meaning that it must be injected with a value at the time of bean creation. If the property is not injected, the application will fail at runtime.

* Usage:This annotation is used on setter methods to ensure that the required property is not null.

* Note: @Required has been deprecated as of Spring 5\. It is now recommended to use constructor injection or @Autowired on fields/setters along with validation mechanisms to enforce required dependencies.

  @Component

  public class EmployeeService {

  	private EmployeeRepository employeeRepository;


  	@Required

  	public void setEmployeeRepository(EmployeeRepository employeeRepository) {

      	this.employeeRepository \= employeeRepository;

  	}

  }

In this example, if employeeRepository is not injected, the application will fail.

**@ConfigurationProperties:**

* **Purpose**: @ConfigurationProperties is used to bind a group of properties defined in the application properties (application.properties or application.yml) file to a Java class.  
* **Usage**: It allows for structured and type-safe access to application configuration properties. Instead of using individual @Value annotations, you can bind a group of related properties to a configuration class.

  @ConfigurationProperties(prefix \= "app.datasource")

  @Component

  public class DataSourceConfig {

  	private String url;

  	private String username;

  	private String password;

      

  	// Getters and setters

  }


  application.properties:

  app.datasource.url=jdbc:mysql://localhost:3306/mydb

  app.datasource.username=root

  app.datasource.password=secret

In this example, the properties under app.datasource will be mapped to the DataSourceConfig class.

**Note:** To enable this feature, you need to add @EnableConfigurationProperties(DataSourceConfig.class) in your configuration class or use @SpringBootApplication.

**@Value:**

* **Purpose**: @Value is used to inject property values from external configuration files (application.properties, application.yml, or environment variables) directly into your Spring components.  
* **Usage**: It can be used to inject simple values (e.g., strings, numbers) or expressions into your beans.

  @Component

  public class AppConfig {


  	@Value("${app.name}")

  	private String appName;


  	@Value("${app.version}")

  	private String appVersion;


  	@Value("${app.debug:false}")

  	private boolean debugMode;


  	// Getters

  }


  application.properties:

  app.name=MySpringApp

  app.version=1.0.0

  app.debug=true

In this example, the values for appName, appVersion, and debugMode are injected from the application.properties file. You can also use expressions like ${ENV\_VAR:default\_value} to set default values.

* @Qualifier: Used to resolve ambiguity when multiple beans of the same type are present.  
* @Required: Marks a bean property as mandatory (deprecated in Spring 5).  
* @RequiresNew: Creates a new transaction, suspending the current one.  
* @ConfigurationProperties: Binds external configuration properties to a Java class.  
* @Value: Injects values from property files or environment variables into Spring beans.

# CORS mapping

CORS, or \*\*Cross-Origin Resource Sharing\*\*, is a security feature implemented by web browsers that allows or restricts resources requested from a domain outside the domain from which the first resource was served. In the context of a Spring Boot application, CORS is crucial for enabling web applications to interact with APIs hosted on different domains.

\#\# Why CORS is Important

Modern browsers enforce a \*\*same-origin policy\*\*, which restricts web applications from making requests to a different domain than the one that served the web page. CORS provides a way to relax this policy, allowing servers to specify who can access their resources and which HTTP methods are permitted.

\#\# Configuring CORS in Spring Boot

Spring Boot provides several ways to configure CORS:

\#\#\# 1\. Method-Level CORS Configuration  
You can enable CORS for specific controller methods using the \`@CrossOrigin\` annotation.

\*\*Example\*\*:  
\`\`\`java  
import org.springframework.web.bind.annotation.\*;

@RestController  
@RequestMapping("/api")  
public class SampleController {

	@CrossOrigin(origins \= "https://example.com")  
	@GetMapping("/data")  
	public String getData() {  
    	return "Data from server";  
	}  
}  
\`\`\`

\#\#\# 2\. Class-Level CORS Configuration  
You can also apply the \`@CrossOrigin\` annotation at the class level, which will apply to all methods within that controller.

\*\*Example\*\*:  
\`\`\`java  
@CrossOrigin(origins \= "https://example.com")  
@RestController  
@RequestMapping("/api")  
public class SampleController {

	@GetMapping("/data")  
	public String getData() {  
    	return "Data from server";  
	}

	@PostMapping("/data")  
	public String postData(@RequestBody String data) {  
    	return "Posted data: " \+ data;  
	}  
}  
\`\`\`

\#\#\# 3\. Global CORS Configuration  
For a more centralized approach, you can configure CORS globally by implementing the \`WebMvcConfigurer\` interface.

\*\*Example\*\*:  
\`\`\`java  
import org.springframework.context.annotation.Bean;  
import org.springframework.context.annotation.Configuration;  
import org.springframework.web.servlet.config.annotation.CorsRegistry;  
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;

@Configuration  
public class WebConfig implements WebMvcConfigurer {

	@Override  
	public void addCorsMappings(CorsRegistry registry) {  
    	registry.addMapping("/\*\*") // Apply to all endpoints  
            	.allowedOrigins("https://example.com") // Specify allowed origins  
            	.allowedMethods("GET", "POST", "PUT", "DELETE") // Specify allowed methods  
            	.allowedHeaders("\*"); // Allow all headers  
	}  
}  
\`\`\`

\#\#\# 4\. CORS with Spring Security  
When using Spring Security, it's essential to configure CORS properly to ensure that preflight requests (OPTIONS) are handled before authentication checks.

\*\*Example\*\*:  
\`\`\`java  
import org.springframework.context.annotation.Bean;  
import org.springframework.security.config.annotation.web.builders.HttpSecurity;  
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;  
import org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter;

@EnableWebSecurity  
public class SecurityConfig extends WebSecurityConfigurerAdapter {

	@Override  
	protected void configure(HttpSecurity http) throws Exception {  
    	http.cors() // Enable CORS support  
        	.and()  
        	.authorizeRequests()  
        	.anyRequest().authenticated(); // Require authentication for all requests  
	}  
}  
\`\`\`

\#\#\# 5\. Customizing CORS Configuration with CorsConfigurationSource  
You can create a custom \`CorsConfigurationSource\` bean to define more complex CORS configurations.

\*\*Example\*\*:  
\`\`\`java  
import org.springframework.context.annotation.Bean;  
import org.springframework.context.annotation.Configuration;  
import org.springframework.web.cors.CorsConfiguration;  
import org.springframework.web.cors.UrlBasedCorsConfigurationSource;  
import org.springframework.web.cors.CorsConfigurationSource;

@Configuration  
public class CorsConfig {

	@Bean  
	public CorsConfigurationSource corsConfigurationSource() {  
    	CorsConfiguration configuration \= new CorsConfiguration();  
    	configuration.setAllowedOrigins(List.of("https://example.com"));  
    	configuration.setAllowedMethods(List.of("GET", "POST", "PUT", "DELETE"));  
    	UrlBasedCorsConfigurationSource source \= new UrlBasedCorsConfigurationSource();  
    	source.registerCorsConfiguration("/\*\*", configuration);  
    	return source;  
	}  
}  
\`\`\`  
Conclusion  
CORS is an essential aspect of web security, allowing controlled access to resources across different origins. In Spring Boot applications, configuring CORS can be done at various levels—method, class, or globally—providing flexibility depending on the application's requirements. Properly handling CORS is especially important when integrating with Spring Security to ensure that preflight requests are managed appropriately.

# Fail fast and Fail safe.

# What are the fundamental concepts to keep in mind before creating a class?

Designing a class in Java involves careful consideration of its purpose, structure, and behavior. Here's a guide on how to design a class and the fundamental properties to keep in mind:  
Steps to Design a Class:

* **Identify the Purpose:**  
   Clearly define the purpose of the class. What real-world entity or concept does it represent? What functionalities should it encapsulate?  
* **Naming:**  
   Choose a meaningful and descriptive name for the class that reflects its purpose. Follow Java naming conventions:  
  * Use PascalCase (capitalize the first letter of each word).  
  * Use nouns for class names.  
* **Define Attributes (Instance Variables):**  
   Determine the data members (variables) that the class needs to hold its state. Consider:  
  * Data types: Choose appropriate data types for each attribute.  
  * Access modifiers: Use `private` to encapsulate data and provide controlled access through methods.  
* **Define Constructors:**  
   Create constructors to initialize the object's state when it is created.  
  * Provide a default constructor if necessary.  
  * Consider overloading constructors for different initialization scenarios.  
* **Define Methods (Behaviors):**  
   Determine the actions or operations that the class can perform.  
  * Use verbs for method names.  
  * Consider access modifiers (e.g., `public`, `private`, `protected`) to control access to the methods.  
  * Follow the Single Responsibility Principle (SRP) for each method.  
* **Implement Relationships:**  
   If the class interacts with other classes, consider:  
  * Inheritance: Use `extends` to inherit properties and behaviors from a parent class.  
  * Interfaces: Use `implements` to define contracts that the class must adhere to.  
* **Encapsulation:**  
   Ensure that the class's internal implementation details are hidden from external code. This is achieved through:  
  * Using `private` access modifiers for attributes.  
  * Providing public accessor methods (`getters`) and mutator methods (`setters`) to control access to attributes.

Fundamental Properties to Keep in Mind:

* **Cohesion:** A class should have a single, well-defined purpose. It should group together closely related data and functionality.  
* **Coupling:** Minimize the dependencies between classes. Loosely coupled classes are easier to maintain and modify.  
* **Encapsulation:** Hide the internal details of a class to protect its integrity and make it easier to change.  
* **Abstraction:** Represent essential features of a class without exposing unnecessary complexity.  
* **Single Responsibility Principle (SRP):** A class should have only one reason to change.  
* **Open-Closed Principle (OCP):** Classes should be open for extension but closed for modification.

# Callable and Future and CompletableFuture.

In Java, `Callable` and `Future` are interfaces used for asynchronous programming. Here's a breakdown of their roles and how they relate to `CompletableFuture`:  
**Callable**:

* Represents a task that returns a result.  
* Similar to `Runnable`, but `Callable`'s `call()` method can return a value and throw an exception.

  import java.util.concurrent.Callable;


  public class MyCallable implements Callable\<Integer\> {

     @Override

     public Integer call() throws Exception {

         // Perform some computation

         return 42;

     }

  }

**Future**:

* Represents the result of an asynchronous computation.  
* Provides methods to check if the computation is complete, retrieve the result, and cancel the task.

  import java.util.concurrent.ExecutorService;

  import java.util.concurrent.Executors;

  import java.util.concurrent.Future;


  public class FutureExample {

     public static void main(String\[\] args) throws Exception {

         ExecutorService executor \= Executors.newSingleThreadExecutor();

         Callable\<Integer\> callable \= new MyCallable();


         Future\<Integer\> future \= executor.submit(callable);


         // Do other work while the task is running


         // Get the result (blocks if not yet available)

         int result \= future.get();

         System.out.println("Result: " \+ result);


         executor.shutdown();

     }

  }

CompletableFuture:

* A more advanced implementation of the `Future` interface, introduced in Java 8\.  
* Provides a rich set of methods for chaining asynchronous operations, handling errors, and composing futures.  
  Java  
  import java.util.concurrent.CompletableFuture;  
    
  public class CompletableFutureExample {  
     public static void main(String\[\] args) {  
         CompletableFuture\<Integer\> future \= CompletableFuture.supplyAsync(() \-\> {  
             // Perform some computation  
             return 42;  
         });  
    
         future.thenApply(result \-\> result \* 2\)  
               .thenAccept(finalResult \-\> System.out.println("Final Result: " \+ finalResult));  
     }  
  }

Key Differences:

* **Blocking vs. Non-Blocking:**  
   `Future.get()` blocks the current thread until the result is available. `CompletableFuture` provides non-blocking methods like `thenApply`, `thenAccept`, and `thenCompose` to chain operations without blocking.  
* **Composition:**  
   `CompletableFuture` allows you to compose multiple asynchronous operations easily using methods like `thenCompose`, `thenCombine`, and `allOf`.  
* **Error Handling:**  
   `CompletableFuture` provides methods like `exceptionally` and `handle` to handle exceptions in asynchronous operations.   
* 

Which one to use?

* For simple asynchronous tasks, `Callable` and `Future` can suffice.  
* For more complex scenarios where you need to chain operations or handle errors in a non-blocking manner, `CompletableFuture` is the recommended choice.

# 