# Java Interview Questions

### Good morning, and thank you for extending this opportunity to me. I'm Devaj Singh, currently working as a software developer at Lumina Datamatics. Over the past four years, I've developed a strong set of skills including both front-end and back-end technologies such as Java, JavaScript, TypeScript, HTML, and CSS. My recent project involvement centered around the Angular Framework for the front end and Spring Boot for the back-end, notably contributing to an publishing project where I led the development of custom plugins and integrating to the angular application and creating rest apis and unit tests with spring boot framework. This experience made me really excited about creating solutions that make a real difference. As your company seeks individuals for a similar role, I am confident that my background aligns well with your requirements.

### As the journey of learning never stops , I am actively honing my skills in system design to strengthen my abilities further. I believe that by improving my proficiency in this area, I can not only contribute effectively to your team but also drive innovation and efficiency within the organization. Thank you for considering my candidacy.

## Explain Java programming language. What are its special features?

Java is a high-level, general-purpose object oriented programming language that was developed by Sun Microsystems in 1995 and is now maintained by Oracle Corporation. It was designed with the primary goal of being platform-independent, meaning that Java programs can run on any device or operating system that has a Java Virtual Machine (JVM) installed.

Key features of Java include:

1. **Platform independence**: Java programs are compiled into bytecode, which is then executed by the JVM. This bytecode can run on any device or operating system that has a compatible JVM, making Java highly portable.  
2. **Object-oriented**\*\*: Java is fully object-oriented, meaning it supports concepts such as encapsulation, inheritance, and polymorphism. This makes it easier to write and maintain complex software systems.  
3. **Simple**\*\*: Java was designed to be simple and easy to learn. It has a clean syntax that is similar to C and C++, making it familiar to many programmers.  
4. **Robustness**\*\*: Java is designed to be robust and reliable. It includes features such as automatic memory management (garbage collection) and exception handling, which help prevent errors and make programs more stable.  
5. **Security**\*\*: Java includes built-in security features that help protect against malicious code. For example, the Java sandbox restricts what applets running in a web browser can do, preventing them from accessing certain system resources.  
6. **Multi-threading**\*\*: Java has built-in support for multi-threading, allowing programs to perform multiple tasks concurrently. This can improve performance and responsiveness in applications that need to handle multiple tasks simultaneously.  
7. **High performance**\*\*: While Java programs are typically slower than natively compiled languages like C or C++, the performance of Java has improved significantly over the years. Just-In-Time (JIT) compilation and other optimizations help make Java programs run faster.  
8. **Rich standard library**\*\*: Java comes with a large standard library that provides classes and methods for common tasks such as I/O, networking, and GUI development. This reduces the need for developers to write code from scratch and helps improve productivity.  
9. **Automatic memory management**\*\*: Java manages memory automatically through garbage collection. This means that developers don't need to explicitly allocate and deallocate memory, reducing the risk of memory leaks and making programming easier.  
10. **Community support**\*\*: Java has a large and active community of developers who contribute libraries, frameworks, and tools to the ecosystem. This wealth of resources makes it easier for developers to find solutions to common problems and accelerate development.

Overall, Java's combination of platform independence, object-oriented design, simplicity, robustness, security, and performance has made it one of the most popular programming languages in the world, widely used in enterprise software development, web development, mobile app development (Android), and many other domains.

## How is Java platform independent?

Yes, Java is platform-independent. This means that Java programs can run on any device or platform that has a Java Virtual Machine (JVM) installed. Java achieves platform independence through its bytecode compilation model. Java source code is compiled into bytecode, which is then executed by the JVM. Since the JVM is available on various platforms (Windows, Linux, macOS, etc.), Java programs can run without modification on different systems, making it a "write once, run anywhere" language.

## What is javac?

The Java compiler is a program that translates Java source code into bytecode, which is a platform-independent representation of the program. It checks the syntax and semantics of the code, ensuring it adheres to the rules of the Java language. The bytecode generated by the compiler can be executed by the Java Virtual Machine (JVM) on any platform, making Java a "write once, run anywhere" language. The primary Java compiler is called \`javac\`, which is included in the Java Development Kit (JDK).

## What is JVM?

The Java Virtual Machine (JVM) is an abstract computing machine that enables Java bytecode to be executed on any platform. It is a crucial component of the Java Runtime Environment (JRE) and the Java Development Kit (JDK). The JVM interprets the bytecode and translates it into machine code that can be understood and executed by the underlying hardware. It provides various services such as memory management, garbage collection, and runtime environment for Java applications. The JVM ensures platform independence by providing a consistent execution environment for Java programs across different operating systems and architectures.

## What are the memory areas of JVM?

In the Java Virtual Machine (JVM), memory is divided into several areas, each serving a specific purpose in managing Java application execution. The main memory areas in the JVM include:

* **Heap**: The heap is the runtime data area where objects are allocated. It is divided into two parts: the young generation and the old generation. The young generation further consists of Eden space and two survivor spaces (from space and to space). Objects are initially allocated in the Eden space, and during garbage collection, surviving objects are moved to the survivor spaces. Eventually, objects that have survived multiple garbage collection cycles are promoted to the old generation.  
* **Stack**: Each thread in a Java application has its own stack, which stores method invocations and local variables. It's a last-in, first-out (LIFO) data structure where method calls and local variables are pushed onto the stack when a method is invoked and popped off when the method completes.  
* **Method Area (PermGen or Metaspace)**\*\*: This area stores class metadata, method information, static variables, and constant pool. In older versions of Java, it was called the Permanent Generation (PermGen), but in Java 8 and later, it's replaced by Metaspace, which dynamically adjusts its size based on application requirements.  
* **Program Counter (PC) Register\***\*: Each thread in the JVM has its own program counter register, which holds the address of the currently executing JVM instruction. It keeps track of the next instruction to be executed.  
* **Native Method Stack**\*\*: This area is reserved for native methods (methods implemented in languages other than Java), providing a stack for their execution.

These memory areas work together to manage Java program execution efficiently, handling object allocation, method execution, and other runtime operations.

## What is a JIT compiler?

The Just-In-Time (JIT) compiler is a component of the Java Virtual Machine (JVM) that dynamically compiles bytecode into native machine code at runtime. When a Java program is executed, the bytecode is initially interpreted by the JVM. However, as the program runs, the JIT compiler identifies frequently executed portions of code (hotspots) and compiles them into optimized native machine code. This native code execution is typically much faster than interpreting bytecode.

The JIT compiler employs various optimization techniques, such as inlining, loop unrolling, and dead code elimination, to generate efficient machine code tailored to the specific execution environment. By selectively compiling only the most performance-critical parts of the code, the JIT compiler strikes a balance between the flexibility of bytecode interpretation and the speed of native code execution.

Overall, the JIT compiler enhances the performance of Java applications by dynamically optimizing code during runtime, leading to improved execution speed and reduced startup time.

## What is the difference between JDK and JRE?

The JDK (Java Development Kit) is a software development kit that includes tools for developing, debugging, and monitoring Java applications. It contains the JRE (Java Runtime Environment) along with development tools such as compilers and debuggers.

The JRE (Java Runtime Environment) is a runtime environment required to run Java applications. It includes the JVM (Java Virtual Machine), class libraries, and other runtime components necessary for executing Java bytecode.

In essence, the JDK is for Java development, providing everything needed to create Java applications, while the JRE is for executing Java applications, providing only the runtime environment without development tools.

## Difference between C, C++ and Java?

**C**:

* Procedural programming language.  
* Low-level language with minimal abstraction from hardware.  
* Offers direct memory manipulation.  
* No built-in support for object-oriented programming (OOP) concepts.  
* Requires manual memory management (allocating and deallocating memory).  
* Widely used for system programming, embedded systems, and performance-critical applications.

**C++:**

* Multi-paradigm programming language (supports procedural, object-oriented, and generic programming).  
* Superset of C, meaning it includes all features of C and adds additional features.  
* Supports classes, inheritance, polymorphism, and encapsulation (OOP concepts).  
* Provides features like templates for generic programming and exception handling.  
* Offers more abstraction and type safety compared to C.  
* Requires manual memory management but also supports automatic memory management through smart pointers.  
* Used in applications ranging from system software to games and graphical user interfaces.

**Java:**

* Object-oriented programming language.  
* Platform-independent, runs on a virtual machine (JVM).  
* Uses automatic memory management through garbage collection, relieving developers from manual memory management concerns.  
* Strongly influenced by C++ but with simpler syntax and no support for certain C++ features like pointers and operator overloading.  
* Provides extensive standard libraries for various tasks, including networking, database access, and graphical user interfaces.  
* Includes features like multithreading and exception handling.  
* Widely used for enterprise applications, web development, mobile applications (Android), and large-scale systems.

In summary, C is a procedural language with minimal abstraction, C++ extends C with support for OOP and other paradigms, while Java is an object-oriented language with platform independence and automatic memory management. Each language has its strengths and is suitable for different types of applications and development scenarios.

## Data types in Java

In Java, data types can be categorized into primitive and non-primitive types.  
**Primitive Data Types\*\***:

* byte\*\*: 8-bit integer.  
* short\*\*: 16-bit integer.  
* int\*\*: 32-bit integer.  
* long\*\*: 64-bit integer.  
* float\*\*: 32-bit floating-point number.  
* double\*\*: 64-bit floating-point number.  
* char\*\*: 16-bit Unicode character.  
* boolean\*\*: Represents true or false.

**Non-Primitive Data Types\*\* (also known as reference types)**:

* Arrays\*\*: Collections of elements of the same type.  
* Classes\*\*: User-defined data types.  
* Interfaces\*\*: Defines a set of methods that a class must implement.  
* Strings\*\*: Sequence of characters. Although String is used like a primitive type, it's actually a class in Java.  
* Wrapper Classes\*\*: Classes that encapsulate primitive types (e.g., Integer, Double) to provide utility methods.

These data types serve various purposes in Java programming, enabling developers to work with different kinds of data efficiently and effectively.

## Volatile keyword

In Java, the \`volatile\` keyword is used to indicate that a variable's value may be modified by multiple threads that are executing concurrently. When a variable is declared as \`volatile\`, it ensures that any thread reading the variable always sees the most recent value written to it by any other thread.

The \`volatile\` keyword provides two main guarantees:

* **Visibility**: Changes made to a \`volatile\` variable are immediately visible to other threads. This means that when one thread writes to a \`volatile\` variable, all other threads are guaranteed to see the updated value when they read the variable.  
* **Ordering**: The \`volatile\` keyword also ensures that accesses to the variable are not reordered by the compiler or the processor. In other words, if one thread writes to a \`volatile\` variable and then writes to a non-volatile variable, those writes cannot be reordered such that the non-volatile write happens before the \`volatile\` write in another thread.


However, it's important to note that \`volatile\` does not provide atomicity or synchronization. It only guarantees visibility and ordering. If multiple threads are performing compound actions that involve more than one variable, \`volatile\` alone may not be sufficient to ensure thread safety, and additional synchronization mechanisms such as locks or atomic classes should be used.  
\`\`\`  
public class SharedData {  
	private volatile int counter \= 0;

	public void increment() {  
    		counter++; // This operation is not atomic  
	}

	public int getCounter() {  
    		return counter;  
	}  
}  
\`\`\`  
In this example, \`counter\` is declared as \`volatile\` to ensure that changes made by one thread are immediately visible to other threads. However, because \`counter++\` is not an atomic operation (it involves reading the current value of \`counter\`, incrementing it, and then writing the new value back to \`counter\`), multiple threads accessing \`increment()\` concurrently could result in lost updates or incorrect values. To ensure atomicity, additional synchronization mechanisms such as \`synchronized\` blocks or the use of \`java.util.concurrent.atomic\` classes should be employed.

## Difference between path and classpath

**Path:**

* Used by the operating system to find executable programs.  
* Essential for running Java tools like \`javac\` and \`java\`.

**Classpath:**

* Used by the JVM and Java compiler to find \`.class\` files and libraries.  
* Essential for running Java applications that depend on external classes and libraries.

## What are keywords?

Keywords in Java are reserved words that have a predefined meaning and cannot be used as identifiers (variable names, method names, etc.). Here's a concise list of Java keywords:

\- Access modifiers: public, private, protected  
\- Primitive data types: byte, short, int, long, float, double, boolean, char  
\- Non-primitive types: void, class, interface, enum  
\- Flow control: if, else, switch, case, default, for, while, do, break, continue, return  
\- Exception handling: try, catch, finally, throw, throws  
\- Object-oriented programming: new, super, this, instanceof, abstract, extends, implements  
\- Modifiers: final, static, strictfp, synchronized, transient, volatile  
\- Others: package, import, null, true, false, assert, native, const (reserved but not used)

Some keywords like goto and const are reserved but not used in Java. It's important to avoid using these keywords as identifiers to prevent compilation errors.

## What are variables? What are its different types?

A variable in Java is a named storage location used to store data temporarily during program execution. There are different types of variables in Java:

1. Local Variables: Local variables are declared within a method, constructor, or block and are accessible only within that scope.  
2. Instance Variables (Non-Static Variables): Instance variables are declared within a class but outside any method, constructor, or block. Each instance of the class has its own copy of these variables.  
3. Static Variables (Class Variables): Static variables are declared with the \`static\` keyword within a class but outside any method, constructor, or block. They are shared among all instances of the class.  
4. Parameters (Method Arguments): Parameters are variables that are passed into methods and constructors to provide data for their execution. They are defined within the method or constructor signature.

These are the main types of variables in Java, each serving a different purpose and scope within a program.

## What is OOP Language?

Object-oriented programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data in the form of fields (often known as attributes or properties) and code in the form of procedures (often known as methods). OOP aims to structure software in a way that models real-world entities or abstract concepts.

Key principles of object-oriented programming include:

1. **Encapsulation:** Encapsulation refers to the bundling of data and methods that operate on the data into a single unit, called a class. This helps in hiding the internal state of an object and only exposing the necessary operations to interact with it.  
2. **Inheritance:** Inheritance allows a class (subclass or derived class) to inherit properties and behavior (methods) from another class (superclass or base class). This promotes code reuse and allows for creating a hierarchy of classes with shared characteristics.  
3. **Polymorphism**: Polymorphism allows objects of different classes to be treated as objects of a common superclass. This enables code to be written that can work with objects of multiple types, providing flexibility and extensibility. Ability of an object to take on multiple forms.  
4. **Abstraction**: Abstraction involves simplifying complex systems by modeling only the essential aspects and ignoring irrelevant details. In OOP, abstraction is achieved through abstract classes and interfaces, which define a common interface for a group of related classes.

By leveraging these principles, OOP promotes modularity, reusability, and maintainability of code. It allows developers to break down complex problems into smaller, more manageable components, leading to more organized and scalable software systems. OOP is widely used in various programming languages, including Java, C++, Python, and many others.

## The execution flow of a Java program

The execution flow of a Java program involves several key steps, which can be summarized as follows:

1. **Creation of a Java Program**: A Java program is written in a text file with a \`.java\` extension.  
2. **Compilation:** The Java source code is compiled using the Java compiler (\`javac\`), which converts it into bytecode. This bytecode is stored in \`.class\` files and is platform-independent, allowing it to run on any system with a Java Virtual Machine (JVM).  
3. **Class Loading:** The JVM loads the compiled bytecode into memory. This process involves the Class Loader, which locates and loads the necessary class files.  
4. **Bytecode Verification:** The bytecode verifier checks the loaded bytecode for security and correctness, ensuring that it adheres to Java's safety rules (e.g., proper variable initialization and method calls).  
5. **Execution:** The JVM executes the bytecode. This may involve interpreting the bytecode or using Just-In-Time (JIT) compilation to convert it into native machine code for improved performance.  
6. **Runtime Services:** During execution, the JVM provides various runtime services, including memory management, garbage collection, and exception handling \[1\].

This flow ensures that Java programs can run securely and efficiently across different platforms.  
How to set class path,   
character set,   
data type, 

## What is JVM, JRE, JDK ?

**JVM (Java Virtual Machine)**: JVM is an abstract computing machine that enables Java bytecode to be executed on different hardware platforms. It provides a runtime environment for Java programs, including memory management, garbage collection, and execution of bytecode instructions.

**JRE (Java Runtime Environment):**JRE is a software package that includes the JVM along with libraries and other components required to run Java applications. It does not contain development tools such as compilers or debuggers.

**JDK (Java Development Kit):** JDK is a software development kit that includes the JRE, development tools (such as javac compiler, debugger, and other utilities), and libraries necessary for developing Java applications. It provides everything needed to develop, compile, and run Java programs.

## Define System.out.println().

In Java, \`System.out.println()\` is a method used to print a line of text to the standard output stream. Here's a breakdown of its components:

* **System**: \`System\` is a pre-defined class in the Java standard library located in the \`java.lang\` package. It provides access to various system-related properties and methods.  
* **out**: \`out\` is a static field within the \`System\` class. It represents the standard output stream, which is typically connected to the console where text output is displayed.  
* **println**(): \`println()\` is a method of the \`PrintStream\` class, which is the type of the \`out\` field. This method is used to print a string followed by a newline character (\`\\n\`). It automatically flushes the stream after printing, ensuring that the output appears immediately.

Combining these elements, \`System.out.println()\` allows you to print text to the console followed by a newline character, making it suitable for displaying messages, debugging information, or any other text-based output in Java programs.

## What is the difference Between Abstract Class and Interface, When to use What?

An abstract class in Java can have both abstract and non-abstract methods, while an interface can only have abstract methods (from Java 8, interfaces can also have default and static methods with implementations).

**Abstract Class:**

* Use when you want to provide a common base implementation for derived classes.  
* Use when you need to define fields, constructors, or non-public methods.  
* Use when you want to enforce a "is-a" relationship between classes.

**Interface:**

* Use when you want to define a contract that multiple unrelated classes can implement.  
* Use when you want to achieve multiple inheritance, as a class can implement multiple interfaces.  
* Use when you want to provide a common way to access related classes, promoting loose coupling.

In summary, use abstract classes when you want to provide a base implementation or enforce a "is-a" relationship, and use interfaces when you want to define a contract for multiple unrelated classes or achieve multiple inheritance. Often, you may use a combination of both to achieve your design goals.

## Final keyword in Java.

The **final** keyword in Java serves several important purposes and can be applied to variables, methods, and classes. Here’s a detailed overview:

**Final Variables**

* Definition: A variable declared as final can be assigned only once. Once assigned, its value cannot be changed.  
* Usage: A final variable must be initialized at the time of declaration or in the constructor if it is a blank final variable (i.e., it does not have an initial value).

	\`\`\`java  
	final int age \= 30; // Cannot change age later  
	\`\`\`

**Final Methods**

* Definition: A method declared as final cannot be overridden by subclasses.  
* Usage: This is useful when you want to prevent changing the behavior of a method in derived classes.

	\`\`\`java  
	class Base {  
    	public final void display() {  
        	System.out.println("Final method");  
    	}  
	}  
      
	class Derived extends Base {  
    	// This will cause a compile-time error  
    	public void display() {  
        	System.out.println("Attempting to override");  
    	}  
	}  
	\`\`\`

**Final Classes**

* Definition: A class declared as final cannot be subclassed.  
* Usage: This is often used for security reasons or to maintain the integrity of the class's implementation.  
  	\`\`\`java  
  	final class Utility {  
      	// Class methods here  
  	}  
        
  	class ExtendedUtility extends Utility { // This will cause a compile-time error  
      	// Cannot extend a final class  
  	}  
  	\`\`\`

**Blank Final Variables**

* These are final variables that are declared without an initializer. They must be initialized in the constructor.  
  	\`\`\`java  
  	class Example {  
      		final int value; // Blank final variable  
     	 

      	Example(int v) {  
          	this.value \= v; // Initialized in constructor  
      	}

  	}  
  	\`\`\`

**Implications of Using Final**

* Using final can enhance performance by allowing certain optimizations by the Java compiler.  
* It also promotes immutability, making code easier to understand and maintain.

In summary, the final keyword is crucial for defining constants, preventing method overriding, and restricting inheritance in Java, thereby enhancing code safety and reliability.

## Explain the Life Cycle of Thread.

The lifecycle of a thread in Java consists of several states:

* **New**: A thread is in this state before it is started via the \`start()\` method.  
* **Runnable**: After calling \`start()\`, the thread enters the runnable state, where it is ready to run but may not be currently executing due to CPU scheduling.  
* **Running**: The thread enters the running state when the scheduler selects it to execute. In this state, the thread is actively executing its code.  
* **Blocked** **(Waiting/Waiting for Monitor)**: A thread can enter a blocked state while waiting for a resource (e.g., I/O operation, synchronization lock). It transitions back to the runnable state when the resource becomes available.  
* **Timed** **Waiting**: A thread enters this state when it calls a method like \`sleep()\` or \`wait()\` with a specified timeout. It waits for the specified duration before transitioning back to the runnable state.  
* **Terminated** (**Dead**): A thread completes its execution and enters this state. It can happen when the \`run()\` method exits normally or when an uncaught exception terminates the thread.

These states represent the lifecycle of a thread in Java, from creation to termination, and the transitions between different states depending on the thread's activities and system events.

## Can we override the static method?

No, we cannot override static methods in Java.

Static methods belong to the class itself, not to any particular object instance, so they cannot be overridden in the same way as instance methods. However, they can be hidden by declaring a method with the same signature in a subclass, but this is called method hiding, not method overriding. The method to be invoked is determined at compile time based on the reference type, not at runtime like with method overriding.

## Can we make constructors Private What will happen if we make it?

Yes, we can make constructors private in Java. If a constructor is private:

* Objects of the class cannot be created directly from outside the class.  
* The class can control the creation of its instances and restrict instantiation to certain conditions or methods within the class.  
* Typically, private constructors are used in classes that contain only static utility methods or constants and are not intended to be instantiated.

In summary, making a constructor private in Java restricts the instantiation of objects of that class to within the class itself, providing control over object creation.

## What are Composition and Aggregation? State the difference.

Composition and Aggregation are two types of associations that define relationships between classes in Java:

**Composition:**

* Represents a strong "has-a" relationship.  
* The child object cannot exist independently of the parent object.  
* Example: A \`Car\` has an \`Engine\`. If the \`Car\` is destroyed, the \`Engine\` is also destroyed.

**Aggregation:**

* Represents a weak "has-a" relationship.  
* The child object can exist independently of the parent object.  
* Example: A \`Library\` has \`Books\`. If the \`Library\` is closed, the \`Books\` still exist.

In summary, use composition when the child object's lifecycle is tied to the parent, and use aggregation when the child object can exist independently of the parent.

## Although inheritance is a popular OOPs concept, it is less advantageous than composition. Explain

In object-oriented programming (OOP), both inheritance and composition are important concepts, but they serve different purposes and have distinct advantages. While inheritance is a popular mechanism for code reuse and defining relationships between classes, composition offers more flexibility and is often considered more advantageous in certain scenarios. Here's why:

Advantages of Composition over Inheritance:

**Flexibility and Loose Coupling:**

* Composition allows you to create complex objects by combining simpler ones. This approach promotes loose coupling between classes, as it emphasizes the "has-a" relationship rather than the "is-a" relationship seen in inheritance.  
* With composition, you can change the behavior of a class at runtime by changing the components it contains, without altering its structure or implementation. This flexibility makes the code easier to maintain and extend.

**Multiple Inheritance:**

* While inheritance in Java supports single inheritance (a class can extend only one superclass), composition allows for multiple inheritance by allowing a class to contain instances of multiple other classes.

**Encapsulation:**

* Composition promotes encapsulation, as it allows you to hide the internal details of how objects are composed. Clients interact with the composed object through its public interface, without needing to know about its internal structure or the classes of its components.  
* This encapsulation reduces the impact of changes to the internal implementation, making the code more robust and easier to refactor.

**Code Reusability:**

* Composition enables greater code reuse compared to inheritance in many cases. Instead of inheriting behavior from a superclass, you can reuse existing classes as components within other classes, leading to more modular and reusable code.

**Avoidance of Fragile Base Class Problem:**

* Inheritance can lead to the fragile base class problem, where changes to a superclass can inadvertently affect its subclasses, potentially introducing bugs or unintended behavior.  
* Composition helps avoid this problem by decoupling classes and reducing the dependencies between them. Changes to one class are less likely to impact other classes that use composition.

**When to Use Composition:**

* Use composition when you want to create flexible, reusable, and loosely coupled code.  
* Use composition to model "has-a" relationships between objects, where one object contains another as a component.  
* Use composition to avoid the limitations and potential drawbacks of inheritance, such as tight coupling, the fragile base class problem, and the inability to support multiple inheritance.

In summary, while inheritance is a powerful mechanism for sharing behavior and defining class hierarchies, composition offers greater flexibility, encapsulation, and code reuse, making it often more advantageous, especially in complex or evolving software systems.

## How is the creation of a String using new() different from that of a literal?

In Java, the creation of a \`String\` using the \`new\` keyword is different from creating a \`String\` using a literal in terms of memory allocation and string pooling.

**String Creation Using \`new\` Keyword:**

* **Syntax:** \`String str \= new String("example");\`  
* **Memory Allocation:** When you use \`new\`, a new \`String\` object is created in the heap memory, regardless of whether an equivalent string already exists in the string pool.  
* **String Pool:** The \`new\` keyword does not check the string pool. Even if an identical string literal exists in the pool, a new instance is created in the heap.

**String Creation Using Literals:**

* **Syntax:** \`String str \= "example";\`  
* **Memory Allocation:** When a string literal is used, the JVM checks the string pool first. If the string already exists in the pool, a reference to the pooled instance is returned. If it does not exist, the string is added to the pool.  
* **String Pool:** String literals are managed in a special memory area called the string pool, which helps in saving memory by reusing immutable string instances.

  \`\`\`

  public class StringExample {

  	public static void main(String\[\] args) {

      	// Using string literal

      	String str1 \= "example";

      	String str2 \= "example";


      	// Using new keyword

      	String str3 \= new String("example");


      	// Check references

      	System.out.println(str1 \== str2); 

  // true, both reference the same object in the string pool

      	System.out.println(str1 \== str3); 

  // false, str3 is a new object in the heap

  	}

  }

  \`\`\`

## StringBuilder() and StringBuffer().

* **Mutability:** Both \`StringBuilder\` and \`StringBuffer\` are mutable, meaning their values can be changed after they are created.  
* **Synchronization:**  
  * **StringBuffer**: Thread-safe and synchronized. Methods in \`StringBuffer\` are synchronized, which means they are safe to use in a multi-threaded environment. This also makes \`StringBuffer\` slower than \`StringBuilder\` due to the overhead of synchronization.  
  * **StringBuilder**: Not thread-safe and not synchronized. It is faster than \`StringBuffer\` because it does not incur the cost of synchronization. Use \`StringBuilder\` when thread safety is not a concern.

* **Performance:**	  
  * **StringBuffer**: Slower due to synchronization.  
  * **StringBuilder**: Faster due to lack of synchronization.

* **Usage:**  
  * **StringBuffer**: Use when working in a multi-threaded environment where thread safety is required.  
  * **StringBuilder**: Use in a single-threaded environment or when thread safety is not a concern for better performance.  
    \`\`\`java  
    public class Main {  
    	public static void main(String\[\] args) {  
        	// StringBuilder example  
        	StringBuilder sb \= new StringBuilder("Hello");  
        	sb.append(" World");  
        	System.out.println(sb.toString()); // Output: Hello World  
      
        	// StringBuffer example  
        	StringBuffer sbf \= new StringBuffer("Hello");  
        	sbf.append(" World");  
        	System.out.println(sbf.toString()); // Output: Hello World  
    	}  
    }  
    \`\`\`

**Summary:**

* **StringBuffer**: Synchronized, thread-safe, slower.  
* **StringBuilder**: Non-synchronized, not thread-safe, faster.

Choose \`StringBuffer\` for multi-threaded contexts requiring thread safety and \`StringBuilder\` for single-threaded or performance-critical applications where synchronization is unnecessary.

## Why is it said that the length() method of String class doesn't return accurate results?

The \`length()\` method of the \`String\` class in Java returns the number of \`char\` values in the string, not necessarily the number of visible characters. This can lead to seemingly inaccurate results in cases such as:

* **Unicode Characters**: Some Unicode characters are represented by surrogate pairs (two \`char\` values), so \`length()\` counts each \`char\` separately.  
* **Combining Characters**: Characters with diacritics (e.g., accents) may be composed of a base character and one or more combining characters, leading to a higher \`length()\` value than the number of visible characters.

Therefore, \`length()\` may not accurately reflect the number of visible or user-perceived characters in a string.

## What is the difference between Array and Collection in java?

Array and Collection are equivalent in terms of storing object references and manipulating data, but they differ in a number of ways. The following are the primary distinctions between an array and a Collection:

| Array | Collection |
| ----- | ----- |
| Arrays have a set size, which means that once we build one, we can't change it to meet our needs. | Collections are naturally grow-able and can be customized to meet our needs. We can change its size as per our requirement. |
| When it comes to performance, Arrays are the preferred to Collection. | Considering performance, Collections are not preferred to Arrays. |
| Only homogeneous data type elements can be stored in arrays. | Both homogeneous and heterogeneous components can be stored in a collection. |
| Because arrays have no underlying data structure, there is no ready-made method support. | Any collection class is built on a standard data structure, and so there is ready-made method support for every demand as a performance. These methods can be used directly, and we are not responsible for their implementation. |
| Objects and primitives can both be stored in arrays. | Only object types can be stored in a collection. |
| When it comes to memory, Arrays are not preferred to Collection. | Considering memory, Collections are preferred to Arrays. |

## Differentiate between Iterator and ListIterator in Java.

In Java's Collection framework, iterators are used to obtain elements one by one. It can be used on any type of Collection object. We can execute both read and remove operations using Iterator. Iterator must be used whenever we want to iterate elements in all Collection framework implemented interfaces, such as Set, List, Queue, and Deque, as well as all Map interface implemented classes. The only cursor accessible for the entire collection framework is the iterator.

ListIterator is only useful for classes that implement List collections, such as array lists and linked lists. It can iterate in both directions. When we wish to enumerate List elements, we must use ListIterator. This cursor has additional methods and capabilities than the iterator.

| Iterator | ListIterator |
| :---: | :---: |
| Only has the ability to traverse components in a Collection in a forward direction. | In both forward and backward orientations, can traverse components in a Collection. |
| Iterators cannot be used to obtain indexes. | It offers methods to get element indexes at any time while traversing List, such as next Index() and previous Index(). |
| It aids in the traversal of Maps, Lists, and Sets. | Only List may be traversed, not the other two. |
| It throws a Concurrent Modification Exception since it can't add elements. | At any time, you can quickly add elements to a collection. |
| next(), remove(), and has Next are some of the Iterator's functions (). | next(), previous(), has Next(), has Previous(), and add() are some of the List Iterator's methods |

## What is the contract bt equals() and hashCode();

In Java, the \`equals()\` and \`hashCode()\` methods have a contract that defines how they should behave in relation to each other to ensure the correct functioning of hash-based collections like \`HashMap\` and \`HashSet\`. The contract is as follows:

**Consistent Behavior:**

* If two objects are equal according to the \`equals()\` method, they must have the same hash code.  
* If two objects have the same hash code, they are not necessarily equal according to the \`equals()\` method.

**Symmetry:**

* If \`a.equals(b)\` is true, then \`b.equals(a)\` must also be true.

**Transitivity:**

* If \`a.equals(b)\` is true and \`b.equals(c)\` is true, then \`a.equals(c)\` must also be true.

**Consistency:**

* If \`a.equals(b)\` is true at one point in time, it must remain true for the duration of both objects' existence, provided neither object is modified.  
* Similarly, the hash code for an object should consistently return the same value, provided no modification to the object’s state that is used in \`equals()\` and \`hashCode()\` calculations.

**Non-Null Reference:**

* For any non-null reference value \`a\`, \`a.equals(null)\` should return \`false\`.

Summary:  
The \`equals()\` and \`hashCode()\` methods must be consistent with each other to ensure that objects behave correctly when stored in hash-based collections. If \`equals()\` considers two objects equal, \`hashCode()\` must return the same value for these objects, ensuring proper functioning of collections like \`HashMap\` and \`HashSet\`.

## When the add() method of HashSet returns true and false?

The \`add()\` method of \`HashSet\` returns \`true\` if the element is successfully added to the set (i.e., it did not already exist in the set) and \`false\` if the element is not added because it already exists in the set.

## Comparable and Comparator.

| Comparable | Comparator |
| ----- | ----- |
| A single sorting sequence is provided by Comparable. To put it another way, we can sort the collection by a single attribute such as id, name, or price. | Multiple sorting sequences are available in the Comparator. To put it another way, we can sort the collection based on different criteria such as id, name, and price. |
| To sort elements, Comparable provides the compareTo() method. | To order elements, the Comparator provides the compare() method. |
| It is present in the java.lang package. | It is present in the java.util package. |
| The original class is affected by Comparable, i.e. the real class is changed.  | The original class is unaffected by the comparator, i.e. the real class is unaffected. |
| The Collections.sort(List) method can be used to sort Comparable type list members. | The Collections.sort(List, Comparator) method can be used to sort the list components of the Comparator type. |

## HashSet and TreeSet?

The primary differences between \`HashSet\` and \`TreeSet\` in Java are:  
**Ordering:**

* HashSet: Does not maintain any order of elements.  
* TreeSet: Maintains elements in a sorted order according to their natural ordering or a specified comparator.

**Performance:**

* HashSet: Offers constant-time performance (O(1)) for basic operations like add, remove, and contains.  
* TreeSet: Provides logarithmic time performance (O(log n)) for these operations due to its underlying Red-Black tree implementation.

**Null Values:**

* HashSet:\*\* Allows null elements.  
* TreeSet:\*\* Does not allow null elements because it uses comparisons for ordering.

Use \`HashSet\` when you need a collection with no duplicates and don't care about order. Use \`TreeSet\` when you need a sorted set of elements and are willing to trade off some performance for the ordering.

## Set vs Map.

The primary differences between \`Set\` and \`Map\` in Java are:

**Structure:**

* Set: A collection that contains no duplicate elements. It represents a group of objects, known as elements.  
* Map: A collection of key-value pairs, where each key is unique and maps to exactly one value.

**Element Storage:**

* Set: Stores only elements.  
* Map: Stores entries (key-value pairs).

**Access:**

* Set: Access elements directly using iteration.  
* Map: Access values by keys.

**Implementations:**

* Set: Common implementations include \`HashSet\`, \`LinkedHashSet\`, and \`TreeSet\`.  
* Map: Common implementations include \`HashMap\`, \`LinkedHashMap\`, and \`TreeMap\`.

Use a \`Set\` when you need a collection of unique elements. Use a \`Map\` when you need to associate keys with values, ensuring unique keys for value retrieval.

## HashSet and HashMap.

The primary differences between \`HashSet\` and \`HashMap\` in Java are:  
**Structure:**

* HashSet: A collection that stores unique elements.  
* HashMap: A collection that stores key-value pairs, with unique keys mapping to specific values.

**Storage:**

* HashSet: Internally uses a \`HashMap\` to store elements, where the elements are stored as keys and a dummy value is used.  
* HashMap: Stores entries consisting of keys and associated values.

**Usage:**

* HashSet: Used when you need a collection of unique elements.  
* HashMap: Used when you need to associate keys with values for quick retrieval.

**Methods:**

* HashSet: Provides methods like \`add()\`, \`remove()\`, and \`contains()\` for managing elements.  
* HashMap: Provides methods like \`put()\`, \`get()\`, \`remove()\`, and \`containsKey()\` for managing key-value pairs.

Use \`HashSet\` for storing unique elements without any key-value association. Use \`HashMap\` when you need to store key-value pairs and retrieve values based on keys.

## ArrayList and LinkedList.

The primary differences between \`ArrayList\` and \`LinkedList\` in Java are:

**Underlying Data Structure:**

* ArrayList: Uses a dynamic array to store elements.  
* LinkedList: Uses a doubly linked list to store elements.

**Access Time:**

* ArrayList: Provides O(1) time complexity for index-based access (i.e., \`get()\` and \`set()\` methods).  
* LinkedList: Provides O(n) time complexity for index-based access, as it requires traversal from the start or end.

**Insertion and Deletion:**

* ArrayList: Generally slower for insertion and deletion operations in the middle of the list (O(n)), as elements need to be shifted.  
* LinkedList: Faster for insertion and deletion operations in the middle (O(1)), as it involves just adjusting the links.

**Memory Overhead:**

* ArrayList: Has less memory overhead, as it only stores the actual elements.  
* LinkedList: Has higher memory overhead, as each element node stores additional references for the next and previous elements.

Use \`ArrayList\` for scenarios requiring fast random access and where the majority of operations are retrieval. Use \`LinkedList\` when you have a lot of insertions and deletions in the middle of the list and do not require fast random access.

## HashMap and TreeMap.

The primary differences between \`HashMap\` and \`TreeMap\` in Java are:

**Ordering:**

* HashMap: Does not maintain any order of the keys.  
* TreeMap: Maintains keys in a sorted order according to their natural ordering or a specified comparator.

**Performance:**

* HashMap: Offers O(1) time complexity for basic operations like \`put()\`, \`get()\`, \`remove()\`.  
* TreeMap: Provides O(log n) time complexity for these operations due to its underlying Red-Black tree implementation.

**Null Values:**

* HashMap: Allows one null key and multiple null values.  
* TreeMap: Does not allow null keys, but allows multiple null values.

**Use Cases:**

* HashMap: Best suited for unsorted, quick access to key-value pairs.  
* TreeMap: Ideal when you need sorted key-value pairs or require navigation methods (like \`firstKey()\`, \`lastKey()\`).

Use \`HashMap\` for faster access and no order requirements. Use \`TreeMap\` when you need sorted keys and order-specific operations.

## Collection and Collection**s**

The primary differences between \`Collection\` and \`Collections\` in Java are:

**Type:**

* Collection: An interface that is part of the Java Collections Framework. It defines the common methods that all collections (like \`List\`, \`Set\`, and \`Queue\`) must implement.  
* Collections: A utility class that provides static methods to operate on or return collections, such as sorting, searching, and synchronization.

**Purpose:**

* Collection: Defines a standard way to handle a group of objects.  
* Collections: Provides utility methods to perform common tasks on collections.

\`Collection\` is an interface that represents a group of objects, while \`Collections\` is a utility class with static methods to manipulate and operate on collections.

## How can we make the arrayList read only?

You can make an \`ArrayList\` read-only in Java by using the \`Collections.unmodifiableList()\` method. This method returns an unmodifiable view of the specified list, meaning that any attempt to modify the list will result in an \`UnsupportedOperationException\`.  
public class ReadOnlyArrayList {  
	public static void main(String\[\] args) {  
    	// Create and populate an ArrayList  
    	ArrayList\<String\> list \= new ArrayList\<\>();  
    	list.add("A");  
    	list.add("B");  
    	list.add("C");

    	// Make the ArrayList read-only  
    	List\<String\> readOnlyList \= Collections.unmodifiableList(list);

    	// Display the read-only list  
    	System.out.println("Read-Only List: " \+ readOnlyList);

    	// Attempt to modify the read-only list  
    	try {  
        	readOnlyList.add("D");  
    	} catch (UnsupportedOperationException e) {  
        	System.out.println("Cannot modify read-only list");  
    	}  
	}  
}

## Why are default methods introduced in interfaces?

Default methods were introduced in interfaces in Java 8 primarily to provide backward compatibility and enhance interface capabilities. They allow new methods to be added to interfaces without breaking existing implementations.

Key Reasons:

* **Backward Compatibility:** Enables the addition of new methods to existing interfaces without requiring all implementing classes to immediately update.  
* **Enhancing Interfaces:** Allows interfaces to have method implementations, which can promote code reuse and provide default behaviors.  
* **Multiple Inheritance of Behavior:** Provides a way to implement methods in interfaces, allowing classes to inherit behavior from multiple sources.

  \`\`\`java

  interface MyInterface {

  	void existingMethod();


  	// Default method with implementation

  	default void newDefaultMethod() {

      		System.out.println("This is a default method.");

  	}

  }


  class MyClass implements MyInterface {

  	@Override

  	public void existingMethod() {

      		System.out.println(

  "This is an existing method implementation.");

  	}

  }


  public class Main {

  	public static void main(String\[\] args) {

      		MyClass myObject \= new MyClass();

      		myObject.existingMethod();  // Calls the overridden method

      		myObject.newDefaultMethod();  // Calls the default method

  	}

  }

  \`\`\`

**Summary:**  
Default methods allow interfaces to evolve by adding new methods without breaking existing implementations, ensuring backward compatibility and enabling richer interfaces.

## Number of ways to create objects in Java

In Java, there are several ways to create objects. Here are the primary methods:

**Using the \`new\` Keyword:** The most common way to create an object.  
 	\`\`\`java  
 	MyClass obj \= new MyClass();  
 	\`\`\`  
**Using Reflection:** Allows dynamic creation of objects.  
 	\`\`\`java  
 	MyClass obj \= (MyClass) Class.forName("MyClass").newInstance();  
 	\`\`\`  
**Using \`clone()\` Method:** Creates a copy of an existing object. The class must implement the \`Cloneable\` interface.  
 	\`\`\`java  
 	MyClass obj1 \= new MyClass();  
 	MyClass obj2 \= (MyClass) obj1.clone();  
 	\`\`\`  
**Using Factory Methods:** Custom methods designed to create objects, often used in design patterns like Factory Method or Singleton.  
 	\`\`\`java  
 	MyClass obj \= MyClassFactory.createInstance();  
 	\`\`\`  
**Using Deserialization:** Creates an object from a byte stream, typically read from a file or network.  
 	\`\`\`java  
 	ObjectInputStream in \= new ObjectInputStream(new FileInputStream("file.ser"));  
 	MyClass obj \= (MyClass) in.readObject();  
 	\`\`\`  
**Using the \`newInstance()\` Method of the \`Constructor\` Class:** Description:\*\* Uses reflection to create a new instance.  
 	\`\`\`java  
 	Constructor\<MyClass\> constructor \= MyClass.class.getConstructor();  
 	MyClass obj \= constructor.newInstance();  
 	\`\`\`  
**Using Enum Constants:** Description:\*\* Each constant of an enum type is an instance of the enum type.  
 	\`\`\`java  
 	MyEnum obj \= MyEnum.CONSTANT;  
 	\`\`\`  
Summary:  
Java provides multiple ways to create objects, each suited for different scenarios ranging from simple instantiation to advanced techniques like reflection and deserialization.

## Where have you seen the fail safe arrayList?

In Java, the terms "fail-safe" and "fail-fast" refer to different behaviors of iterators when a collection is modified while it is being iterated over.

### **Fail-Fast:**

* **Description:** Fail-fast iterators immediately throw a \`ConcurrentModificationException\` if they detect that the collection has been modified structurally (elements added, removed, or modified) after the iterator was created.  
* **Common Examples:** Most of the iterators provided by the \`java.util\` package, such as those for \`ArrayList\`, \`HashSet\`, and \`HashMap\`.  
* **Behavior:** If a modification is detected during iteration, the fail-fast iterator fails quickly and cleanly by throwing an exception.  
* **Usage Scenario:** Useful for detecting concurrent modification issues during development and debugging.  
    \`\`\`  
    List\<String\> list \= new ArrayList\<\>(Arrays.asList("a", "b", "c"));  
    Iterator\<String\> iterator \= list.iterator();  
     
    while (iterator.hasNext()) {  
    	System.out.println(iterator.next());  
    	list.add("d"); // This will cause ConcurrentModificationException  
    }  
    \`\`\`

### **Fail-Safe:**

* **Description:** Fail-safe iterators do not throw \`ConcurrentModificationException\` if the collection is modified during iteration. Instead, they work on a copy of the collection’s data, thus allowing modifications.  
* **Common Examples:** Iterators provided by concurrent collections like \`CopyOnWriteArrayList\`, \`ConcurrentHashMap\`.  
* **Behavior:** Modifications to the collection during iteration do not affect the iteration process. These iterators operate on a snapshot of the collection's state.  
* **Usage Scenario:** Useful in concurrent applications where the collection can be modified by multiple threads without causing iteration issues.  
    \`\`\`java  
    CopyOnWriteArrayList\<String\> list \= new 

  CopyOnWriteArrayList\<\>(Arrays.asList("a", "b", "c"));


    Iterator\<String\> iterator \= list.iterator();  
     
    while (iterator.hasNext()) {  
    	System.out.println(iterator.next());  
    	list.add("d"); // No ConcurrentModificationException will be thrown  
    }  
    \`\`\`

Summary:  
Fail-Fast Iterators: Throw \`ConcurrentModificationException\` if the collection is modified during iteration. Commonly found in standard collections like \`ArrayList\`, \`HashSet\`.  
Fail-Safe Iterators: Allow modifications without throwing exceptions, typically found in concurrent collections like \`CopyOnWriteArrayList\`, \`ConcurrentHashMap\`.

 DriverManager

## How many exceptions have you dealt with till now and explain

Some of the common Java exceptions that every developer should know:

### **Checked Exceptions:**

**IOException:** Signals that an I/O operation has failed or been interrupted. Common Scenarios include File handling, network operations.  
 	\`\`\`  
 	try {  
     	FileReader file \= new FileReader("test.txt");  
 	} catch (IOException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**SQLException:** Provides information on a database access error or other errors. Common Scenarios include Database operations using JDBC.  
 	\`\`\`  
 	try {  
     	Connection con \= DriverManager.getConnection(url, user, password);  
 	} catch (SQLException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**ClassNotFoundException:** Thrown when an application tries to load a class through its name but no definition for the class with the specified name could be found. Common scenarios include Dynamic class loading.  
 	\`\`\`  
 	try {  
     	Class.forName("com.example.SomeClass");  
 	} catch (ClassNotFoundException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`

### **Unchecked Exceptions:**

**NullPointerException:** Thrown when an application attempts to use \`null\` where an object is required. Common scenarios include Accessing methods or fields of a null object.  
 	\`\`\`  
 	String str \= null;  
 	System.out.println(str.length()); // Throws NullPointerException  
 	\`\`\`  
**ArrayIndexOutOfBoundsException**: Thrown to indicate that an array has been accessed with an illegal index. Common scenarios include Accessing array elements with invalid indices.  
 	\`\`\`  
 	int\[\] arr \= new int\[3\];  
 	System.out.println(arr\[3\]); // Throws ArrayIndexOutOfBoundsException  
 	\`\`\`  
**ArithmeticException:** Thrown when an exceptional arithmetic condition has occurred. Common scenarios include Division by zero.  
 	\`\`\`  
 	int result \= 10 / 0; // Throws ArithmeticException  
 	\`\`\`  
**IllegalArgumentException:** Thrown to indicate that a method has been passed an illegal or inappropriate argument. Common scenarios include Passing invalid arguments to methods.  
 	\`\`\`  
 	Thread t \= new Thread();  
 	t.setPriority(100); // Throws IllegalArgumentException  
 	\`\`\`  
**NumberFormatException:** Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format. Common scenarios include Parsing strings to numbers.  
 	\`\`\`  
 	String number \= "abc";  
 	int num \= Integer.parseInt(number); // Throws NumberFormatException  
 	\`\`\`

### **Error:**

**StackOverflowError:** Thrown when the stack has overflowed, typically due to excessive recursion.  
Common Scenarios include Infinite recursion.  
 	\`\`\`  
 	public void recursiveMethod() {  
     	recursiveMethod(); // Causes StackOverflowError  
 	}  
 	\`\`\`  
**OutOfMemoryError:** Thrown when the JVM cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. Common scenarios include Memory leaks, large data processing.  
 	\`\`\`  
 	List\<int\[\]\> list \= new ArrayList\<\>();  
 	while (true) {  
     	list.add(new int\[1000000\]); // May eventually cause OutOfMemoryError  
 	}  
 	\`\`\`

### **Hibernate Exceptions:**

**HibernateException:** The base exception class for all Hibernate exceptions. Common Scenarios include Any generic Hibernate-related error.  
 	\`\`\`java  
 	try {  
     		Session session \= sessionFactory.openSession();  
     		// Some Hibernate operations  
 	} catch (HibernateException e) {  
     		e.printStackTrace();  
 	}  
 	\`\`\`  
**ConstraintViolationException:** Thrown when a database constraint (like a foreign key, unique key, or not-null constraint) is violated. Common Scenarios include Saving or updating entities.  
 	\`\`\`  
 	try {  
     		// Some Hibernate operations  
 	} catch (ConstraintViolationException e) {  
     		e.printStackTrace();  
 	}  
 	\`\`\`  
**LazyInitializationException:** Thrown when an uninitialized proxy or collection is accessed outside of a session context. Common Scenarios include Accessing lazily loaded collections or proxies after the session is closed.  
 	\`\`\`java  
 	try {  
     		// Fetching entity with lazy loaded collection  
 	} catch (LazyInitializationException e) {  
     		e.printStackTrace();  
 	}  
 	\`\`\`  
**QueryException:** Thrown when there is a problem with the query syntax or parameters. Common Scenarios include Issues in HQL/SQL queries.  
 	\`\`\`java  
 	try {  
     	Query query \= session.createQuery("FROM NonExistentEntity");  
     	query.list();  
 	} catch (QueryException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**StaleObjectStateException:** Thrown when an object was updated or deleted by another transaction after the current transaction loaded it. Common Scenarios includes Concurrent modifications in a multi-user environment.  
 	\`\`\`java  
 	try {  
     	// Update operation on a stale object  
 	} catch (StaleObjectStateException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`

### **Spring Exceptions:**

**UnsatisfiedDependencyException:** *UnsatisfiedDependencyException* gets thrown when some bean or property dependency isn’t satisfied. This may happen when a Spring application tries to wire a bean and can’t resolve one of the mandatory dependencies.

**BeansException**: The base exception class for all bean-related exceptions. Common Scenarios include Issues with bean creation, configuration, or wiring.  
 	\`\`\`java  
 	try {  
     	ApplicationContext context \= new ClassPathXmlApplicationContext("beans.xml");  
 	} catch (BeansException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**BeanCreationException:** Thrown when a bean could not be created. Common Scenarios includes Issues during bean instantiation or dependency injection.  
 	\`\`\`java  
 	try {  
     	ApplicationContext context \= new ClassPathXmlApplicationContext("beans.xml");  
 	} catch (BeanCreationException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**NoSuchBeanDefinitionException:** Thrown when a bean could not be found in the Spring context. Common Scenarios includes Requesting a non-existent bean.  
 	\`\`\`java  
 	try {  
     	ApplicationContext context \= new ClassPathXmlApplicationContext("beans.xml");  
     	MyBean bean \= context.getBean(MyBean.class);  
 	} catch (NoSuchBeanDefinitionException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**DataAccessException:** The base class for data access exceptions in Spring. Common Scenarios include Any database-related issue when using Spring's data access support.  
 	\`\`\`  
 	try {  
     	// Some database operations  
 	} catch (DataAccessException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
**TransactionException:** Thrown when there is a transaction-related issue. Common Scenarios include issues with transaction management, committing, or rolling back.  
 	\`\`\`java  
 	try {  
     	// Transactional operations  
 	} catch (TransactionException e) {  
     	e.printStackTrace();  
 	}  
 	\`\`\`  
Summary:  
Knowing these common exceptions in Hibernate and Spring helps developers diagnose and handle issues effectively, ensuring more robust and maintainable applications. Proper exception handling can improve debugging and provide better error feedback in production systems.

On what basis cache on hibernate works?  
	Query level

# StreamApi questions

* **Find list of students whose first name starts with alphabet A**

  List\<Student\> lstStuName \= list.stream().filter(dt \-\> dt.getFirstName().startsWith("A"))

     .collect(Collectors.toList());

  System.out.println("List of students whose name starts with letter A : "+lstStuName);

* **Group The Student By Department Names**

  Map\<String, List\<Student\>\> mapData \= list.stream().collect(Collectors.groupingBy(Student::getDepartmantName));

  System.out.println("Students grouped by the department names : "+mapData);

* **Find the total count of student using stream**

  long countStudent \= list.stream().count();

  System.out.println("Total count of students : "+countStudent);

* **Find the max age of student**

  OptionalInt maxAge \= list.stream().mapToInt(dt \-\> dt.getAge()).max();

  System.out.println("Max age of student : "+maxAge.getAsInt());

* **Find all departments names**

  List\<String\> lstDepartments \= list.stream().map(dt \-\> dt.getDepartmantName()).distinct()

     .collect(Collectors.toList());

  System.out.println("All distinct department names : "+lstDepartments);

* **Find the count of student in each department**

  Map\<String, Long\> countStudentInEachdept \= list.stream()

     .collect(Collectors.groupingBy(Student::getDepartmantName, Collectors.counting()));

  System.out.println("Student count in each department : "+countStudentInEachdept);

* **Find the list of students whose age is less than 30**

  List\<Student\> lstStudent \= list.stream().filter(dt \-\> dt.getAge() \< 30).collect(Collectors.toList());

  System.out.println("List of students whose age is less than 30 : "+lstStudent);

* **Find the list of students whose rank is in between 50 and 100**

  List\<Student\> lstStu \= list.stream().filter(dt \-\> dt.getRank() \> 50 && dt.getRank() \< 100\)

     .collect(Collectors.toList());

  System.out.println("List of students whose rank is between 50 and 100 : "+lstStu);

* **Find the average age of male and female students**

  Map\<String, Double\> mapAvgAge \= list.stream()

     .collect(Collectors.groupingBy(Student::getGender, Collectors.averagingInt(Student::getAge)));

  System.out.println("Average age of male and female students : "+mapAvgAge);

* **Find the department who is having maximum number of students**

  Entry\<String, Long\> entry \= list.stream()

     .collect(Collectors.groupingBy(Student::getDepartmantName, Collectors.counting())).entrySet().stream()

     .max(Map.Entry.comparingByValue()).get();

  System.out.println("Department having maximum number of students : "+entry);

* **Find the Students who stays in Delhi and sort them by their names**

  List\<Student\> lstDelhistudent \= list.stream().filter(dt \-\> dt.getCity().equals("Delhi"))

     .sorted(Comparator.comparing(Student::getFirstName)).collect(Collectors.toList());

  System.out.println("List of students who stays in Delhi and sort them by their names : "+lstDelhistudent);

* **Find the average rank in all departments**

  Map\<String, Double\> collect \= list.stream()

     .collect(Collectors.groupingBy(Student::getDepartmantName, Collectors.averagingInt(Student::getRank)));

  System.out.println("Average rank in all departments  : "+collect);

* **Find the highest rank in each department**

  Map\<String, Optional\<Student\>\> studentData \= list.stream().collect(Collectors.groupingBy(Student::getDepartmantName,

     Collectors.minBy(Comparator.comparing(Student::getRank))));

  System.out.println("Highest rank in each department  : "+studentData);

* **Find the list of students and sort them by their rank**

  List\<Student\> stuRankSorted \= list.stream().sorted(Comparator.comparing(Student::getRank))

     .collect(Collectors.toList());

  System.out.println("List of students sorted by their rank  : "+stuRankSorted);

* **Find the student who has second rank**

  Student student \= list.stream().sorted(Comparator.comparing(Student::getRank)).skip(1).findFirst().get();

  System.out.println("Second highest rank student  : "+student);

# Why are strings immutable in Java?

Strings are immutable in Java for several key reasons:

* **Security**: Immutable strings prevent security vulnerabilities that could arise if strings are mutable. If strings are mutable, a hacker could potentially modify a string reference and cause an application to load the wrong class, leading to security issues.\[3\]\[4\]  
* **Synchronization and Concurrency**: Immutable strings are thread-safe, as multiple threads can access the same string instance without the need for synchronization. This improves performance in concurrent applications.\[3\]\[4\]  
* **Caching**: The Java Virtual Machine (JVM) can efficiently cache string literals in the string pool, since immutable strings will always have the same hash code. This reduces memory usage.\[3\]\[4\]  
* **Class Loading**: The immutability of strings ensures that the correct class is always loaded by the class loader. If strings are mutable, the class loader could potentially load the wrong class, leading to errors.\[3\]  
* **Performance**: Immutable strings allow the JVM to perform various optimizations, such as deduplicating identical string literals and performing aggressive compiler optimizations, which improve overall application performance.\[1\]\[2\]\[4\]

Strings in Java are immutable to enhance security, ensure thread safety, optimize performance through string pooling and hash code caching, and provide consistency and predictability in behavior. These benefits make String a powerful and reliable class in the Java programming language.\[1\]\[2\]\[3\]\[4\]

# What are the changes done to the Java 8 interface? And what are the advantages it brought to it?

**Default Methods**: Java 8 allows interfaces to have default methods with implementation. This means interfaces can now have methods with a body, marked with the \`default\` keyword.

* They provide a way to add new methods to interfaces without breaking existing implementations of that interface.  
* Implementing classes are not required to implement default methods. If needed, they can override the default implementation.  
* The access modifier for default methods is implicitly \`public\`.

The main advantage of default methods is that they enable adding new functionality to interfaces without breaking existing code that implements those interfaces.

**Static Methods:** Java 8 also allows interfaces to have static methods.

* They are similar to default methods, except they cannot be overridden in implementing classes.  
* They are implicitly \`public\`.  
* They can be called on the interface itself, using the interface name.

The advantages of static methods in interfaces are:

* They provide utility methods that don't require an instance of the interface.  
* They allow adding new functionality to interfaces without breaking existing code.

In summary, the introduction of default and static methods in Java 8 interfaces provides a way to evolve interfaces over time and add new functionality without breaking existing implementations. This enables better code reuse and extensibility.

# What is a functional interface?

It's an interface which has one abstract method and it can have any number of static and default methods. Also it should be annotated with @functional Interface.

# What is the lambda function and what are the advantages of Lambdas in java?

Lambda expressions in Java are a concise way to represent anonymous functions. They allow you to write smaller, more readable code by eliminating the need for boilerplate method declarations.

The key advantages of using lambda expressions in Java are:

**Conciseness**

* Lambda expressions provide a more compact syntax compared to defining a separate method or anonymous inner class.  
* This makes the code more readable and reduces boilerplate.

**Functional Programming**

* Lambda expressions enable functional programming techniques in Java, such as passing functions as arguments, returning functions, and using higher-order functions.  
* This promotes a more declarative style of programming.

**Improved Readability**

* Lambda expressions make the intent of the code more explicit by focusing on what the code does rather than how it does it.  
* This can improve the overall readability and maintainability of the codebase.

**Parallelism and Streams**

* Lambda expressions integrate well with Java 8's Streams API, enabling efficient parallel processing of data.  
* This allows for more concise and powerful data processing pipelines.

In summary, lambda expressions in Java provide a more concise and functional way of writing code, leading to improved readability, maintainability, and support for parallel processing. They are a key feature of Java 8 that enables a more modern and expressive programming style.

# Can we print in the console without the main method?

1. **Static Blocks**: You can print to the console using a static block, which executes when the class is loaded.

     \`\`\`

     class WithoutMain {

     	static {

         	System.out.println("Hello World\!\!");

         	System.exit(0); 

   // Prevents JVM from looking for main method

     	}

     }

     \`\`\`

* Limitations:  
  * **Java Version**: This method works in Java versions up to 6\. From Java 7 onwards, the JVM requires a \`main\` method for execution.  
  * **IDE Behavior**: Some IDEs may enforce the presence of a \`main\` method.

2. **JUnit Tests**: You can also print to the console within JUnit test cases without needing a \`main\` method.

While printing to the console without a \`main\` method is possible, it is not a common practice and has significant limitations in modern Java development.

# Can we create multiple static blocks in a single class?

Multiple Static Blocks in Java

* A class can have any number of static blocks in Java.  
* Static blocks are executed in the order they appear in the class, from top to bottom, when the class is loaded.  
* Useful for initializing static variables based on complex logic.

Use Cases of Static Blocks

* Initializing static variables.  
* Performing static setup (e.g., loading configuration files, connecting to databases).  
* Executing code at class loading time

Summary:

* Static blocks are executed only once, when the class is first loaded.  
* If you create multiple instances of the class, the static blocks will not be re-executed. 

# What is finally block. Can we create multiple finally blocks and explain about the execution process of it.

The \`finally\` block in Java is a crucial component of exception handling that ensures a block of code is executed regardless of whether an exception occurs or is caught. It follows a \`try\` block and any associated \`catch\` blocks.

**Key Features of the \`finally\` Block**

* **Guaranteed Execution**: The code inside the \`finally\` block is executed after the \`try\` and \`catch\` blocks, regardless of whether an exception was thrown or handled. This makes it ideal for cleanup operations, such as closing files or releasing resources.

    \`\`\`

    try {

    	// Code that may throw an exception

    } catch (ExceptionType e) {

    	// Handle exception

    } finally {

    	// Code that will always execute

    }

    \`\`\`

* **Single \`finally\` Block**: A \`try\` block can have only one \`finally\` block, but it can have multiple \`catch\` blocks. You cannot create multiple \`finally\` blocks for a single \`try\` statement.

**Execution Process**

* **Normal Execution**: If no exception occurs, the \`finally\` block executes after the \`try\` block completes.  
* **Exception Handling**: If an exception is thrown and caught in the \`catch\` block, the \`finally\` block executes afterward.  
* **Return Statements**: If a return statement is executed in the \`try\` or \`catch\` block, the \`finally\` block still executes before the method returns.  
* **Unhandled Exceptions**: If an exception occurs that is not caught, the \`finally\` block executes before the program terminates.  
* **Exceptions to Execution**: The \`finally\` block will not execute if the program is terminated by calling \`System.exit()\` or if a fatal error occurs that causes the JVM to abort.

Conclusion  
The \`finally\` block is essential for ensuring that critical cleanup code runs, regardless of how the preceding code executes. It provides a reliable way to manage resources and maintain program stability.

# Dependencies that we have used till now.

Spring Boot simplifies dependency management by providing a variety of "starter" dependencies that aggregate common libraries needed for various functionalities. Here are some of the common dependencies used in Spring Boot projects:

Common Spring Boot Dependencies

* Core Starter:   
  * **\`spring-boot-starter\`** The core starter that includes essential dependencies for Spring applications, such as auto-configuration, logging, and YAML support.

* Web Applications:   
  * **\`spring-boot-starter-web\`**: For building web applications, including RESTful services. It includes Spring MVC and embedded Tomcat.

* Data Access:   
  * **\`spring-boot-starter-data-jpa\`**: For JPA (Java Persistence API) support, enabling database interactions with Spring Data JPA.  
  * **\`spring-boot-starter-jdbc\`**: For JDBC support, allowing direct database access without JPA.  
  * **mysql-connector-j**

* Security:  
  * **\`spring-boot-starter-security\`**\*\*: Provides security features for authentication and authorization in web applications.

* Testing:  
  * **\`spring-boot-starter-test\`**: Includes testing libraries such as JUnit, Mockito, and Spring Test for writing unit and integration tests.

* Development Tools:  
  * **\`spring-boot-devtools\`**: Provides features for improved development experience, such as automatic restarts and live reload.

* API Documentation:  
  * **\`springdoc-openapi-ui\`:**   
  * **\`springdoc-swagger2.ui\`:**

* Messaging:  
  * **\`spring-boot-starter-amqp\`**: For messaging with RabbitMQ.  
  * **\`spring-boot-starter-activemq\`**: For messaging with ActiveMQ.

* Template Engines:  
  * **\`spring-boot-starter-thymeleaf\`**: For server-side rendering using the Thymeleaf template engine.  
  * **\`spring-boot-starter-freemarker\`**: For server-side rendering using Freemarker.

* Microservices:  
  * **\`spring-boot-starter-eureka\`**: For service discovery with Netflix Eureka.  
  * **\`spring-boot-starter-cloud\`**: For cloud-native applications, including Spring Cloud features.

* Reactive Programming:  
  * **\`spring-boot-starter-webflux\`**: For building reactive web applications using Spring WebFlux.

Spring Boot's starter dependencies significantly reduce the complexity of managing libraries and configurations, allowing developers to focus on writing business logic rather than dealing with dependency management. Each starter encapsulates a set of related dependencies, making it easier to include necessary functionalities in a Spring Boot application \[1\]\[2\]\[4\]\[5\].

# API

The term **API**(Application Programming Interface) encompasses a broad range of interfaces that allow different software applications to communicate with each other. The reason it is called an API is that it serves as a contract or a set of rules that defines how software components should interact, regardless of the underlying implementation.

Understanding Different Types of APIs

* **General API**: This is a generic term that refers to any interface that allows different software systems to communicate. It can include libraries, frameworks, or any set of functions that a developer can use to interact with a software component.  
* **Stream API**: In Java, the Stream API is a specific API that allows developers to process sequences of elements (like collections) in a functional style. It provides methods for filtering, mapping, and reducing data, making it easier to work with collections of data.  
* **REST API**: REST (Representational State Transfer) APIs are a specific type of web API that adhere to the principles of REST architecture. They use standard HTTP methods (GET, POST, PUT, DELETE) for communication and are designed to be stateless and scalable. REST APIs are commonly used for web services and facilitate interaction between client and server over the internet.

Differences Between APIs

* **Purpose**: While all APIs serve the purpose of enabling communication between software components, their specific use cases can vary widely. For example, the Stream API is focused on data processing, while REST APIs are designed for web communication.  
* **Implementation**: Different APIs may have different methods, protocols, and data formats. For instance, REST APIs typically use JSON or XML for data exchange, whereas the Stream API uses method chaining for processing data.  
* **Scope**: Some APIs, like the Java Stream API or Date and Time API, are specific to the Java programming language and its ecosystem, while REST APIs can be implemented in any programming language that supports HTTP.

In summary, the term API is used to describe a wide range of interfaces that allow software components to interact. Different APIs, such as the Stream API, Date and Time API, and REST APIs, serve different purposes and are designed for specific use cases. Understanding these distinctions helps developers choose the right API for their needs and utilize them effectively in their applications.

# Caching java.

Second-Level Cache with Hibernate and EhCache  
\`\`\`  
import org.hibernate.Session;  
import org.hibernate.SessionFactory;  
import org.hibernate.cfg.Configuration;

public class SecondLevelCacheExample {  
	public static void main(String\[\] args) {  
    	SessionFactory sessionFactory \= new Configuration()  
        	.configure()  
        	.buildSessionFactory();

    	Session session1 \= sessionFactory.openSession();  
    	Book book1 \= session1.get(Book.class, 1L);  
    	System.out.println(book1.getTitle());  
    	session1.close();

    	Session session2 \= sessionFactory.openSession();  
    	Book book2 \= session2.get(Book.class, 1L);  
    	System.out.println(book2.getTitle());  
    	session2.close();  
	}  
}  
\`\`\`  
In this example, we configure Hibernate to use EhCache as the second-level cache provider. We then open two separate sessions and retrieve the same book entity using its ID. The first query will hit the database, but the second query will retrieve the book from the second-level cache.

To enable second-level caching in Hibernate, we need to configure the cache provider in \`hibernate.cfg.xml\`:  
\`\`\`xml  
\<hibernate-configuration\>  
	\<session-factory\>  
    	\<\!-- Other configuration \--\>  
    	\<property name="hibernate.cache.use\_second\_level\_cache"\>true\</property\>  
    	\<property name="hibernate.cache.region.factory\_class"\>org.hibernate.cache.ehcache.EhCacheRegionFactory\</property\>  
	\</session-factory\>  
\</hibernate-configuration\>  
\`\`\`  
We also need to annotate the entities we want to cache:  
\`\`\`java  
@Entity  
@Cacheable  
@org.hibernate.annotations.Cache(usage \= CacheConcurrencyStrategy.READ\_WRITE)  
public class Book {  
	// Fields and methods  
}  
\`\`\`  
These examples demonstrate how to implement in-memory caching using a library like Guava Cache and second-level caching using Hibernate with EhCache. The in-memory cache is useful for caching frequently accessed data within a single application instance, while the second-level cache is beneficial for caching data across multiple sessions and instances of an application.

# Configuration, EnableAutoConfiguration, and PropertiesConfiguration.

In Spring Boot, configuration annotations play a crucial role in defining and managing the configuration of your application. Here’s an overview of the key configuration annotations, particularly focusing on \`@Configuration\`, \`@EnableAutoConfiguration\`, and \`@ConfigurationProperties\`.

**\`@Configuration\`**

* **Purpose**: The \`@Configuration\` annotation indicates that a class declares one or more \`@Bean\` methods. These methods return instances of beans that should be managed by the Spring container.  
* Usage\*\*: It is used to define configuration classes in a Spring application, allowing for Java-based configuration instead of XML configuration.

  \`\`\`java

  import org.springframework.context.annotation.Bean;

  import org.springframework.context.annotation.Configuration;


  @Configuration

  public class AppConfig {


  	@Bean

  	public MyService myService() {

      	return new MyService();

  	}

  }

  \`\`\`

In this example, \`AppConfig\` is a configuration class that defines a bean of type \`MyService\`.

**\`@EnableAutoConfiguration\`**

* **Purpose**: This annotation is part of Spring Boot's auto-configuration feature. It tells Spring Boot to automatically configure your application based on the dependencies present on the classpath.  
* **Functionality**: When you annotate your main application class with \`@EnableAutoConfiguration\`, Spring Boot scans the classpath and configures beans and settings automatically, providing sensible defaults for various components like databases, web servers, etc.

  \`\`\`java

  import org.springframework.boot.SpringApplication;

  import org.springframework.boot.autoconfigure.SpringBootApplication;


  @SpringBootApplication // This includes @EnableAutoConfiguration

  public class MyApplication {

  	public static void main(String\[\] args) {

      	SpringApplication.run(MyApplication.class, args);

  	}

  }

  \`\`\`

In this example, the \`@SpringBootApplication\` annotation includes \`@EnableAutoConfiguration\`, enabling automatic configuration for the application.

**\`@ConfigurationProperties\`**

* **Purpose**: This annotation is used to bind external configuration properties (like those in \`application.properties\` or \`application.yml\`) to a Java object.  
* **Usage**: It allows you to create a strongly typed configuration class that can hold multiple related properties, making it easier to manage configuration.

  \`\`\`

  import org.springframework.boot.context.properties.ConfigurationProperties;

  import org.springframework.stereotype.Component;


  @Component

  @ConfigurationProperties(prefix \= "app")

  public class AppProperties {

  	private String name;

  	private String version;


  	// Getters and Setters

  	public String getName() {

      	return name;

  	}

  	public void setName(String name) {

      	this.name \= name;

  	}

  	public String getVersion() {

      	return version;

  	}

  	public void setVersion(String version) {

      	this.version \= version;

  	}

  }

  \`\`\`

In this example, \`AppProperties\` is a configuration class that binds properties prefixed with \`app\` from the \`application.properties\` file.

Summary

* **\`@Configuration\`**: Used to define configuration classes and bean definitions.  
* **\`@EnableAutoConfiguration\`**: Enables Spring Boot's automatic configuration based on the classpath.  
* **\`@ConfigurationProperties\`**: Binds external configuration properties to Java objects for easier management.

These annotations collectively enhance the flexibility and maintainability of Spring Boot applications by allowing developers to define configurations in a structured and type-safe manner.

# Jar and War.

The difference between JAR (Java ARchive) and WAR (Web Application aRchive) files is primarily based on their intended use and structure. Here’s a concise comparison:

**JAR (Java ARchive)**

* **Purpose**: JAR files are used to package Java classes, libraries, and resources into a single archive for distribution. They are typically used for standalone applications or libraries.  
* **Contents**: A JAR file can contain:  
  * \`.class\` files (compiled Java classes)  
  * Metadata (like a \`MANIFEST.MF\` file)  
  * Resources (like images, property files, etc.)

* Structure: JAR files do not have a specific internal structure, allowing flexibility in how files are organized.  
* Deployment: JAR files can be run on any Java Runtime Environment (JRE) and can also be included as libraries in other applications or WAR files.  
* Example Use Case\*\*: Packaging utility libraries or standalone applications.

**WAR (Web Application aRchive)**

* Purpose\*\*: WAR files are specifically designed to package web applications that can be deployed on a servlet container or web server (like Tomcat, Jetty, etc.).  
* Contents\*\*: A WAR file contains:  
  * Web components (like Servlets, JSP files)  
  * Static resources (HTML, CSS, JavaScript)  
  * A \`WEB-INF\` directory which includes:  
    * \`web.xml\` (deployment descriptor)  
    * Other libraries (JAR files) needed for the web application

* Structure: WAR files have a predefined structure that must include the \`WEB-INF\` directory, which is essential for the web application to function correctly.  
* Deployment: WAR files are deployed to servlet containers, which provide the necessary environment for running web applications.  
* Example Use Case\*\*: Deploying a web application that serves dynamic content to users.

\#\#\# Summary Table

| Feature                	| JAR                             	| WAR                             	|  
|----------------------------|-------------------------------------|-------------------------------------|  
| \*\*Purpose\*\*              | Packaging Java classes and libraries| Packaging web applications       	|  
| \*\*Contents\*\*           	| \`.class\` files, metadata, resources | Web components, static resources, \`WEB-INF\` |  
| \*\*Structure\*\*             | Flexible structure              	| Predefined structure with \`WEB-INF\` |  
| \*\*Deployment\*\*        | Any Java runtime environment    	| Servlet containers/web servers   	|  
| \*\*Use Case\*\*           	| Standalone applications or libraries| Web applications                 	|

In summary, JAR files are used for general Java applications and libraries, while WAR files are specifically designed for web applications that require a servlet container for deployment.

# **What were some of the key challenges you faced while developing the Spring Boot application?**

**Data Consistency and Transactions**

* Ensuring data consistency across multiple microservices was a challenge, especially for order and payment processing.  
* To address this, I frequently used the @Transaction annotation which helped me maintain the data consistency across the microservices.

**Service Communication and Resilience**

* Handling failures and timeouts during inter-service communication was critical  
* I leveraged Spring Cloud Openfeign, maintaining the inter service communication.  
* This made the microservices more resilient to failures and improved overall system stability

**Centralized Configuration and Logging**

* Maintaining consistent configuration and logging across multiple services was a challenge  
* I used Spring Cloud Config Server to externalize configuration and Jaeger for distributed tracing  
* This allowed me to manage configuration centrally and correlate logs across services

**Data Migration and Versioning**

* Handling data migrations and versioning across multiple databases was a concern.  
* I used Flyway for managing database schema migrations and versioning  
* This ensured that database changes were applied consistently across environments

By leveraging Spring Boot's opinionated defaults and Spring Cloud's ecosystem of tools, I was able to address these challenges and build a robust, scalable, and maintainable microservices architecture for the e-commerce application.

# What is distributed tracing? When you don’t know the answer.

I am not sure If I will be able to explain this topic or not but as far as I remember we implemented jaeger for distributed tracing which helped us gain insights into the performance and dependencies of our microservices architecture, making it easier to pinpoint failures and optimize system behavior.

# Bean scope

The Spring Framework provides a flexible way to manage the lifecycle and visibility of beans through various scopes. The scope of a bean defines how many instances of that bean will be created and how long they will live. Here are the primary scopes available in Spring:  
Bean Scopes in Spring

1\. \*\*Singleton\*\*:  
   \- \*\*Description\*\*: This is the default scope. A single instance of the bean is created per Spring IoC container. All requests for that bean will return the same instance.  
   \- \*\*Use Case\*\*: Ideal for stateless beans where the same instance can be shared across multiple requests\[1\]\[4\].

2\. \*\*Prototype\*\*:  
   \- \*\*Description\*\*: A new instance of the bean is created every time it is requested. This means that each request for the bean will yield a different instance.  
   \- \*\*Use Case\*\*: Suitable for stateful beans where each instance may maintain its own state\[1\]\[5\].

3\. \*\*Request\*\*:  
   \- \*\*Description\*\*: This scope creates a new bean instance for each HTTP request. The bean is only available during the lifecycle of that request.  
   \- \*\*Use Case\*\*: Useful for handling request-specific data, such as user input during a web request. This scope is only valid in a web-aware Spring ApplicationContext\[1\]\[4\].

4\. \*\*Session\*\*:  
   \- \*\*Description\*\*: A new bean instance is created for each HTTP session. The bean is available for the duration of the session.  
   \- \*\*Use Case\*\*: Ideal for maintaining user-specific data across multiple requests within a session, such as user preferences\[1\]\[4\].

5\. \*\*Application\*\*:  
   \- \*\*Description\*\*: Similar to singleton but scoped to the lifecycle of a ServletContext. A single instance is created for the entire application.  
   \- \*\*Use Case\*\*: Useful for beans that need to be shared across all users and sessions in a web application\[4\].

6\. \*\*WebSocket\*\*:  
   \- \*\*Description\*\*: This scope is specific to WebSocket sessions, allowing a single instance to be created for the lifecycle of a WebSocket connection.  
   \- \*\*Use Case\*\*: Useful for managing stateful interactions over WebSocket connections\[4\].

**Summary**  
The choice of bean scope in Spring is crucial for managing the lifecycle and sharing of beans effectively. The singleton and prototype scopes are available in all types of IoC containers, while the request, session, application, and WebSocket scopes are specific to web-aware contexts. Understanding these scopes helps in designing applications that manage resources efficiently and maintain the desired state across different components.

# **Spring Boot:**

## What is Spring?

Spring is a popular open-source application framework for Java that provides a comprehensive programming and configuration model for Java applications. It simplifies the development of Java applications by providing a set of abstractions and services that help developers write code more efficiently and effectively.

## What are the benefits of Spring Framework?

* **Lightweight:** Spring is lightweight when it comes to size and transparency. The basic version of spring framework is around 2MB.  
* **Inversion of Control (IoC)**: Spring uses IoC to manage the lifecycle and dependencies of application objects, making the code more modular, testable, and maintainable.  
* **Dependency Injection (DI)**: Spring's DI feature allows objects to define their dependencies without creating them, promoting loose coupling and flexibility.  
* **Aspect-Oriented Programming (AOP)**: Spring's AOP support enables the separation of cross-cutting concerns from business logic, leading to more modular and reusable code.  
* **Declarative Programming**: Spring's declarative approach to tasks like transaction management and caching simplifies development and promotes consistency.  
* **Abstraction and Integration**: Spring provides abstractions for JDBC, JMS, and other APIs, simplifying development and promoting consistency.  
* **Transaction Management:** Spring provides a consistent transaction management interface that can scale down to a local transaction and scale up to global transactions (JTA).  
* **Exception Handling:** Spring provides a convenient API to translate technology-specific exceptions (thrown by JDBC, Hiber-nate, or JDO) into consistent, unchecked exceptions.

## Which are the Spring framework modules?

The Spring Framework consists of several modules grouped into the following layers:

### Core Container

* **Core**: Provides the fundamental parts of the framework, including IoC and DI features.  
* **Beans**: Provides the BeanFactory, a sophisticated implementation of the factory pattern.  
* **Context**: Builds on the Core and Beans modules, providing a medium to access objects defined and configured.  
* **Expression Language (SpEL)**: Provides a powerful expression language for querying and manipulating an object graph at runtime.

### Data Access/Integration

* **JDBC**: Provides a JDBC-abstraction layer that removes the need for tedious JDBC-related coding.  
* **ORM**: Provides integration layers for popular object-relational mapping APIs, including JPA, JDO, Hibernate, and iBatis.  
* **OXM**: Provides an abstraction layer that supports Object/XML mapping implementations for JAXB, Castor, XMLBeans, JiBX, and XStream.  
* **JMS**: Contains features for producing and consuming messages.  
* **Transactions**: Supports programmatic and declarative transaction management.

### Web

* **Web**: Provides basic web-oriented integration features such as multipart file-upload functionality and the initialization of the IoC container using servlet listeners and a web-oriented application context.  
* **Web-MVC**: Contains Spring's Model-View-Controller (MVC) implementation for web applications.  
* **Web-Socket**: Provides support for WebSocket-based, two-way communication between the client and the server in web applications.  
* **Web-Portlet**: Provides the MVC implementation to be used in a portlet environment.

### AOP, Aspects, Instrumentation, Messaging, and Test

These modules provide support for aspect-oriented programming, class instrumentation, messaging, and testing, respectively.

## What is transaction management?

Transaction management refers to the process of managing a sequence of operations that must be executed as a single unit to ensure data consistency and integrity. It ensures that either all operations within a transaction are completed successfully (committed) or none are applied (rolled back) in the event of an error. Key aspects of transaction management include:

1. **ACID Properties**: Transactions must adhere to the ACID properties:  
   * **Atomicity**: Ensures that all operations in a transaction are completed; if one fails, the entire transaction fails.  
   * **Consistency**: Guarantees that a transaction takes the database from one valid state to another.  
   * **Isolation**: Ensures that transactions do not interfere with each other.  
   * **Durability**: Guarantees that once a transaction is committed, it remains so, even in the case of a system failure.  
2. **Concurrency Control**: Manages simultaneous transactions to prevent conflicts and ensure data integrity.  
3. **Recovery Management**: Restores the database to a consistent state after a failure, ensuring that committed transactions are preserved and uncommitted ones are discarded

## Explain the JDBC abstraction and DAO module

With the JDBC abstraction and DAO module we can be sure that we keep the database code clean and simple, and prevent problems that result from a failure to close database resources. It provides a layer of meaningful exceptions on top of the error messages given by several database servers. It also makes use of Spring’s AOP module to provide transaction management services for objects in a Spring application.

Explain the object/relational mapping integration module

Spring also supports for using of an object/relational mapping (ORM) tool over straight JDBC by providing the ORM module. Spring provides support to tie into several popular ORM frameworks, including Hibernate, JDO, and iBATIS SQL Maps. Spring’s transaction management supports each of these ORM frameworks as well as JDBC.

1.14	What are the benefits of IOC?

IOC or dependency injection minimizes the amount of code in an application. It makes easy to test applications, since no singletons or JNDI lookup mechanisms are required in unit tests. Loose coupling is promoted with minimal effort and least intrusive mechanism. IOC containers support eager instantiation and lazy loading of services.

1.15	What are the common implementations of the ApplicationContext?

The FileSystemXmlApplicationContext container loads the definitions of the beans from an XML file. The full path of the XML bean configuration file must be provided to the constructor. The ClassPathXmlApplicationContext container also loads the definitions of the beans from an XML file. Here, you need to set CLASSPATH properly because this container will look bean configuration XML file in CLASSPATH. The WebXmlApplicationContext container loads the XML file with definitions of all beans from within a web application.

1.16	What is the difference between Bean Factory and ApplicationContext?

Application contexts provide a means for resolving text messages, a generic way to load file resources (such as images), they can publish events to beans that are registered as listeners. In addition, operations on the container or beans in the container, which have to be handled in a programmatic fashion with a bean factory, can be handled declaratively in an application context. The ap-plication context implements MessageSource, an interface used to obtain localized messages, with the actual implementation being pluggable.

1.17	What does a Spring application look like?

An interface that defines the functions.

The implementation that contains properties, its setter and getter methods, functions etc.,

Spring AOP

The Spring configuration XML file.

Client program that uses the function

Chapter 2  
Dependency Injection  
2.1	What is Dependency Injection in Spring?

Dependency Injection, an aspect of Inversion of Control (IoC), is a general concept, and it can be expressed in many different ways.This concept says that you do not create your objects but describe how they should be created. You don’t directly connect your components and services together in code but describe which services are needed by which components in a configuration file. A container (the IOC container) is then responsible for hooking it all up.

2.2	What are the different types of IoC (dependency injection)?

Constructor-based dependency injection: Constructor-based DI is accomplished when the container invokes a class con-structor with a number of arguments, each representing a dependency on other class.

Setter-based dependency injection: Setter-based DI is accomplished by the container calling setter methods on your beans after invoking a no-argument constructor or no-argument static factory method to instantiate your bean.

2.3	Which DI would you suggest Constructor-based or setter-based DI?

You can use both Constructor-based and Setter-based Dependency Injection. The best solution is using constructor arguments for mandatory dependencies and setters for optional dependencies.

Chapter 3  
Spring Beans  
3.1	What are Spring beans?

The Spring Beans are Java Objects that form the backbone of a Spring application. They are instantiated, assembled, and managed by the Spring IoC container. These beans are created with the configuration metadata that is supplied to the container, for example, in the form of XML \<bean/\> definitions.

Beans defined in spring framework are singleton beans. There is an attribute in bean tag named "singleton" if specified true then bean becomes singleton and if set to false then the bean becomes a prototype bean. By default it is set to true. So, all the beans in spring framework are by default singleton beans.

3.2	What does a Spring Bean definition contain?

A Spring Bean definition contains all configuration metadata which is needed for the container to know how to create a bean, its lifecycle details and its dependencies.

3.3	How do you provide configuration metadata to the Spring Container?

There are three important methods to provide configuration metadata to the Spring Container:

XML based configuration file.

Annotation-based configuration

Java-based configuration

3.4	How do you define the scope of a bean?

When defining a \<bean\> in Spring, we can also declare a scope for the bean. It can be defined through the scope attribute in the bean definition. For example, when Spring has to produce a new bean instance each time one is needed, the bean’s scope attribute to be prototype. On the other hand, when the same instance of a bean must be returned by Spring every time it is needed, the the bean scope attribute must be set to singleton.

3.5	Explain the bean scopes supported by Spring

There are five scoped provided by the Spring Framework supports following five scopes:

In singleton scope, Spring scopes the bean definition to a single instance per Spring IoC container.

In prototype scope, a single bean definition has any number of object instances.

In request scope, a bean is defined to an HTTP request. This scope is valid only in a web-aware Spring ApplicationContext.

In session scope, a bean definition is scoped to an HTTP session. This scope is also valid only in a web-aware Spring ApplicationContext.

In global-session scope, a bean definition is scoped to a global HTTP session. This is also a case used in a web-aware Spring ApplicationContext.

The default scope of a Spring Bean is Singleton.

3.6	Are Singleton beans thread safe in Spring Framework?

No, singleton beans are not thread-safe in Spring framework.

3.7	Explain Bean lifecycle in Spring framework

The spring container finds the bean’s definition from the XML file and instantiates the bean.

Spring populates all of the properties as specified in the bean definition (DI).

If the bean implements BeanNameAware interface, spring passes the bean’s id to setBeanName() method.

If Bean implements BeanFactoryAware interface, spring passes the beanfactory to setBeanFactory() method.

If there are any bean BeanPostProcessors associated with the bean, Spring calls postProcesserBeforeInitial ization() method.

If the bean implements IntializingBean, its afterPropertySet() method is called. If the bean has init method declaration, the specified initialization method is called.

If there are any BeanPostProcessors associated with the bean, their postProcessAfterInitialization() methods will be called.

If the bean implements DisposableBean, it will call the destroy() method.

3.8	Which are the important beans lifecycle methods? Can you override them?

There are two important bean lifecycle methods. The first one is setup which is called when the bean is loaded in to the container. The second method is the teardown method which is called when the bean is unloaded from the container. The bean tag has two important attributes (init-method and destroy-method) with which you can define your own custom initialization and destroy methods. There are also the correspondive annotations(@PostConstruct and @PreDestroy).

3.9	What are inner beans in Spring?

When a bean is only used as a property of another bean it can be declared as an inner bean. Spring’s XML-based configura-tion metadata provides the use of \<bean/\> element inside the \<property/\> or \<constructor-arg/\> elements of a bean definition, in order to define the so-called inner bean. Inner beans are always anonymous and they are always scoped as prototypes.

3.10	How can you inject a Java Collection in Spring?

Spring offers the following types of collection configuration elements:

The \<list\> type is used for injecting a list of values, in the case that duplicates are allowed.

The \<set\> type is used for wiring a set of values but without any duplicates.

The \<map\> type is used to inject a collection of name-value pairs where name and value can be of any type.

The \<props\> type can be used to inject a collection of name-value pairs where the name and value are both Strings.

3.11	What is bean wiring?

Wiring, or else bean wiring is the case when beans are combined together within the Spring container. When wiring beans, the Spring container needs to know what beans are needed and how the container should use dependency injection to tie them together.

3.12	What is bean auto wiring?

The Spring container is able to autowire relationships between collaborating beans. This means that it is possible to automatically let Spring resolve collaborators (other beans) for a bean by inspecting the contents of the BeanFactory without using \<cons tructor-arg\> and \<property\> elements.

3.13	Explain different modes of auto wiring?

The autowiring functionality has five modes which can be used to instruct Spring container to use autowiring for dependency injection:

no: This is default setting. Explicit bean reference should be used for wiring.

byName: When autowiring byName, the Spring container looks at the properties of the beans on which autowire attribute is set to byName in the XML configuration file. It then tries to match and wire its properties with the beans defined by the same names in the configuration file.

byType: When autowiring by datatype, the Spring container looks at the properties of the beans on which autowire attribute is set to byType in the XML configuration file. It then tries to match and wire a property if its type matches with exactly one of the beans name in configuration file. If more than one such beans exist, a fatal exception is thrown.

constructor: This mode is similar to byType, but type applies to constructor arguments. If there is not exactly one bean of the constructor argument type in the container, a fatal error is raised.

autodetect: Spring first tries to wire using autowire by constructor, if it does not work, Spring tries to autowire by byType.

3.14	Are there limitations with autowiring?

Limitations of autowiring are:

Overriding: You can still specify dependencies using \<constructor-arg\> and \<property\> settings which will always override autowiring.

Primitive data types: You cannot autowire simple properties such as primitives, Strings, and Classes.

Confusing nature: Autowiring is less exact than explicit wiring, so if possible prefer using explicit wiring.

3.15	Can you inject null and empty string values in Spring?

Yes, you can.

Chapter 4  
Spring Annotations  
4.1	What is Spring Java-Based Configuration? Give some annotation example.

Java based configuration option enables you to write most of your Spring configuration without XML but with the help of few Java-based annotations. An example is the @Configuration annotation, that indicates that the class can be used by the Spring IoC container as a source of bean definitions. Another example is the @Bean annotated method that will return an object that should be registered as a bean in the Spring application context.

4.2	What is Annotation-based container configuration?

An alternative to XML setups is provided by annotation-based configuration which relies on the bytecode metadata for wiring up components instead of angle-bracket declarations. Instead of using XML to describe a bean wiring, the developer moves the configuration into the component class itself by using annotations on the relevant class, method, or field declaration.

4.3	How do you turn on annotation wiring?

Annotation wiring is not turned on in the Spring container by default. In order to use annotation based wiring we must enable it in our Spring configuration file by configuring \<context:annotation-config/\> element.

4.4	@Required annotation  
This annotation simply indicates that the affected bean property must be populated at configuration time, through an explicit property value in a bean definition or through autowiring. The container throws BeanInitializationException if the affected bean property has not been populated.

4.5	@Autowired annotation  
The @Autowired annotation provides more fine-grained control over where and how autowiring should be accomplished. It can be used to autowire bean on the setter method just like @Required annotation, on the constructor, on a property or pn methods with arbitrary names and/or multiple arguments.

4.6	@Qualifier annotation

When there are more than one beans of the same type and only one is needed to be wired with a property, the @Qualifier annotation is used along with @Autowired annotation to remove the confusion by specifying which exact bean will be wired.

Chapter 5  
Spring Data Access

5.1	How can JDBC be used more efficiently in the Spring framework?  
When using the Spring JDBC framework the burden of resource management and error handling is reduced. So developers only need to write the statements and queries to get the data to and from the database. JDBC can be used more efficiently with the help of a template class provided by Spring framework, which is the JdbcTemplate (example here).

5.2	JdbcTemplate

JdbcTemplate class provides many convenience methods for doing things such as converting database data into primitives or objects, executing prepared and callable statements, and providing custom database error handling.

5.3	Spring DAO support

The Data Access Object (DAO) support in Spring is aimed at making it easy to work with data access technologies like JDBC, Hibernate or JDO in a consistent way. This allows us to switch between the persistence technologies fairly easily and to code without worrying about catching exceptions that are specific to each technology.

5.4	What are the ways to access Hibernate by using Spring?

There are two ways to access Hibernate with Spring:

Inversion of Control with a Hibernate Template and Callback.

Extending HibernateDAOSupport and Applying an AOP Interceptor node.

5.5	ORM’s Spring support

Spring supports the following ORM’s:

Hibernate

iBatis

JPA (Java Persistence API)

TopLink

JDO (Java Data Objects)

OJB

5.6	How can we integrate Spring and Hibernate using HibernateDaoSupport?

Use Spring’s SessionFactory called LocalSessionFactory. The integration process is of 3 steps:

Configure the Hibernate SessionFactory

Extend a DAO Implementation from HibernateDaoSupport

Wire in Transaction Support with AOP

5.7	Types of the transaction management Spring support

Spring supports two types of transaction management:

Programmatic transaction management: This means that you have managed the transaction with the help of programming. That gives you extreme flexibility, but it is difficult to maintain.

Declarative transaction management: This means you separate transaction management from the business code. You only use annotations or XML based configuration to manage the transactions.

5.8	What are the benefits of the Spring Framework’s transaction management?

It provides a consistent programming model across different transaction APIs such as JTA, JDBC, Hibernate, JPA, and JDO.

It provides a simpler API for programmatic transaction management than a number of complex transaction APIs such as JTA.

It supports declarative transaction management.

It integrates very well with Spring’s various data access abstractions.

5.9	Which Transaction management type is more preferable?

Most users of the Spring Framework choose declarative transaction management because it is the option with the least impact on application code, and hence is most consistent with the ideals of a non-invasive lightweight container. Declarative transaction management is preferable over programmatic transaction management though it is less flexible than programmatic transaction management, which allows you to control transactions through your code.

Chapter 6  
Spring Aspect Oriented Programming (AOP)

6.1	Explain AOP  
Aspect-oriented programming, or AOP, is a programming technique that allows programmers to modularize crosscutting con-cerns, or behavior that cuts across the typical divisions of responsibility, such as logging and transaction management.

6.2	Aspect

The core construct of AOP is the aspect, which encapsulates behaviors affecting multiple classes into reusable modules. It ia a module which has a set of APIs providing cross-cutting requirements. For example, a logging module would be called AOP aspect for logging. An application can have any number of aspects depending on the requirement. In Spring AOP, aspects are implemented using regular classes annotated with the @Aspect annotation (@AspectJ style).

6.3	What is the difference between concern and cross-cutting concern in Spring

AOP

The Concern is behavior we want to have in a module of an application. A Concern may be defined as a functionality we want to implement. The cross-cutting concern is a concern which is applicable throughout the application and it affects the entire application. For example, logging, security and data transfer are the concerns which are needed in almost every module of an application, hence they are cross-cutting concerns.

6.4	Join point

The join point represents a point in an application where we can plug-in an AOP aspect. It is the actual place in the application where an action will be taken using Spring AOP framework.

6.5	Advice

The advice is the actual action that will be taken either before or after the method execution. This is actual piece of code that is invoked during the program execution by the Spring AOP framework.

Spring aspects can work with five kinds of advice:

before: Run advice before the a method execution.  
after: Run advice after the a method execution regardless of its outcome.  
after-returning: Run advice after the a method execution only if method completes successfully.  
after-throwing: Run advice after the a method execution only if method exits by throwing an exception.  
around: Run advice before and after the advised method is invoked.

6.6	Pointcut

The pointcut is a set of one or more joinpoints where an advice should be executed. You can specify pointcuts using expressions or patterns.

6.7	What is Introduction?

An Introduction allows us to add new methods or attributes to existing classes.

6.8	What is Target object?

The target object is an object being advised by one or more aspects. It will always be a proxy object. It is also referred to as the advised object.

6.9	What is a Proxy?

A proxy is an object that is created after applying advice to a target object. When you think of client objects the target object and the proxy object are the same.

6.10	What are the different types of AutoProxying?

BeanNameAutoProxyCreator

DefaultAdvisorAutoProxyCreator

Metadata autoproxying

6.11	What is Weaving? What are the different points where weaving can be ap-plied?

Weaving is the process of linking aspects with other application types or objects to create an advised object. Weaving can be done at compile time, at load time, or at runtime.

6.12	Explain XML Schema-based aspect implementation?

In this implementation case, aspects are implemented using regular classes along with XML based configuration.

6.13	Explain annotation-based (@AspectJ based) aspect implementation

This implementation case (@AspectJ based implementation) refers to a style of declaring aspects as regular Java classes anno-tated with Java 5 annotations.

Chapter 7  
Spring Model View Controller (MVC)

7.1	What is Spring MVC framework?  
Spring comes with a full-featured MVC framework for building web applications. Although Spring can easily be integrated with other MVC frameworks, such as Struts, Spring’s MVC framework uses IoC to provide a clean separation of controller logic from business objects. It also allows declaratively binding request parameters to business objects.

7.2	DispatcherServlet

The Spring Web MVC framework is designed around a DispatcherServlet that handles all the HTTP requests and responses.

7.3	WebApplicationContext

The WebApplicationContext is an extension of the plain ApplicationContext that has some extra features necessary for web applications. It differs from a normal ApplicationContext in that it is capable of resolving themes, and that it knows which servlet it is associated with.

7.4	What is Controller in Spring MVC framework?

Controllers provide access to the application behavior that you typically define through a service interface. Controllers interpret user input and transform it into a model that is represented to the user by the view. Spring implements a controller in a very abstract way, which enables you to create a wide variety of controllers.

7.5	@Controller annotation

The @Controller annotation indicates that a particular class serves the role of a controller. Spring does not require you to extend any controller base class or reference the Servlet API.

7.6	@RequestMapping annotation  
@RequestMapping annotation is used to map a URL to either an entire class or a particular handler method.

## Why to use spring boot rather than spring MVC?

* Spring Boot has an embedded Tomcat server, no need to add an external server.  
* It has a starter form Maven Dependency. (Web Starter, JPA Starter, etc.)  
* It automatically configures spring applications by using @Autoconfigure based on the dependencies.  
* It has annotations that’s why it skips XML configurations.

## Different ways to create spring boot annotations?

* Using Spring Initializer ([https://start.spring.io/](https://start.spring.io/))  
* Using Spring STS (Spring Tool Suite)  
* Using Spring Boot CLI  
* Using Spring IDE (Eclipse)

## How does spring boot application work?

* Create a new spring boot application.  
* First specify dependency starter in pom.xml  
* Then dependencies are added to the project.  
* Executes the program from main( ) where auto configuration is done.  
* Executes SpringApplication.run( ) that launches the program.

## What does @SpringBootApplication do?

* It marks class as a bean.  
* It has 3 annotations working inbuilt are @Configuration , @EnableAutoConfiguration and @ComponentScan.  
* @Configuration \= It tells that class is spring bean.  
* @EnableAutoConfiguration \= It configures applications as per jars added.  
* @ComponentScan \= Scans other packages in application.

## SpringApplication.run ( ) statement?

* It bootstraps and launches the application.

## How do we monitor & manage our application?

* To get production ready features we use spring boot actuators.  
* It has inbuilt HTTP endpoints.  
* We can create our endpoints.  
* Enable this using a spring boot actuator.  
* E.g. of endpoints /bean (name of beans in application), /health (up or down of application).

## What is spring boot profile (@profile)?

* It provides ways to divide applications to spare them for particular environments.  
* We specify @Profile to tell code is written for a particular environment.  
* Environments like Development environment, Production environment, Testing environment, etc.  
* Each environment has different configurations.

## What is spring data JPA?

* It has 3 repository interfaces in that-  
* CrudRepository (It is parent interface, used for CRUD operations)  
* PagingAndSortingRepository (It extends CrudRepository, used for Paging & Sorting purpose)  
* JPARepository (It extends PagingAndSortingRepository, used for all above and its additional services

## How to create custom queries?

* Using @Query annotation.  
* E.g. @Query("select c from City c where c.name like %?1") List\<City\> findByNameEndsWith(String chars);

## How to configure Hibernate in spring boot?

* Add JPA & MySQL database dependency.  
* In application.properties, write hibernate configurations to connect databases.

## How application.properties file added to IOC container?

* @EnableAutoConfiguration annotation is responsible for connection between database & application while configuring hibernate by adding application.properties file to container from its fixed path or specified path.

# RESTful Web Service:

## What is a web service?

* It is medium or way of communicating application over the network.  
* It is a client-server application or application component for communication.  
* The method of communication between two devices over the network.  
* It is a software system for the interoperable machine to machine communication.  
* It is a collection of standards or protocols for exchanging information between two devices or application.


## What are the advantages of web service?

* Interoperability: Web services are accessible over network and runs on HTTP/SOAP protocol and uses XML/JSON to transport data, hence it can be developed in any programming language. Web service can be written in java programming and client can be PHP and vice versa.  
* Reusability: One web service can be used by many client applications at the same time.  
* Loose Coupling: Web services client code is totally independent with server code, so we have achieved loose coupling in our application.  
* Easy to deploy and integrate, just like web applications.  
* Multiple service versions can be running at same time.

## What are the types of web service and difference between them?

SOAP (Simple object Access Protocol) & REST (Representational State transfer) are the types of web services.

| SOAP | REST |
| :---- | :---- |
| It supports XML data format only. | It supports XML, HTML, Plain text, JSON, etc. data formats. |
| It is protocol based. | It is architecture based. |
| SOAP cannot use REST. | REST can use SOAP. |
| It has its own security. | Have to add security. |
| It is less preferred. | It is more preferred. |
| Need JAX-WS API to implement SOAP. | Need JAX-RS API to implement REST. |

## What are the ways to implement Restful web service? 

* In JAX-RS, there are 3 types to implement Restful web service.  
* Jersey.  
* REST easy.  
* Spring with REST.

## By using spring with REST, how do we create Restful web service?

* Add REST dependency in pom.xml. (spring-boot-starter-data-rest)  
* Add @RestController annotation for controller class.  
* Map the methods written in controller class.  
* What is REST? Why do you choose Restful web service?  
* REST is the acronym for REpresentational State Transfer. REST is an architectural style for developing applications that can be accessed over the network.  
* REST is a stateless client-server architecture where web services are resources and can be identified by their URIs (Uniform Resource Identifiers).  
* We choose Restful web service because-  
* It is architectural style not protocol.  
* It is fast and has no restrictions like SOAP.  
* It uses data formats like XML, HTML, Plain Text, JSON, etc.  
* It also can use SOAP.  
* It is programming language and platform (OS) independent.


## Annotations used in Restful web service?

* @RestController  
* @GetMapping  
* @PostMapping  
* @DeleteMapping  
* @PutMapping  
* @PathVariable  
* @RequestBody  
* @ResponseBody

## Difference between @Controller & @RestController?

| @Controller | @RestController |
| :---- | :---- |
| It is used to mark a class as Spring MVC Controller. | It is used in RESTFul web services and the equivalent of @Controller \+ @ResponseBody. |
| It returns a view. | It returns data. |
| Added in Spring 2.5 version. | Added in Spring 4.0 version. |

## Difference between @PathVariable & @PathParam?

In Spring Boot, both \`@PathVariable\` and \`@PathParams\` are used to extract values from the URI of a request, but they serve slightly different purposes and are used in different contexts. Here’s a detailed explanation of each:

\#\# @PathVariable

\#\#\# Definition  
\`@PathVariable\` is an annotation used in Spring MVC to bind method parameters to URI template variables. It allows you to extract values from the URL and use them in your controller methods.

\#\#\# Usage  
\- \*\*Syntax\*\*: You can use \`@PathVariable\` in your request mapping methods to specify which part of the URI should be bound to a method parameter.  
\- \*\*Example\*\*:  
	\`\`\`java  
	@RestController  
	public class MyController {  
    	@GetMapping("/users/{userId}")  
    	public String getUser(@PathVariable("userId") String userId) {  
        	return "User ID: " \+ userId;  
    	}  
	}  
	\`\`\`  
  In this example, if you call \`/users/123\`, the \`userId\` parameter will be bound to the value \`123\`.

\#\#\# Optional Elements  
\- \*\*name\*\*: The name of the path variable to bind to.  
\- \*\*required\*\*: Indicates whether the path variable is required (default is true).  
\- \*\*value\*\*: An alias for \`name\`.

\#\#\# Example with Multiple Variables  
You can also bind multiple path variables:  
\`\`\`java  
@GetMapping("/products/{category}/{id}")  
public String getProduct(@PathVariable String category, @PathVariable String id) {  
	return "Category: " \+ category \+ ", Product ID: " \+ id;  
}  
\`\`\`

\#\# @PathParams

\#\#\# Definition  
While \`@PathParams\` is not a standard Spring annotation, it is often confused with \`@RequestParam\`, which is used for query parameters rather than path variables. However, if you are referring to a custom implementation or a specific library that uses \`@PathParams\`, it would typically serve a similar purpose as \`@PathVariable\`.

\#\#\# General Usage  
If you need to use query parameters instead of path variables, you would use \`@RequestParam\`. For example:  
\`\`\`java  
@GetMapping("/search")  
public String search(@RequestParam("query") String query) {  
	return "Search query: " \+ query;  
}  
\`\`\`  
In this case, if you call \`/search?query=spring\`, the \`query\` parameter will be bound to the value \`spring\`.

\#\# Summary

\- \*\*@PathVariable\*\*: Used for extracting values from the URI path. Useful in RESTful services where resource identifiers are part of the URL.  
\- \*\*@RequestParam\*\*: Used for extracting query parameters from the URL. Useful for optional parameters or filters.

Using these annotations appropriately helps create clean and maintainable RESTful APIs in Spring Boot applications.

## Have you Consumed or Produced Restful web service? Explain?

Consume or Produce in Restful web service means specifying which type of data to be requested (it is just telling type of data accepted or send through application)

* E.g. While consuming data type we use syntax, consumes=”application/JSON”, it specify that certain service accepts only JSON data format.  
* Produce is associated with @GetMapping annotation where we mention type of data while we are sending it when that method/service is called.  
* Consume is associated with @PostMapping annotation where we mention type of data is to be accepted for saving it into the database when that method/service is called.  
* E.g. Film Producer makes (Produce) Movies & Viewers watch (Consume) those movies.

## How to consume and produce data using xml format?

* First use @XmlRootElement on POJO class or need to add Xml data supporting dependency.  
* Then in Controller methods specify,  
* (For Produce) produces=”application/xml”  
* (For Consume) consumes=”application/xml”  
* In Restful web service, how to convert JSON format data to Object format or vice versa?  
* Object to JSON format:  
* ObjectMapper mapper=new ObjectMapper( );  
* String jsonResult=mapper.writeValueAsString(object);  
* JSON to Object format:  
* ObjectMapper mapper=new ObjectMapper( );  
* Student s=mapper.readValue (jsonResult, Student.class);

## Difference between API & web services?

| API | Web Services |
| :---- | :---- |
| It is an interface between two different applications. | It is interaction between applications over the network. |
| All APIs are not web services. | All web services are APIs. |
| API can be used for any style of communication. | Web service uses styles like REST, SOAP for communication. |
| It can be used by a client who understands JSON or XML. | It can be used by any client who understands XML. |
| API has a light-weight architecture. | Web Services does not have a light- weight architecture. |

## How to test web service?

* Using ARC & POSTMAN.  
* Locally –  
* By creating a war file.  
* Deploy on the local Tomcat server.

## How do you mock the web service?

Mocking Web service is testing applications using dummy data

## What are HTTP methods?

* GET, POST, DELETE, PUT, etc.  
* GET \- The GET method requests a representation of the specified resource. Requests using GET should only retrieve data.  
* POST \- The POST method is used to submit an entity to the specified resource, often causing a change in state.  
* PUT \- The PUT method replaces all current representations of the target resource with the request payload.  
* DELETE \- The DELETE method deletes the specified resource.  
* PATCH \- The PATCH method is used to apply partial modifications to a resource.

## What are components in HTTP?

Request, Body, Header, etc
