**Interview questions**

- ### What is a **compiler**? List some types of compiler.

A compiler is a computer program that **changes source code** written in a high-level language into low-level machine language. It translates the code written in one programming language to some other language without modifying the definition of the code.   
Some important types of compiler are:  
Just-In-Time (JIT) Compilers: JIT (Just-In-Time) compilers are a type of compiler that dynamically compiles and executes code at runtime.  
In the context of the Angular framework, JIT (Just-In-Time) compilation is used to compile TypeScript code into JavaScript code that can be executed by the browser. When an Angular application is built using JIT compilation, the compilation process happens in the user's browser at runtime, as opposed to ahead-of-time (AOT) compilation, where the compilation happens during the build process.  
Ahead-of-Time (AOT) Compilers: In computer science, ahead-of-time compilation is the act of compiling an higher-level programming language into an lower-level language before execution of a program, usually at build-time, to reduce the amount of work needed to be performed at run time.

* ### **Transpilation** in programming?

Transpilation is a process in which source code written in one programming language is transformed or translated into source code written in another programming language. The term "transpile" is a combination of "translate" and "compile".

In contrast to traditional compilation, transpilation is typically used when the source code is translated into a language that has similar syntax and functionality as the original language, but with additional features or compatibility with a specific runtime environment. For example, transpilation may be used to convert JavaScript code written in the latest version of ECMAScript into code that is compatible with older web browsers that do not support the latest JavaScript syntax.

Transpilers are tools that automate the process of transpiling code, and they are available for a variety of programming languages. Some popular transpilers include Babel for JavaScript, TypeScript for JavaScript, CoffeeScript for JavaScript, and Haxe for several programming languages.

* ### **Difference between Compilation and Transpilation?**

Compilation and transpilation are both processes that involve transforming code from one form to another, but they differ in the source and target languages.

Compilation is the process of translating code written in a high-level programming language into machine code that can be executed directly by the computer's processor. The output of a compiler is typically an executable file or a binary code that can be run on a specific platform or operating system. Compilers are used to convert code written in languages such as C, C++, Java, and Python into machine code.

Transpilation, on the other hand, is the process of translating code from one programming language to another. The output of a transpiler is usually code written in a different programming language that performs the same function as the input code. Transpilers are used to convert code written in languages such as TypeScript, CoffeeScript, or ES6 into code that can be run on a different platform or in a different environment. For example, transpiling TypeScript code into JavaScript code allows developers to use TypeScript in web browsers that do not natively support the language.

In summary, the main difference between compilation and transpilation is that compilation translates code into machine code, while transpilation translates code from one programming language to another.

- ### What are **primitive and non-primitive** data types?

Primitive data types are basic data types that are not objects and are immutable. There are five primitive data types in TypeScript: number, string, boolean, null, and undefined.  
Non-primitive data types, on the other hand, are more complex data types that are derived from primitive data types. They are mutable and can contain other values and objects. Some examples of non-primitive data types in TypeScript include arrays, objects, and functions, interface, class, etc.  
Here are some key differences between primitive and non-primitive data types in TypeScript:

* Primitive data types are simple, basic values, whereas non-primitive data types are more complex and can contain other values.  
  * Primitive data types are passed by value, meaning that a copy of the value is created when passed to a function or assigned to a new variable. Non-primitive data types are passed by reference, meaning that a reference to the original value is passed instead of a copy.  
  * Primitive data types have a fixed size in memory, while non-primitive data types can grow or shrink dynamically as needed.

* ### **D/f b/w Javascript and Typescript?**

JavaScript and TypeScript are both programming languages that are widely used in web development. Here are some key differences between the two:

- Type System: TypeScript is a statically typed language, which means that the types of variables and function parameters must be declared at compile-time. In contrast, JavaScript is a dynamically typed language, which means that the types of variables and function parameters are determined at runtime.  
- Compiler: TypeScript requires a compiler to convert TypeScript code to JavaScript code, while JavaScript code can be executed directly in a web browser or Node.js environment without the need for a compiler.  
- Syntax: TypeScript is a superset of JavaScript, which means that it includes all the features of JavaScript as well as additional syntax for type annotations and other features.  
- Error Handling: TypeScript provides compile-time error checking, which can help catch errors before runtime, while JavaScript errors can only be detected at runtime.  
- Tooling: TypeScript provides better tooling support, including code editors with built-in support for TypeScript syntax highlighting, code completion, and refactoring.  
- Learning Curve: TypeScript requires additional knowledge of types and other features not present in JavaScript, which can increase the learning curve for developers new to the language.  
- Adoption: JavaScript is more widely adopted and supported than TypeScript, which means that it may be easier to find libraries and resources for JavaScript development.

Overall, TypeScript is a more robust and structured language that can help catch errors early and make code more maintainable. However, it requires additional knowledge and tooling, and may not be necessary for smaller projects or simpler applications.

* ### What are spread operators?

The spread operator is a feature introduced in ECMAScript 6 (ES6) that allows an iterable such as an array or string to be expanded into individual elements. The syntax for the spread operator is three dots followed by the name of the iterable, like so:  
const arr \= \[1, 2, 3\];  
console.log(...arr); // output: 1 2 3  
The spread operator can be used in several ways:

1. Copying arrays: The spread operator can create a new array with the same elements as an existing array. For example:

   const arr1 \= \[1, 2, 3\];

   const arr2 \= \[...arr1\]; // create a new array with the same elements as arr1

   console.log(arr2); // output: \[1, 2, 3\]

   

   Combining arrays: The spread operator can also be used to concatenate arrays. For example:

   const arr1 \= \[1, 2\];

   const arr2 \= \[3, 4\];

   const combinedArr \= \[...arr1, ...arr2\];

   console.log(combinedArr); // output: \[1, 2, 3, 4\]

2.   
3. Function arguments: The spread operator can be used to pass an array as arguments to a function. For example:

   function sum(a, b, c) {

     return a \+ b \+ c;

   }

   

   const arr \= \[1, 2, 3\];

   console.log(sum(...arr)); // output: 6

4.   
   Overall, the spread operator is a convenient way to manipulate arrays and other iterables in JavaScript.

* ### What are constructors?

In Object Oriented Programming(OOP),a constructor is a special method that is called when an object is created from a class. The purpose of a constructor is to initialise the state of an object by assigning initial values to its parameter.

* ### D/f b/w Null and Undefined?

Null: It is the intentional absence of the value. It is one of the primitive values of JavaScript.  
Undefined: It means the value does not exist in the compiler. It is the global object.

- ### **What is Typescript?**

TypeScript is an open-source programming language developed and maintained by Microsoft. It is a superset of JavaScript, which means that any valid JavaScript code is also valid TypeScript code. TypeScript adds optional static typing and other features to JavaScript, making it more suitable for large-scale software projects.

One of the main benefits of TypeScript is its ability to catch errors at compile-time, rather than at runtime, which can help to prevent bugs and improve code quality. Additionally, TypeScript supports modern features of JavaScript, such as classes, interfaces, and async/await, and also allows developers to define their own types and interfaces.

* ### **What is an open-source programming language?**

An open source programming language is a programming language whose source code is freely available for users to study, modify, and distribute. This means that anyone can contribute to the development of the language by suggesting improvements, fixing bugs, and creating new features.  
Examples of popular open source programming languages include Python, Ruby, PHP, Java, and JavaScript.

- ### **Why Typescript?**

TypeScript offers several advantages over traditional JavaScript, including:

- Strong Typing: TypeScript supports static typing, which allows for catching errors at compile-time rather than runtime. This helps in identifying type-related bugs early in the development cycle, which ultimately leads to improved code quality and better maintainability.  
- Improved Code Maintainability: TypeScript offers a more structured and organised approach to coding. It makes it easier to read and understand code, and also makes it easier to maintain and refactor. It provides features like classes, interfaces, and modules, which are not available in JavaScript.  
- Better Tooling Support: TypeScript is supported by a variety of tools, including code editors and integrated development environments (IDEs), which offer features like autocompletion, code navigation, and error highlighting.  
- Large Community Support: TypeScript has a large and growing community of developers and contributors, which means that it is constantly improving and evolving. The community provides documentation, tutorials, and support, making it easier for developers to learn and use the language.  
- Backward Compatibility: TypeScript is a superset of JavaScript, which means that any valid JavaScript code is also valid TypeScript code. This makes it easier to adopt TypeScript gradually, by adding it to existing JavaScript projects or by converting JavaScript code to TypeScript.

Overall, TypeScript can help improve code quality, maintainability, and developer productivity, while also providing a better development experience. However, it is important to note that TypeScript may not be suitable for all projects and use cases, and the decision to use it should be based on the specific requirements and constraints of each project.

- ### What is a callback function?

A callback function is a function that is passed as an argument to another function and is executed by that function at a certain point in time. The idea behind callbacks is to allow a function to receive another function as input and to use that function as necessary, such as when an asynchronous operation completes.

- ### What is the **framework?**

A framework is a collection of pre-written code that provides a structure and set of rules for how to develop software applications. Frameworks provide developers with a foundation to work on and often include features like libraries, APIs, and templates that make it easier to develop complex applications.

Frameworks typically aim to solve common problems that developers encounter while building software, such as how to handle user interfaces, manage data, or connect to databases. By using a framework, developers can avoid having to reinvent the wheel and focus on writing code that is specific to their application's unique requirements.

* ### Difference b/w Angular and React?

Some common difference between Angular and react are as follows:

- Architecture: Angular is a complete framework that provides an opinionated structure and set of guidelines for building applications, while React is a library that focuses on providing a flexible and lightweight solution for building user interfaces.  
- Learning Curve: Angular can have a steeper learning curve due to its comprehensive nature and the use of TypeScript, which is a typed superset of JavaScript. React, on the other hand, has a simpler and more intuitive API, making it easier for developers to learn and start using quickly.  
- State Management: Angular uses a two-way data binding approach, where changes in the data automatically update the UI and vice versa. React, on the other hand, uses a unidirectional data flow, where data flows in one direction from parent to child components, making it easier to manage and maintain application state.  
- Performance: React is known for its fast rendering speed due to its use of a virtual DOM(Document Object Model), which minimises the number of actual DOM manipulations needed for updates. Angular uses a real DOM, which can lead to slower performance in some cases.  
- Tooling: Angular has a built-in CLI tool that provides a comprehensive set of features for building and testing applications, while React relies on external tools and libraries for features like routing and state management.

* ### **What is Angular?**

Angular is a popular open-source JavaScript/Typescript framework for building web applications. It is developed and maintained by Google and a community of developers.   
Angular is often used for building enterprise-level applications that require a high degree of functionality, reliability and performance. It is also widely used in the development of single-page applications (SPAs), where a single HTML page is dynamically updated in response to user actions, without requiring a full page refresh.

* ### Difference b/w **\== and \===**?

In TypeScript (and many other programming languages), the \== and \=== operators are used for equality comparison between two values.  
The main difference between \== and \=== is that \== performs a loose or abstract equality comparison, while \=== performs a strict or identity equality comparison.  
Here's what that means:

- \== (loose or abstract equality) compares values by first converting them to a common type, if necessary, and then comparing their values. This means that the two values being compared don't have to be of the same type. For example, 0 \== false is true because the false value is coerced to the number 0\.  
- \=== (strict or identity equality) compares values by both type and value. This means that the two values being compared must be of the same type and have the same value. For example, 0 \=== false is false because 0 is a number and false is a boolean, so they are not the same type.

* ### **What is a function()?**

In TypeScript, a function is a block of code designed to perform a specific task. It is a first-class citizen in the language, meaning that it can be assigned to variables, passed as arguments to other functions, and returned as values from other functions.

TypeScript also supports optional parameters, default parameter values, rest parameters, and function overloading, which allow you to define functions with varying parameter types and numbers.

* ### **Difference b/w slice() and splice()?**

In TypeScript, slice() and splice() are both array methods used to extract or modify parts of an array, but they have different behaviours and purposes.  
slice() is used to extract a portion of an array without modifying the original array, while splice() is used to modify an array by removing or replacing existing elements and/or adding new elements.

**1\. \`slice()\`**: The \`slice()\` method is used to extract a section of an array and return it as a new array, without modifying the original array. Example syntax: slice(start, end)  
\- \`**start**\`: The zero-based index at which to begin extraction. If negative, it is treated as \`length \+ start\` where \`length\` is the length of the array.  
**\- \`end\` (optional):** The zero-based index before which to end extraction. The character at this index is not included. If negative, it is treated as \`length \+ end\` where \`length\` is the length of the array. If \`end\` is omitted, \`slice()\` extracts through the end of the array.  
\`\`\`  
const fruits \= \['apple', 'banana', 'orange', 'mango'\];

const citrus \= fruits.slice(2);  
console.log(citrus); // Output: \['orange', 'mango'\]

const tropicalFruits \= fruits.slice(1, 3);  
console.log(tropicalFruits); // Output: \['banana', 'orange'\]  
\`\`\`  
2\. **\`splice()\`**: The \`splice()\` method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place. Example syntax:splice(start, deleteCount, item1, item2, ...)

**\`start\`**: The index at which to start changing the array. If negative, it is treated as \`length \+ start\` where \`length\` is the length of the array.  
**\- \`deleteCount\` (optional)**: An integer indicating the number of elements in the array to remove from \`start\`. If \`deleteCount\` is 0, no elements are removed.  
**\- \`item1, item2, ...\` (optional):** The elements to add to the array, beginning from \`start\`. If you do not specify any elements, \`splice()\` will only remove elements from the array.  
const numbers \= \[1, 2, 3, 4, 5\];

// Remove elements  
const removedElements \= numbers.splice(2, 2);  
console.log(numbers); // Output: \[1, 2, 5\]  
console.log(removedElements); // Output: \[3, 4\]

// Add elements  
numbers.splice(2, 0, 'a', 'b');  
console.log(numbers); // Output: \[1, 2, 'a', 'b', 5\]

// Replace elements  
numbers.splice(2, 1, 3);  
console.log(numbers); // Output: \[1, 2, 3, 'b', 5\]  
\`\`\`

* \`slice()\` extracts a section of an array and returns it as a new array, without modifying the original array.  
* \`splice()\` changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

Both methods are useful for manipulating arrays in JavaScript, but they serve different purposes. \`slice()\` is used for extracting a portion of an array, while \`splice()\` is used for inserting or removing elements from an array.

* ### What is **scope** in typescript?

In TypeScript, a scope is a region of a program where a particular identifier (such as a variable, function, class, or type) is valid and can be referenced.  
TypeScript has two types of scopes:

1. Global scope: The global scope is the outermost scope of a program, and any identifier declared outside of a function or block belongs to the global scope. Global scope identifiers are accessible from anywhere in the program.  
2. Local scope: A local scope is created whenever a new function or block is defined. Identifiers declared within a local scope are only accessible within that scope or any nested scopes. This means that variables declared inside a function or block are not visible outside of that function or block.

In addition to these two scopes, TypeScript also has a concept of block scope, which is created by using curly braces {} to define a block of code. Variables declared inside a block using the *let or const* keywords have block scope, which means they are only accessible within that block or any nested blocks.  
TypeScript also supports lexical scoping, which means that the scope of an identifier is determined by its position in the source code. This allows for nested functions to access variables declared in their outer function, creating a hierarchy of scopes.  
Overall, understanding scopes in TypeScript is crucial for writing well-organised and efficient code, and for preventing unintended side-effects caused by variable name clashes or global variable pollution.

* ### **What is class?**

In object-oriented programming (OOP), a class is a blueprint or template for creating objects that encapsulate data (attributes) and behaviour (methods). A class defines a set of attributes and methods that describe the characteristics and behaviours that the objects created from it will have.

For example, consider a class called "Car". This class may have attributes like make, model, year, and colour, and methods like start(), stop(), accelerate(), and brake(). Objects created from the "Car" class would have their own set of attribute values, such as a make of "Toyota" and a model of "Camry", and can perform actions using the methods defined in the class.

Classes are a fundamental building block of OOP, allowing programmers to create complex and organised code by defining and reusing reusable templates for objects.

* What is **super()** and why is it needed?

In object-oriented programming languages like JavaScript, super() is a keyword used to call a parent class's constructor method from a child class.   
When a subclass extends a superclass, it inherits all the properties and methods of the superclass. However, if the superclass has a constructor method, it is not automatically called when an instance of the subclass is created. To invoke the constructor of the parent class from the constructor of the child class, we use the super() method.

class Animal {  
   name:string;  
   constructor(name:string) {  
   this.name \= name;  
 }  
}

class Dog extends Animal {  
   breed;  
 constructor(name:string, breed:string) {  
   **super(name)**; // call the constructor of the parent class  
   this.breed \= breed;  
 }  
}

var Dog1 \= new Dog("Tommy", "Retriever")  
console.log(Dog1.name)    //”Tommy”  
In summary, the super() method is used to call the constructor of the parent class from the constructor of the child class, and it is needed to properly initialise the parent class's properties and methods when creating instances of the child class.

* ### What is **iteration**?

In JavaScript, iteration refers to the process of repeating a set of instructions or operations multiple times until a specific condition is met. It is a fundamental programming concept that allows you to perform the same task repeatedly.

There are several ways to perform iteration in JavaScript, including:

* for loop: It is a commonly used loop construct in JavaScript that allows you to execute a block of code repeatedly until a specified condition is met.  
* while loop: This loop continues to execute the block of code as long as the specified condition is true.  
* do-while loop: This loop executes the block of code once before checking the specified condition. If the condition is true, the loop continues to execute the block of code until the condition becomes false.  
* for-of loop: This loop is used to iterate over iterable objects such as arrays and strings and executes a block of code for each element.  
* forEach() method: It is an array method that executes a provided function once for each array element.  
* map() method: It is also an array method that creates a new array by executing a provided function for each element in the original array.

Iteration is a powerful programming concept that is used extensively in JavaScript for a wide variety of tasks, such as data processing, animation, and event handling.

### **Array Methods**

JavaScript offers a variety of array methods that allow developers to manipulate and work with arrays efficiently. Here’s an overview of some key array methods along with examples for better understanding.

**1\. \`push()\`:** The \`push()\` method adds one or more elements to the end of an array and returns the new length of the array.  
\`\`\`javascript  
let fruits \= \['apple', 'banana'\];  
fruits.push('orange');  
console.log(fruits); // Output: \['apple', 'banana', 'orange'\]  
\`\`\`  
**2\. \`pop()\`:** The \`pop()\` method removes the last element from an array and returns that element. This method changes the length of the array.  
\`\`\`javascript  
let fruits \= \['apple', 'banana', 'orange'\];  
let lastFruit \= fruits.pop();  
console.log(lastFruit); // Output: 'orange'  
console.log(fruits); // Output: \['apple', 'banana'\]  
\`\`\`  
**3\. \`shift()\`:** The \`shift()\` method removes the first element from an array and returns that element. This method also changes the length of the array.  
\`\`\`javascript  
let fruits \= \['apple', 'banana', 'orange'\];  
let firstFruit \= fruits.shift();  
console.log(firstFruit); // Output: 'apple'  
console.log(fruits); // Output: \['banana', 'orange'\]  
\`\`\`  
**4\. \`unshift()\`:** The \`unshift()\` method adds one or more elements to the beginning of an array and returns the new length of the array.  
\`\`\`javascript  
let fruits \= \['banana', 'orange'\];  
fruits.unshift('apple');  
console.log(fruits); // Output: \['apple', 'banana', 'orange'\]  
\`\`\`  
**5\. \`splice()\`:** The \`splice()\` method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.  
\`\`\`javascript  
let fruits \= \['apple', 'banana', 'orange'\];  
fruits.splice(1, 1, 'kiwi'); // Remove 1 element at index 1 and add 'kiwi'  
console.log(fruits); // Output: \['apple', 'kiwi', 'orange'\]  
\`\`\`  
**6\. \`slice()\`:** The \`slice()\` method returns a shallow copy of a portion of an array into a new array object selected from \`start\` to \`end\` (end not included).  
let fruits \= \['apple', 'banana', 'orange', 'kiwi'\];  
let citrus \= fruits.slice(1, 3);  
console.log(citrus); // Output: \['banana', 'orange'\]  
\`\`\`  
**7\. \`map()\`:** The \`map()\` method creates a new array populated with the results of calling a provided function on every element in the calling array.  
let numbers \= \[1, 2, 3\];  
let doubled \= numbers.map(num \=\> num \* 2);  
console.log(doubled); // Output: \[2, 4, 6\]  
\`\`\`  
**8\. \`filter()\`:** The \`filter()\` method creates a new array with all elements that pass the test implemented by the provided function.  
let numbers \= \[1, 2, 3, 4, 5\];  
let even \= numbers.filter(num \=\> num % 2 \=== 0);  
console.log(even); // Output: \[2, 4\]  
\`\`\`  
9\. **\`reduce()\`**: The \`reduce()\` method executes a reducer function on each element of the array, resulting in a single output value.  
let numbers \= \[1, 2, 3, 4\];  
let sum \= numbers.reduce((accumulator, current) \=\> accumulator \+ current, 0);  
console.log(sum); // Output: 10  
\`\`\`  
10\. **\`forEach()\`:** The \`forEach()\` method executes a provided function once for each array element.  
\`\`\`javascript  
let fruits \= \['apple', 'banana', 'orange'\];  
fruits.forEach((fruit, index) \=\> {  
	console.log(\`${index}: ${fruit}\`);  
});  
// Output:  
// 0: apple  
// 1: banana  
// 2: orange  
\`\`\`  
JavaScript array methods provide powerful tools for manipulating arrays, including adding, removing, transforming, and iterating over elements. These methods enhance code readability and efficiency, making it easier to manage collections of data.

* ### **What is oops**?

Object-oriented programming (OOP) is a programming paradigm that revolves around the concept of objects, which are instances of classes that encapsulate data and behaviour. In OOP, programs are designed by defining objects that interact with each other to perform tasks. The four fundamental concepts of OOP are:

1. Encapsulation:  Encapsulation is the practice of keeping related data and methods together in a single unit called a class. By using encapsulation, the data and methods are protected from outside interference and can only be accessed through the class's public interface.  
2. Inheritance: It is the process of creating a new class by inheriting the properties and methods of an existing class. The new class is known as a derived class or subclass, and the existing class is known as the base class or superclass. Inheritance promotes code reusability and helps to organise code.  
3. Polymorphism: Polymorphism is the ability of an object to take on many forms. In OOP, polymorphism is achieved through method overriding and method overloading.  
4. Abstraction: It is the process of hiding complex implementation details from the users and providing them with only the necessary information. Abstraction is achieved through abstract classes and interfaces.

Overall, OOP is a powerful tool for creating modular, reusable, and maintainable code, and it is widely used in a variety of programming languages and applications, from web development to video game design.

* ### **Multi page application?**

A multi-page application (MPA) is a type of web application that includes multiple pages with different URLs, each designed to perform a specific function or task. In an MPA, users navigate between pages by clicking on links or buttons, and the server generates a new HTML page for each request.  
Each page in an MPA may have its own layout, design, and functionality, and may require separate server-side processing and database queries. This can make MPAs more suitable for certain types of content or user interfaces, such as e-commerce websites or news portals.

* ### **Comparison operator**?

A comparison operator is a type of operator in programming that is used to compare two values or expressions and produce a Boolean result (i.e., either true or false). The most common comparison operators are:

1. Equal to (==): Compares whether two values are equal to each other.  
2. Not equal to (\!=): Compares whether two values are not equal to each other.  
3. Greater than (\>): Compares whether one value is greater than the other.  
4. Less than (\<): Compares whether one value is less than the other.  
5. Greater than or equal to (\>=): Compares whether one value is greater than or equal to the other.  
6. Less than or equal to (\<=): Compares whether one value is less than or equal to the other.

These comparison operators are commonly used in conditional statements (e.g., if statements) to test whether a certain condition is true or false, based on the comparison of two values or Expressions.

* ### **Nullish coalescing Operator.**

The ?? operator is the nullish coalescing operator, which returns its right-hand side operand when its left-hand side operand is null or undefined, and returns its left-hand side operand otherwise.  
const x \= undefined;  
const result1 \= x ?? 0 \+ 10;  
**console.log(result1);  // 10**

const y \= 100;  
const result2 \= y ?? 0 \+ 10;  
**console.log(result2);  // 100**

- ### **Logical Operators.**

In TypeScript, logical operators are used to combine or negate boolean expressions. There are three logical operators:

* AND (&&): The && operator returns true if both operands are true. Otherwise, it returns false. For example:

  let x \= 5;

  let y \= 10;

  if (x \> 0 && y \> 0\) {

      console.log("Both x and y are positive");

  }

* OR (||): The || operator returns true if at least one of the operands is true. Otherwise, it returns false. For example:

  let x \= 5;

  let y \= \-10;

  if (x \> 0 || y \> 0\) {

      console.log("Either x or y is positive");

  }

* NOT (\!): The \! operator is used to negate a boolean expression. It returns true if the expression is false, and false if the expression is true. For example:

  let x \= 5;

  let y \= 10;

  if (\!(x \> 0 && y \> 0)) {

      console.log("Either x or y is not positive");

  }

These operators can be used to combine and manipulate boolean expressions in TypeScript code.

* ### **What is an API?**

API stands for Application Programming Interface. It is a set of rules and protocols that allow different software applications to communicate with each other. APIs define how software components should interact, which data formats to use, and which functions or operations are available for use.

APIs work by exposing a set of functions or endpoints that can be called by other applications or systems. These endpoints usually accept and return data in a standardised format, such as JSON or XML, which allows applications to understand and interpret the data being sent and received.

For example, consider a weather app that uses data from a third-party weather API. The app can make a request to the API using a specific endpoint, such as "get current weather data for a specific location". The API will then process the request and return the requested data in a standardised format. The weather app can then use this data to display the current weather conditions to the user.

APIs can be public or private, depending on their intended use. Public APIs are typically available to anyone who wants to use them, while private APIs are restricted to specific users or applications. APIs are used extensively in web and mobile applications, cloud computing, and other areas of software development.

*An API (Application Programming Interface) is like a waiter at a restaurant. Just like a waiter takes your order, sends it to the kitchen, and brings your food back to you, an API takes your request for information or action, sends it to a server or application, and returns the response back to you. It allows different software applications to communicate and work together, even if they were not originally designed to do so.*

* ### **What are some features of Typescript?**

TypeScript is a superset of JavaScript that adds optional static typing and other features to JavaScript. Some of the features of TypeScript include:

- Strong Typing: TypeScript introduces static typing, which helps in detecting type-related errors at compile-time.  
- Object-Oriented Programming: TypeScript provides support for classes, interfaces, inheritance, and other object-oriented features.  
- Type Annotations: TypeScript allows developers to add type annotations to variables, function parameters, and function return types.  
- Tooling Support: TypeScript provides a rich set of tooling support, such as code completion, error highlighting, and refactoring.  
- Compatibility with JavaScript: TypeScript is a superset of JavaScript, which means that all JavaScript code is valid TypeScript code.  
- Better Error Handling: TypeScript provides better error handling compared to JavaScript. Errors are caught at compile-time, which helps in preventing runtime errors.  
- Improved Productivity: With the help of features like type checking and tooling support, TypeScript improves developer productivity and code quality.  
- ECMAScript Support: TypeScript supports the latest ECMAScript features, such as async/await, destructuring, and template literals.

* ### **What are semantic tags?**

Semantic tags in HTML are tags that convey the meaning of the content they enclose to the browser and the developer. These tags provide contextual information about the content**,** which can be used by search engines and other web applications to better understand the content of the webpage.  
Some examples of semantic tags include:

1. \<header\>: used to define the header section of a webpage.  
2. \<nav\>: used to define a block of navigation links.  
3. \<main\>: used to define the main content section of a webpage.  
4. \<section\>: used to define a section of a webpage.  
5. \<article\>: used to define an article or blog post on a webpage.  
6. \<aside\>: used to define a sidebar or additional content section.  
7. \<footer\>: used to define the footer section of a webpage.

Using semantic tags not only helps in making the code more readable and understandable but also makes it easier for search engines to crawl and index the content. It also provides better accessibility to users with screen readers or other assistive technologies, as they can better understand the structure and hierarchy of the webpage.

* What is **type inference** in typescript?

Type inference allows the compiler to automatically infer the types of variables, functions, and other entities based on the context in which they are used.

* ### **HTML \<table\> tag?**

The HTML table tag \<table\> is used to define a table in a web page. It is a container element that is used to hold tabular data, such as a list of items with multiple properties. The \<table\> element is typically used in combination with other table-related elements like \<tr\> (table row), \<th\> (table header cell), and \<td\> (table data cell).  
Here's an example of a basic HTML table structure:  
\<table\>  
 \<tr\>  
  \<th\>Header 1\</th\>  
  \<th\>Header 2\</th\>  
 \</tr\>   
 \<tr\>   
  \<td\>Data 1\</td\>  
  \<td\>Data 2\</td\>   
 \</tr\>  
 \<tr\>  
  \<td\>Data 3\</td\>  
  \<td\>Data 4\</td\>   
 \</tr\>  
\</table\>  
In this example, we have a table with two columns and three rows. The first row is a header row, with two header cells (\<th\>) labelled "Header 1" and "Header 2". The remaining rows contain data cells (\<td\>) with corresponding data values.  
HTML tables can be further customised using CSS styles to control the appearance and layout of the table, including things like cell spacing, border styles, and column widths.  
Regenerate response

* ### What is **\<noscript\>** tag?

The \<noscript\> tag in HTML is used to provide an alternative content for users who have disabled JavaScript in their web browser or have a browser that does not support JavaScript.

When a web page contains a \<noscript\> tag, the content within the tag is displayed to users who have JavaScript disabled, instead of the JavaScript-powered content that is normally displayed.

This tag can be useful for providing a fallback option or alternative content for users who cannot or choose not to use JavaScript. For example, if a website has a form that requires JavaScript to work properly, the \<noscript\> tag can be used to display a message to users who have JavaScript disabled, instructing them to enable JavaScript or use a different browser to access the form.

* ### **What are var, let, and const keywords in typescript?**

In TypeScript, var, let, and const are keywords used to declare variables. These keywords have different scoping rules and behaviour, as described below:

* var: The var keyword is used to declare a variable with function-level scope. Variables declared with var can be accessed within the function in which they are defined or in any nested functions. However, they are not block-scoped, which means that they can also be accessed outside of the block in which they are defined.  
* let: The let keyword is used to declare a block-scoped variable. Variables declared with let are only accessible within the block in which they are defined, including nested blocks. This keyword is often preferred over var because it allows for more predictable and maintainable code.  
* const: The const keyword is used to declare a constant variable. Constants cannot be reassigned once they are defined. They have the same block-scoping rules as let variables, meaning that they are only accessible within the block in which they are defined. Constants are often used to define values that should never change, such as mathematical constants or configuration values.

Overall, the let and const keywords provide a safer and more predictable way of defining variables in TypeScript compared to the traditional var keyword. They help prevent common programming errors related to variable scoping and reassignment.

* ### What is **Promise** in javascript?

In JavaScript, a Promise is an object that represents a value that may not be available yet, but will be at some point in the future. Promises provide a way to handle asynchronous operations, such as fetching data from an API or reading a file, without blocking the main thread of execution.  
A Promise has three states:

1. Pending: The initial state when the promise is created and the value is not yet available.  
2. Resolved: The state when the value is available and the promise has been successfully resolved.  
3. Rejected: The state when an error occurs and the promise cannot be resolved.

The Promise object takes a function as its argument, which is called the "executor" function. This function takes two arguments: a "resolve" function and a "reject" function. When the promise is resolved successfully, the "resolve" function is called with the value as its argument. When an error occurs, the "reject" function is called with the error object as its argument. Example:  
const myPromise \= new Promise((resolve, reject) \=\> {  
  // perform an asynchronous operation, such as fetching data from an API  
  fetch('https://example.com/data')  
    .then(response \=\> response.json())  
    .then(data \=\> resolve(data))  
    .catch(error \=\> reject(error))  
});  
A JavaScript Promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value.  
Think of it as a guarantee that a task will be completed at some point in the future, even if you don't know exactly when. When you create a Promise, you can attach functions to it that will be called when the Promise is resolved (successfully completed) or rejected (failed).  
Promises are commonly used in JavaScript for tasks like fetching data from a server, waiting for user input, or performing animations.

### **What are asynchronous operations?**

Asynchronous operations are a way of performing tasks where the execution does not block the program until the task is complete. In other words, the program can continue running while the task is being executed in the background.  
In contrast to synchronous operations, where the program waits for the operation to complete before proceeding to the next task, asynchronous operations allow the program to execute other tasks concurrently while waiting for the asynchronous task to complete.  
This approach is commonly used in programming to improve the efficiency of applications and user interfaces, as it allows for the program to remain responsive to user input even when there are long-running tasks being executed in the background. Asynchronous operations are commonly used in web development, server-side programming, and other areas of software development.

* ### What are **access modifiers** in Typescript?

Access modifiers in TypeScript are keywords that are used to control the visibility and accessibility of class members (properties and methods) from outside the class. TypeScript supports three access modifiers:

1. Public: Members declared as public are accessible from anywhere, both inside and outside the class.  
2. Private: Members declared as private are only accessible from within the class. They cannot be accessed from outside the class, including derived classes.  
3. Protected: Members declared as protected are accessible from within the class and its derived classes. They cannot be accessed from outside the class hierarchy.

To specify an access modifier in TypeScript, you can prefix the member declaration with one of the access modifier keywords: public, private, or protected. Here's an example:

class Car {  
  public model: string;  
  private engine: string;  
  protected speed: number;  
    
  constructor(model: string, engine: string, speed: number){  
    this.model \= model;  
    this.engine \= engine;  
    this.speed \= speed;  
  }  
    
  public accelerate() {  
    console.log(\`Accelerating at ${this.speed} km/h\`);  
  }  
    
  private turnOn() {  
    console.log(\`Turning on the ${this.engine} engine\`);  
  }  
    
  protected stop() {  
    console.log(\`Stopping the car\`);  
  }  
}

const myCar \= new Car("Ford Mustang", "V8", 200);  
myCar.model \= "Chevrolet Camaro"; // OK  
// myCar.engine \= "V6"; // Error: private member  
// myCar.speed \= 0; // Error: protected member  
myCar.accelerate(); // OK  
// myCar.turnOn(); // Error: private member  
// myCar.stop(); // Error: protected member

* ### What is a **Recursion function** in Javascript?

In JavaScript, a recursion function is a function that calls itself during its execution. This allows a problem to be solved by breaking it down into smaller and smaller sub-problems until the smallest sub-problems can be easily solved.  
Here is an example of a simple recursive function in JavaScript that calculates the factorial of a number:  
function factorial(num) {  
  if (num \<= 1\) {  
    return 1;  
  } else {  
    return num \* factorial(num \- 1);  
  }  
}

console.log(factorial(5)); // Output: 120  
In this example, the factorial() function takes a number as input and returns the factorial of that number. If the input number is less than or equal to 1, the function returns 1\. Otherwise, it multiplies the input number by the result of calling factorial() with the input number decremented by 1\.

When factorial() is called with the argument 5, it computes the factorial of 5 as 5 \* 4 \* 3 \* 2 \* 1, which equals 120\. The function achieves this by recursively calling itself with decreasing values of num until it reaches the base case of num \<= 1, at which point it returns 1 and the recursion ends.

* ### What is a **Call by value** and **Call by reference**?

In JavaScript, primitive data types are passed by value and non-primitive data types are passed by reference.

* ### What is **NaN property** in Javascript?

In JavaScript, \`NaN\` stands for "Not a Number". It is a special value that represents an unrepresentable or undefined value resulting from an invalid arithmetic operation, such as trying to perform a mathematical operation on a non-numeric value or dividing by zero.  
For example, if you try to perform a mathematical operation on a non-numeric string or undefined variable, the result will be \`NaN\`. Here's an example:  
const result \= 'hello' / 2;  
console.log(result); // Output: NaN

It is important to note that \`NaN\` is a value of the \`number\` type in JavaScript, and \`NaN\` is not equal to any value, including itself. So, you cannot use the \`==\` or \`===\` operators to check if a value is \`NaN\`. Instead, you can use the \`isNaN()\` function, which returns \`true\` if the argument is \`NaN\` and \`false\` otherwise. Here's an example:  
const result \= 'hello' / 2;  
console.log(isNaN(result)); // Output: true

* ### What are the **uses of Undefined?**

In TypeScript, undefined is a data type that represents the absence of a value. It can be assigned to any variable that has not been assigned a value, or a function that doesn't return anything.  
Here are some of the common uses of undefined in TypeScript:

* Variable initialization: If a variable is declared but not initialised, its value will be undefined by default. This is useful when you want to declare a variable but don't know its value yet.  
* Function parameters and return types: When a function doesn't return a value, its return type is usually set to undefined. Similarly, if a function parameter is optional, its type can be set to undefined.  
* Checking for missing values: You can use the typeof operator to check if a variable has a value or not. If its type is undefined, it means that the variable is missing a value.  
* Error handling: When an error occurs in your program, you can set a variable to undefined to indicate that something went wrong. This can be useful for debugging purposes, as you can check if a variable is undefined to see if there was an error in your code.

Overall, undefined in TypeScript can be used to represent the absence of a value or to check for missing values, and is a common type used in the language.

* ### What is an **Enum**?

In TypeScript, an enum is a way to define a collection of related constants with friendly names. Enums are essentially a set of named values that are assigned numeric values by default.

Here's an example of an enum in TypeScript:  
enum Colour {   
Red,   
Green,   
Blue   
}  
In this example, we've defined an enum called Color with three named values: Red, Green, and Blue. By default, these values are assigned numeric values starting from 0\. So Red is 0, Green is 1, and Blue is 2\.  
Enums can also be assigned specific numeric values if needed, like this:

enum Color {   
Red \= 1,   
Green \= 2,   
Blue \= 4   
}  
In this example, we've assigned specific numeric values to each named value. So Red is 1, Green is 2, and Blue is 4\.

Enums in TypeScript can be useful for creating a set of predefined values that can be used throughout your application. They can also make your code more readable and maintainable by using friendly names instead of numeric values.  
You can access the values of an enum using dot notation, like this:  
const red \= Color.Red;  
You can also get the name of an enum value from its numeric value using the reverse mapping feature, like this:  
const colorName \= Color\[1\];  // returns 'Red'

Overall, enums in TypeScript provide a way to define a set of related constants with friendly names and numeric values.

* ### What is **DOM**?

DOM stands for Document Object Model, which is a programming interface for web documents. It defines the way in which web pages are structured and manipulated by scripts or programming languages such as JavaScript.

The DOM represents the structure of an HTML or XML document as a hierarchical tree of nodes. Each node in the tree corresponds to an element, attribute, or piece of text in the document, and can be manipulated or modified by scripts.

The DOM provides a way for scripts to access and manipulate the content and structure of web pages dynamically, allowing developers to create interactive and dynamic web applications. For example, JavaScript code can be used to modify the text content of an HTML element, change the attributes of an element, or add or remove elements from the page.

In addition to providing a way to manipulate the content of web pages, the DOM also provides a set of events that can be used to trigger scripts in response to user actions or other events, such as clicking a button or loading a new page.

Overall, the DOM is a critical component of modern web development and is essential for creating dynamic, interactive, and responsive web applications.

* ### **What is an image map?**

An image map is a graphic image that has clickable areas, called "hotspots," that allow the user to interact with the image by clicking on different regions. These hotspots are typically defined by invisible shapes or coordinates overlaid on top of the image.  
Image maps are commonly used in web design to create interactive graphics that allow users to explore and navigate different parts of an image. For example, a map of a city might have hotspots over each landmark, allowing users to click on the landmark to learn more about it or to get directions to that location.  
Image maps can be created using HTML or other web design tools. They can be static, with predefined hotspots, or dynamic, with hotspots that are generated based on user input or other variables.

* **What is a hyperlink?**

A hyperlink, also known as a link, is a clickable element in a document or webpage that redirects the user to another location, which could be a different webpage, a different section of the same page, or even a different file or resource altogether.

Hyperlinks are typically displayed as underlined or coloured text, but they can also be represented as images, buttons, or other elements that the user can click on to follow the link. When a user clicks on a hyperlink, the browser navigates to the location specified in the link, either by loading a new page or by scrolling to a specific part of the current page.

Hyperlinks are an essential component of the web, enabling users to navigate between different pages and resources and to access a vast range of information quickly and easily. They are created using HTML or other web design tools, and can be styled and customised to match the design and branding of the page.

* ### What is the **Never data type?**

In TypeScript, "never" is a special type that represents a value that can never occur. It is typically used to indicate values or scenarios that are impossible or should never occur. "never" is commonly used as a return type for functions that never return, such as functions that always throw an error or enter an infinite loop.. It can also be used as a type for variables or function parameters that are not expected to have a value.

* ### What is an **Unknown data type**?

In TypeScript, the unknown type is a type that represents values that could be of any type. This type was introduced in TypeScript 3.0 as a way to represent values whose type is not known at compile-time or that could come from dynamic sources such as user input or external APIs.

The unknown type is similar to the ANY type, but it provides more type safety because it forces the developer to perform type-checking before using the value. In other words, you cannot perform any operations on an unknown value until you have checked its type or casted it to a more specific type. Here's an example:  
function processData(data: unknown) {  
  if (typeof data \=== "string") {  
    console.log(data.toUpperCase());  
  } else if (typeof data \=== "number") {  
    console.log(data \* 2);  
  }  
}

processData("hello"); // Output: HELLO  
processData(5); // Output: 10  
processData(true); // Compilation error: Type 'boolean' is not assignable to type 'unknown'.

* ### **What is Javascript?**

JavaScript is a programming language used primarily for creating dynamic, interactive web pages and applications.

JavaScript is a client-side scripting language, which means that it runs directly in a user's web browser, rather than on a web server. This allows developers to create dynamic web pages that can respond to user interactions without the need for a page refresh.

JavaScript is also used in server-side programming, such as with Node.js, which allows developers to use JavaScript to create server-side applications as well. It has a syntax similar to other programming languages such as Java, C++, and Python, but also has unique features and capabilities, such as first-class functions and closures, which make it a powerful and flexible language.

* ### **Client side and Server side javascript?**

JavaScript is a programming language that can be used on both the client side and server side of web development. However, there are some key differences between client-side and server-side JavaScript.  
Client-side JavaScript is executed in the web browser of the user, and is responsible for creating dynamic user interfaces and performing client-side validation. It is often used for enhancing the user experience, such as creating animations or interactive forms, and can be used to communicate with a server-side API.  
Server-side JavaScript, on the other hand, is executed on the server-side of a web application and is responsible for processing data and generating HTML or other content to be sent to the client-side for display. It is often used for server-side validation, database interactions, and handling user authentication.  
Node.js is a popular runtime environment that allows JavaScript to be used on the server-side. It allows developers to create highly scalable and efficient server-side applications using JavaScript, which can help reduce development time and improve the overall performance of web applications.  
In summary, client-side JavaScript is used for enhancing the user experience on the web, while server-side JavaScript is used for processing data and generating content on the server-side of a web application.

* ### D/f b/w **scripting language and programming language**?

Scripting languages and programming languages are both used for software development, but they have some key differences:

- Execution: Scripting languages are interpreted at runtime, while programming languages are compiled before execution.  
- Scope: Scripting languages are typically used for smaller, simpler tasks and have a narrower scope, while programming languages can be used for more complex tasks and have a broader scope.  
- Syntax: Scripting languages typically have a simpler, more concise syntax, while programming languages can have more complex syntax that allows for greater flexibility and control.  
- Speed: Because scripting languages are interpreted at runtime, they are generally slower than compiled programming languages. However, this gap is narrowing with the use of just-in-time (JIT) compilation in some scripting languages.  
- Purpose: Scripting languages are often used for tasks such as automation, web development, and system administration, while programming languages are used for developing more complex software applications, such as operating systems, databases, and video games.

Examples of scripting languages include JavaScript, Python, and Ruby, while examples of programming languages include C++, Java, and Python (which can be used for both scripting and programming).

* ### What is a **switch case**?

In JavaScript, a switch statement is a conditional statement used to compare a variable or expression to multiple possible values and execute different blocks of code depending on the value of the variable or expression.   
The syntax for a switch statement is as follows:

switch (expression) {  
  case value1:  
    // code to be executed if expression matches value1  
    break;  
  case value2:  
    // code to be executed if expression matches value2  
    break;  
  case value3:  
    // code to be executed if expression matches value3  
    break;  
  default:  
    // code to be executed if expression doesn't match any of the above cases  
}  
The expression is evaluated and compared to each case value in turn. If the expression matches a case value, the code block following that case is executed. The \`break\` keyword is used to exit the switch statement and prevent the execution of any subsequent cases. The \`default\` case is optional and is executed if none of the cases match the expression.

**Why do we use inheritance?**  
There are several reasons why inheritance is used in programming:

- Code reusability: Inheritance allows you to reuse code that already exists in a superclass, rather than having to write the same code multiple times in different classes.  
- Modularity: By dividing functionality into separate classes, each class can be developed and tested independently. This makes the code easier to maintain and modify.  
- Polymorphism: Polymorphism allows different classes to be used interchangeably, even if they have different implementations. This makes it easier to write generic code that can work with a variety of objects.  
- Code organisation: Inheritance provides a way to organise code by creating a hierarchy of classes that share common properties and behaviours. This makes the code more understandable and easier to navigate.

### **Can we avoid hoisting?**

Hoisting is a default behaviour in JavaScript where variable declarations and function declarations are moved to the top of their respective scopes at compile time, regardless of where they were actually declared in the code.

While it can be convenient to use hoisting in some cases, it can also lead to bugs and unexpected behaviour in large and complex codebases. Fortunately, there are several techniques that can be used to avoid hoisting in JavaScript:

- **Use let and const instead of var**: The let and const keywords were introduced in ES6 and have block scope instead of function scope, so they do not suffer from hoisting. It's generally considered a best practice to use let and const instead of var whenever possible.  
- **Use strict mode**: Enabling strict mode by adding the 'use strict' directive at the beginning of a script or function will disable hoisting for variable and function declarations that violate strict mode rules. This can help catch errors and improve code reliability.  
- **Declare all variables at the top of the scope**: While this doesn't completely eliminate hoisting, it can help make the code more predictable and easier to understand. By declaring all variables at the top of their respective scopes, developers can ensure that variable declarations are always processed before they are used.  
- **Use function expressions instead of function declarations**: Function expressions are not subject to hoisting, so they can be used to avoid issues with function declarations being unexpectedly moved to the top of their scope. However, this approach can make the code less readable and more difficult to maintain.

Overall, while hoisting can be a useful feature in some cases, it's generally best to avoid it as much as possible to improve code reliability and reduce the likelihood of bugs.

- ### **Different string methods.**

.slice(), .substring(), .split(), .includes(), .trim(), .concat(), .replaceAll(), .lastIndexOf(), .toUpperCase(), .toLowerCase(), .indexOf(), 

- ### **Can we pass an array in a rest parameter?**

Yes, we can pass an array as a rest parameter to a function. In JavaScript and TypeScript, the rest parameter syntax allows us to represent an indefinite number of arguments as an array. This can be useful when we want to pass multiple arguments to a function, but we don't know in advance how many arguments will be passed.

Here is an example of using an array as a rest parameter in a function:  
function sum(...numbers: number\[\]) {  
  return numbers.reduce((total, num) \=\> total \+ num, 0);  
}

let result \= sum(1, 2, 3, 4, 5);  
console.log(result); // Output: 15

let numbers \= \[1, 2, 3, 4, 5\];  
result \= sum(...numbers);  
console.log(result); // Output: 15  
In the above example, the sum() function uses the rest parameter syntax to accept any number of arguments as an array. We can pass an array to this function by using the spread syntax (...) to spread the elements of the array into individual arguments.

In the second example, we pass an array of numbers to the sum() function using the spread syntax. This will effectively pass the elements of the numbers array as individual arguments to the sum() function.

So, in summary, we can use an array as a rest parameter in a function by using the spread syntax to spread the elements of the array into individual arguments.

- ### **Try and catch** function?

In JavaScript, the try and catch statements are used together to handle runtime errors that may occur in a block of code. The try statement is used to enclose the code that may cause an error, while the catch statement is used to handle the error and execute an alternative block of code.  
Here's an example:  
try {  
  // Code that may cause an error  
  let x \= y \+ 1;  
} catch(error) {  
  // Code to handle the error  
  console.log('An error occurred: ' \+ error);  
}  
In this example, the try statement encloses the code that may cause an error, which in this case is trying to add 1 to an undefined variable y. If an error occurs, the catch statement handles the error and logs a message to the console.  
The catch statement takes an argument, commonly named error, that represents the error object thrown by the try statement. This object contains information about the type of error that occurred, such as the name and message of the error.  
Note that if an error occurs in the try block and there is no corresponding catch block to handle it, the error will propagate up the call stack until it is caught by a higher-level catch block or until it reaches the top level of the program, where it may cause the program to crash.

* ### **Types of loops.**

In TypeScript, you can use the following types of loops:

**for loop**: This is the most commonly used loop in TypeScript, which is used to iterate over a range of values. The syntax of the for loop is as follows:

for (initialization; condition; increment/decrement) {  
  // code block to be executed  
}  
**while loop**: The while loop is used to execute a block of code repeatedly as long as a specified condition is true. The syntax of the while loop is as follows:

while (condition) {  
  // code block to be executed  
}  
**do-while loop**: This loop is similar to the while loop, but the code block is executed at least once before the condition is checked. The syntax of the do-while loop is as follows:

do {  
  // code block to be executed  
} while (condition);  
**for-in loop**: This loop is used to iterate over the properties of an object. The syntax of the for-in loop is as follows:

for (variable in object) {  
  // code block to be executed  
}  
**for-of loop**: This loop is used to iterate over the values of an iterable object, such as an array or a string. The syntax of the for-of loop is as follows:

for (variable of iterable) {  
  // code block to be executed  
}  
Each of these loops has its own use cases, and choosing the right loop for a particular situation can help make your code more efficient and easier to read.

* ### **How does for-in loop work?**

In JavaScript, the \`for...in\` loop is used to iterate over the properties of an object. It allows you to loop through all enumerable properties of an object, including both its own properties and inherited ones.

The general syntax of the \`for...in\` loop is as follows:  
\`\`\`javascript  
for (variable in object) {  
  // code to be executed  
}  
\`\`\`  
Here's how it works:

1. The \`variable\` is a variable that will hold the name of each property in each iteration. It represents the current property key being iterated.

2. The \`object\` is the object you want to iterate over. It can be any object, including built-in objects like arrays, as well as user-defined objects.

3. Inside the loop, you can write the code that will be executed for each property in the object. This code will typically involve accessing or manipulating the values associated with the current property.

Here's an example that demonstrates the usage of \`for...in\` loop:  
\`\`\`javascript  
const person \= {  
  name: 'John',  
  age: 30,  
  occupation: 'Developer'  
};

for (let prop in person) {  
  console.log(prop \+ ': ' \+ person\[prop\]);  
}  
\`\`\`  
In this example, the \`for...in\` loop iterates over each property of the \`person\` object. In each iteration, the \`prop\` variable holds the name of the current property. We can use this name to access the corresponding value of the property using bracket notation (\`person\[prop\]\`). The code inside the loop logs the property name and its value to the console.

Output:  
\`\`\`  
name: John  
age: 30  
occupation: Developer  
\`\`\`

It's important to note that the order in which the properties are iterated is not guaranteed and may vary between different JavaScript engines. Also, the \`for...in\` loop only iterates over enumerable properties, and it will not iterate over properties with the \`enumerable\` attribute set to \`false\` or non-enumerable properties of the prototype chain. To iterate over the elements of an array or an array-like object, the \`for...of\` loop is usually preferred.

* ### **Better way to loop over objects?**

In TypeScript, the \`for...in\` loop can be used to iterate over the properties of an object, similar to JavaScript. However, since TypeScript is a typed superset of JavaScript, it provides additional features and constructs that can make object iteration more type-safe and expressive. While \`for...in\` loop can be used in TypeScript, there are alternative and often preferred methods for object iteration:

1.  \*\*\`Object.keys()\`\*\*: The \`Object.keys()\` method returns an array containing the enumerable property names of an object. It allows you to iterate over an object's keys more straightforwardly and is commonly used in TypeScript.  
      \`\`\`typescript  
      const obj \= { a: 1, b: 2, c: 3 };  
     
      Object.keys(obj).forEach(key \=\> {  
        console.log(key \+ ': ' \+ obj\[key\]);  
      });  
      \`\`\`  
     
      Output:  
      \`\`\`  
      a: 1  
      b: 2  
      c: 3  
      \`\`\`

   \`Object.keys()\` returns an array of strings, representing the enumerable property names of the object. You can then use array iteration methods like \`forEach()\` or traditional \`for\` loops to loop over the keys and access the corresponding values.

2.  \*\*\`Object.entries()\`\*\*: The \`Object.entries()\` method returns an array of key-value pairs for each enumerable property in an object. It allows you to iterate over both the keys and values simultaneously.

      \`\`\`typescript

      const obj \= { a: 1, b: 2, c: 3 };

   

      Object.entries(obj).forEach((\[key, value\]) \=\> {

        console.log(key \+ ': ' \+ value);

      });

      \`\`\`

   

      Output:

      \`\`\`

      a: 1

      b: 2

      c: 3

      \`\`\`

   \`Object.entries()\` returns an array of arrays, where each inner array contains a key-value pair. Destructuring assignment is used in the example to assign the key and value variables from each inner array.

3.  \*\*\`for...of\` loop with \`Object.entries()\`\*\*: TypeScript supports the \`for...of\` loop, which can be used in combination with \`Object.entries()\` to iterate over the key-value pairs of an object.

      \`\`\`typescript

      const obj \= { a: 1, b: 2, c: 3 };

   

      for (const \[key, value\] of Object.entries(obj)) {

        console.log(key \+ ': ' \+ value);

      }

      \`\`\`

   

      Output:

      \`\`\`

      a: 1

      b: 2

      c: 3

      \`\`\`

The \`for...of\` loop provides a more concise syntax for iterating over iterable objects, such as arrays or objects with a \`\[Symbol.iterator\]\` method. In this case, \`Object.entries()\` returns an iterable that produces key-value pairs, which can be directly looped over using \`for...of\`.

Using methods like \`Object.keys()\`, \`Object.entries()\`, or \`for...of\` loop with \`Object.entries()\` can provide better type safety and clarity in TypeScript code compared to the generic \`for...in\` loop. These methods explicitly operate on the properties of an object and allow you to access the keys and values more easily.

* ### **How to iterate over an array of objects.**

Yes, the methods mentioned (\`Object.keys()\`, \`Object.entries()\`, and \`for...of\` loop with \`Object.entries()\`) can also be used to iterate over an array of objects in TypeScript.

Here's an example that demonstrates iterating over an array of objects using these methods:  
\`\`\`typescript  
const arrayOfObjects \= \[  
  { name: 'John', age: 30 },  
  { name: 'Alice', age: 25 },  
  { name: 'Bob', age: 35 }  
\];

// Using Object.keys()  
arrayOfObjects.forEach(obj \=\> {  
  Object.keys(obj).forEach(key \=\> {  
    console.log(key \+ ': ' \+ obj\[key\]);  
  });  
});

// Using Object.entries()  
arrayOfObjects.forEach(obj \=\> {  
  Object.entries(obj).forEach((\[key, value\]) \=\> {  
    console.log(key \+ ': ' \+ value);  
  });  
});

// Using for...of loop with Object.entries()  
for (const obj of arrayOfObjects) {  
  for (const \[key, value\] of Object.entries(obj)) {  
    console.log(key \+ ': ' \+ value);  
  }  
}  
\`\`\`

Output:  
\`\`\`  
name: John  
age: 30  
name: Alice  
age: 25  
name: Bob  
age: 35  
\`\`\`

In this example, \`arrayOfObjects\` is an array containing three objects. The methods \`Object.keys()\`, \`Object.entries()\`, and the \`for...of\` loop with \`Object.entries()\` are used to iterate over each object in the array. Inside the nested iterations, the properties of each object are accessed and logged to the console.

These methods provide a convenient way to iterate over an array of objects and access their properties. Each iteration allows you to work with one object at a time and perform operations based on the object's properties.

* ### **What are Ternary Operators?**

The ternary operator, also known as the conditional operator, is a shorthand way of writing an if-else statement in JavaScript. The syntax of the ternary operator is as follows:  
condition ? expression1 : expression2

If the condition is true, \`expression1\` is evaluated and returned. If the condition is false, \`expression2\` is evaluated and returned.

Here's an example that uses the ternary operator to assign a value to a variable:

let x \= 10;  
let y \= x \> 5 ? "x is greater than 5" : "x is less than or equal to 5";  
console.log(y); // "x is greater than 5"

In this example, the condition \`x \> 5\` evaluates to true, so \`y\` is assigned the value \`"x is greater than 5"\`. If the condition had been false, \`y\` would have been assigned the value \`"x is less than or equal to 5"\`.

* ### **What are the types of arrays in javascript?**

In JavaScript, there are two main types of arrays:  
Indexed arrays: This is the most common type of array in JavaScript. It is also known as a numeric array or an array with numeric indexes. In this type of array, each element is assigned a unique index starting from 0, and the elements can be of any data type. Here's an example of an indexed array:  
let fruits \= \[  
"apple","banana","orange"  
\];  
Associative arrays: This type of array is also known as a hash or a dictionary. In this type of array, elements are stored in key-value pairs, where the key is a string and the value can be of any data type. Here's an example of an associative array:

let person \= {  
"name":"John",  
"age": 30,  
"city":"New York"  
};  
Note that JavaScript doesn't have a separate data type for associative arrays. Instead, they are implemented using objects, which are a fundamental data type in JavaScript. However, it's important to note that the order of elements in an associative array is not guaranteed, unlike in an indexed array.

* ### **What is an object in oops?**

In object-oriented programming (OOP), an object is an instance of a class that encapsulates data and behaviour. It can be thought of as a self-contained entity that has state (data) and behaviour (methods or functions) that operate on that state.

An object has properties, which are the data members or variables that store the state of the object, and methods, which are the functions that define the behaviour of the object. The properties and methods of an object are accessed using the dot notation in most OOP languages.

* ### **What are the uses of objects in Typescript?**

In TypeScript, objects are an essential data type and can be used for a wide range of purposes. Here are some of the most common uses of objects in TypeScript:

- Storing and manipulating data: Objects can be used to store and manipulate data in a structured way. For example, you can create an object to represent a person with properties like name, age, and address.  
- Creating complex data structures: Objects can be used to create more complex data structures like arrays, sets, and maps.  
- Creating classes: Objects are the basis of creating classes in TypeScript.  
- Passing data between functions: Objects can be used to pass data between functions. For example, you can create an object that represents a user's input data and pass it to a function that processes that data.  
- Implementing interfaces: Objects are used to implement interfaces in TypeScript. An interface is a contract that defines a set of properties and methods that an object must implement.  
- Working with APIs: Objects are commonly used when working with APIs. APIs often return data in the form of objects, and you can use objects to send data to APIs as well.

Overall, objects are an essential data type in TypeScript that can be used for a variety of purposes, from storing data to creating complex data structures and classes. 

* ### **Define polymorphism in OOPs.**

Polymorphism is one of the fundamental concepts in Object-Oriented Programming (OOPs) that allows objects of different classes to be treated as if they were objects of the same class. The word "polymorphism" comes from the Greek words "poly" meaning "many" and "morph" meaning "form," so it refers to the ability of an object to take on many forms.

In OOPs, there are two types of polymorphism: compile-time polymorphism (also known as method overloading) and runtime polymorphism (also known as method overriding).  
Compile-time polymorphism occurs when there are multiple methods with the same name but different parameters in a class, and the appropriate method to be called is determined at compile time based on the number and types of arguments passed to the method.

Example:  
class Calculator {  
  add(x: number, y: number): number {  
    return x \+ y;  
  }  
  add(x: number, y: number, z: number): number {  
    return x \+ y \+ z;  
  }  
}

let calculator \= new Calculator();  
console.log(calculator.add(1, 2)); // Output: 3  
console.log(calculator.add(1, 2, 3)); // Output: 6

Runtime polymorphism(also known as method overriding) occurs when a subclass provides its own implementation of a method that is already defined in its superclass, and the appropriate method to be called is determined at runtime based on the actual type of the object.  
Example:  
class Animal {  
  makeSound() {  
    console.log("The animal makes a sound");  
  }  
}

class Cat extends Animal {  
  makeSound() {  
    console.log("Meow");  
  }  
}

let animal: Animal \= new Cat();  
animal.makeSound(); // Output: Meow

In both types of polymorphism, the goal is to provide a more flexible and extensible code by allowing different objects to be treated as if they were the same type of object. Polymorphism is a powerful concept that enables us to write code that is reusable, modular, and easier to maintain.

* ### **What is readonly in html?**

In HTML, the \`readonly\` attribute is used to create an input field that cannot be edited by the user, but can still be submitted with a form. This attribute is commonly used with text input fields, such as \`input type="text"\`, \`textarea\`, and \`select\`.

To use \`readonly\` in HTML, you simply need to add the attribute to the relevant HTML tag. Here's an example:

\<input type="text" name="username" value="JohnDoe" readonly\>  
In this example, the \`readonly\` attribute is added to the \`input\` tag, which creates a text input field that contains the value "JohnDoe" and cannot be edited by the user. When the form containing this input field is submitted, the value "JohnDoe" will be included in the form data.

Note that the \`readonly\` attribute only prevents the user from editing the value of the input field. It does not prevent the user from selecting or copying the text in the field. If you want to create an input field that cannot be edited or selected at all, you can use the \`disabled\` attribute instead.

* ### **What are higher-order functions?**

In programming, a higher-order function is a function that takes one or more functions as arguments, or returns a function as its result. In other words, it is a function that operates on other functions.  
Higher-order functions are a fundamental concept in functional programming, and they provide a powerful way to write modular, reusable, and concise code. They can be used for a variety of purposes, such as transforming data, filtering collections, and handling asynchronous operations.

* ### **Hoisting in javascript.**

Hoisting is the default behaviour of javascript where all the variable and function declarations are moved on top.

* ### **What is a unary operator in javascript?**

In JavaScript, a unary operator is an operator that takes a single operand and performs an operation on it.  
There are several unary operators in JavaScript, including:

- The positive (+) operator, which converts its operand to a number.  
- The negative (-) operator, which negates its operand.  
- The logical not (\!) operator, which converts its operand to a boolean value and negates it (i.e., if the operand is true, the result is false; if the operand is false, the result is true).  
- The typeof operator, which returns a string that indicates the type of its operand.  
- The void operator, which discards the result of its operand and returns undefined.

* ### **BoxModel?**

The box model is a fundamental concept in CSS that defines how elements are rendered and laid out on a web page. It consists of four components: content, padding, border, and margin.

The content area is where the actual content of an element is displayed. The padding is the space between the content and the border. The border is the line that surrounds the padding and content. The margin is the space between the border and the next adjacent element.

* ### **Position**

The position property in CSS is used to control the positioning of an element on a web page.  
There are five values that the position property can take:

- static: This is the default value for all HTML elements. An element with position: static is positioned according to the normal flow of the page, and cannot be moved using the top, bottom, left, or right properties.  
- relative: An element with position: relative is positioned relative to its normal position in the flow of the page. It can be moved using the top, bottom, left, or right properties. However, the original space occupied by the element is still reserved, and other elements will not fill the space.  
- absolute: An element with position: absolute is positioned relative to its nearest positioned ancestor element. If there is no positioned ancestor, it is positioned relative to the initial containing block (usually the viewport). It can be moved using the top, bottom, left, or right properties. The space occupied by the element is removed from the normal flow of the page, and other elements will fill the space.  
- fixed: An element with position: fixed is positioned relative to the viewport, and does not move when the page is scrolled. It can be moved using the top, bottom, left, or right properties. The space occupied by the element is removed from the normal flow of the page, and other elements will fill the space.  
- sticky: An element with position: sticky is positioned based on the user's scroll position. It is similar to position: relative, except that it "sticks" to the top or bottom of its containing element when the user scrolls past it. It can be moved using the top, bottom, left, or right properties.

* ### **Z-index**

The z-index property in CSS is used to control the vertical stacking order of positioned elements on a web page.  
When elements are positioned using CSS, they can overlap with other elements. The z-index property determines which elements appear in front of or behind other elements.  
The z-index property takes an integer value, with higher values indicating that an element should appear in front of elements with lower values. The default value of z-index is 0\.

* ### **Media query**

Media queries allow developers to create responsive designs that adapt to different screen sizes and orientations, and to apply specific styles to different types of devices, such as smartphones, tablets, laptops, and desktops.

@media (max-width: 600px) {  
  body {  
    font-size: 14px;  
    line-height: 1.5;  
  }  
}  
/\* apply styles to the body element when the screen width is less than 600px \*/

* ### **Display**

The display property in CSS is used to control how an HTML element is displayed on a web page. It determines whether the element is treated as a block-level or an inline-level element, or whether it is removed from the flow of the page altogether.  
The display property can take several values:

- none: The element is completely removed from the flow of the page and is not visible.  
- block: The element is displayed as a block-level element, taking up the full width of its parent container and creating a new line after it.  
- inline: The element is displayed as an inline-level element, flowing with the surrounding text and taking up only as much width as necessary.  
- inline-block: The element is displayed as an inline-level element, but behaves like a block-level element in terms of width and height.  
- table: The element is displayed as a table.  
- flex: The element is displayed as a flex container, allowing you to use the flexbox layout.  
- grid: The element is displayed as a grid container, allowing you to use the CSS grid layout.

### **display none vs visibility hidden in CSS**

Both display:none and visibility:hidden are CSS properties used to hide elements from the user interface, but they work in different ways:

* display:none: This property removes the element from the document flow and the space it occupies, making it completely invisible and inaccessible to the user. The element is not rendered, and any child elements are also not rendered. This means that the element is not available to screen readers and search engines.  
* visibility:hidden: This property makes the element invisible but still takes up space in the document flow. The element is not rendered, but the space it occupies is still reserved, so other elements will still be affected by its presence. This means that the element is still accessible to screen readers and search engines.

In summary, display:none completely removes the element from the page, whereas visibility:hidden hides the element but still reserves space for it. Which one you use depends on your specific use case.

* ### **Flexbox**

Flexbox (short for "Flexible Box Layout") is a layout model in CSS that allows you to create flexible and responsive layouts for web pages. It is a powerful and easy-to-use layout system that helps you control the positioning and sizing of elements on a web page, even as the size of the viewport or the size of the content changes.

With flexbox, you can easily align and distribute elements within a container, regardless of their size or content. You can also control the order in which elements appear, and adjust the spacing between them.

The flexbox layout consists of a flex container and one or more flex items. The container is the parent element that holds the flex items. The container is set to display: flex to activate the flexbox layout, and the child elements (flex items) are set to flex: 1 to make them flexible and fill the available space.

### **Overflow in css**

In CSS, the overflow property controls what happens when the content of an element overflows its container. The overflow property has four possible values:

- visible: This is the default value. Content is not clipped and may overflow the container.  
- hidden: Content that overflows the container is hidden and not visible.  
- scroll: The container displays a scrollbar to allow users to scroll the content that overflows the container.  
- auto: The container displays a scrollbar only when the content overflows. If the content fits within the container, no scrollbar is displayed.

The overflow property is particularly useful for controlling the behaviour of elements with fixed sizes, such as images, text blocks, or menus. For example, you can set the overflow property to scroll or auto for a menu to make sure all the menu items are accessible, even if they overflow the container.

### **D/F B/w js and TS data types**

JavaScript and TypeScript are both programming languages used for developing web applications. However, TypeScript is a superset of JavaScript, which means that it includes all the features of JavaScript and adds some additional features to the language.

When it comes to data types, both JavaScript and TypeScript have similar primitive data types such as string, number, boolean, null, and undefined. However, TypeScript has additional data types that are not available in JavaScript, including:

- Any: This type allows any kind of data to be assigned to a variable.  
- Void: This type is used to represent the absence of any type. It is often used as the return type of functions that do not return any value.  
- Tuple: This type is an array with a fixed number of elements, where each element may have a different data type.  
- Enum: This type is used to define a set of named constants. Each constant has an associated numeric value, and the values can be accessed using the constant name.  
- Never: This type represents a value that will never occur. It is often used as the return type of functions that throw an error or enter an infinite loop.

Overall, TypeScript provides more robust and strict typing than JavaScript, which can help catch errors at compile-time instead of runtime.

### **Define \`declare\` keyword in typescript.**

In TypeScript, the \`declare\` keyword is used to declare the existence of a variable, function, class, interface, or module without actually providing an implementation for it. It is often used to define types for external libraries or to declare global variables in a TypeScript project.

Here are some examples of how \`declare\` can be used in TypeScript:  
1\. Declaring a variable without initialising it:

declare let myVar: string;

This tells TypeScript that there is a variable called \`myVar\` of type \`string\`, but it doesn't provide an initial value for it.

2\. Declaring a function without implementing it:

declare function myFunc(arg: string): number;

This tells TypeScript that there is a function called \`myFunc\` that takes a \`string\` argument and returns a \`number\`, but it doesn't provide an implementation for the function.

3\. Declaring an interface for an external library:

declare interface MyLibrary {  
  doSomething(): void;  
  doSomethingElse(): number;  
}

This tells TypeScript that there is an external library called \`MyLibrary\` that has two methods: \`doSomething\`, which returns \`void\`, and \`doSomethingElse\`, which returns a \`number\`.

4\. Declaring a module:

declare module "my-module" {  
  export function myFunc(arg: string): void;  
  export const myVar: number;  
}

This tells TypeScript that there is a module called \`"my-module"\` that exports a function called \`myFunc\` that takes a \`string\` argument and returns \`void\`, as well as a constant called \`myVar\` of type \`number\`.

* ### **Use of the debugger in javascript.**

A debugger in JavaScript is a tool that helps developers find and fix errors or bugs in their code. It allows developers to pause the execution of their code and examine its state at a specific point in time. This helps them to identify any issues in their code, such as incorrect variable values, unexpected behaviour, or syntax errors.

There are various ways to debug JavaScript code, including using the built-in debugger statement, which triggers the debugger when the code is executed in a web browser's developer console. Developers can also use debugging tools provided by web browsers or integrated development environments (IDEs) such as Visual Studio Code or IntelliJ IDEA.

The debugging process typically involves setting breakpoints in the code where execution can be paused, examining the values of variables at a particular point, stepping through the code one line at a time, and tracking the flow of the code to identify and fix any issues. The goal of debugging is to ensure that the code runs correctly and efficiently and to eliminate any bugs that could cause errors or unexpected behaviour.

* ### **What is \!important?**

In web development, \!important is a CSS rule that gives a particular CSS declaration priority over other declarations that might be applied to the same element.  
When you add \!important to a CSS declaration, it tells the browser to prioritise that rule over any other conflicting rules that might be applied to the same element. This means that the CSS rule with \!important will override any other rules that might be applied to the element

* ### **Why was Angular version 3 skipped?**

Angular-2 introduced the "@angular/router" module and version 2\. In this router version-2 they had a lot of bugs. So, they updated version 2 of the router and individually modified the router and released the angular router version 3\. And, this led to the discrepancies in the version of both router and the Angular version and they wanted to use every package of Angular on the same version. So, they skipped the 3rd version of Angular so that every other package of Angular will be on the same version. And if they would have launched the Angular 3 then with the latest update angular/router version would have been 4\. So, they decided to skip it.

* ### **Difference b/w HTML5 and HTML4.**

HTML5 is the latest version of the HTML (Hypertext Markup Language) standard, and it introduces several new features and improvements over previous versions. Some of the key differences between HTML5 and previous versions of HTML include:

1. **New Semantic Elements**: HTML5 introduces new semantic elements like article, section, header, footer, nav, etc. that provide more context to the content on a web page, making it easier for search engines and screen readers to interpret.  
2. **Multimedia Support**: HTML5 provides native support for multimedia content like audio and video, without the need for plugins like Flash or Silverlight.  
3. **Improved Forms**: HTML5 includes several new form controls like date, time, color, etc. that make it easier to create more complex forms with fewer lines of code. It also includes built-in form validation that can help prevent common form submission errors.  
4. **Canvas and SVG**: HTML5 introduces the canvas and svg elements that allow developers to create and manipulate graphics and animations directly within the web page.  
5. **Offline Support**: HTML5 introduces the ability to store web application data locally on the user's device, allowing users to access web applications even when they are offline.  
6. **Simplified Doctype**: HTML5 introduced a simplified \<\!DOCTYPE\> declaration that makes it easier for developers to write valid HTML5 markup.

Overall, HTML5 introduces many new features and improvements that make it easier for developers to create rich and interactive web applications while providing a better user experience for website visitors.

* ### **CSS sprites**

CSS sprites are a technique used in web development to combine multiple small images into a single larger image, which can then be loaded as a single resource on a web page. The individual images within the larger image are then displayed on the web page using CSS background positioning.

The purpose of using CSS sprites is to reduce the number of HTTP requests that a web page needs to make to the server to load all of its images. When a web page has multiple images, each image requires a separate HTTP request to the server, which can slow down the page load time. By combining these images into a single sprite image, the web page only needs to make one HTTP request to the server, which can significantly reduce the page load time.

To use CSS sprites, developers typically create a single image that contains all the individual images they need for their web page. They then use CSS to specify the position of each individual image within the larger sprite image. When the web page loads, the sprite image is downloaded as a single resource, and each individual image is displayed on the page using the CSS background positioning technique.

CSS sprites are particularly useful for web pages with a large number of small images, such as navigation icons or social media icons, and can help improve the overall performance of the web page.

* ### **\!Doctype**

The HTML document type declaration, also known as DOCTYPE, is the first line of code required in every HTML or XHTML document. The DOCTYPE declaration is an instruction to the web browser about what version of HTML the page is written in. This ensures that the web page is parsed the same way by different web browsers.

* ### **Uses of float**

In CSS, the float property is used to position elements on a web page. When an element is set to float, it is moved to the left or right of its parent container, and other elements flow around it. Here are some common uses of the float property in CSS:

1. Creating columns: The float property is often used to create columns on a web page. By floating two or more elements side by side, you can create a multi-column layout.  
2. Image alignment: Floats are commonly used to align images within text. By floating an image to the left or right of a paragraph, the text will wrap around the image.  
3. Navigation menus: Floats can be used to create horizontal navigation menus. By floating the menu items to the left or right, you can create a row of links that are easy to click.  
4. Grid layouts: The float property is often used in conjunction with other layout techniques, such as CSS grid, to create complex web page layouts.

Overall, the float property is a versatile tool for positioning elements on a web page, and is widely used in modern CSS layouts.

* **CSS Grid property.**

In CSS, a grid system is a set of guidelines that allow you to create a layout of web page elements in a structured way. A grid system typically divides the web page into a series of rows and columns, providing a framework for placing content within these rows and columns.

There are several ways to create a grid system in CSS, but the most popular approach is to use the CSS Grid Layout. The CSS Grid Layout is a two-dimensional grid system that allows you to define rows and columns and place items within them. It provides a high level of flexibility and control over the layout of web page elements.

To create a grid system using CSS Grid Layout, you first need to define a container element using the display: grid property. Once you have defined the container element, you can then define the rows and columns of the grid using the grid-template-rows and grid-template-columns properties respectively. You can also define the size of the grid cells using the grid-template-areas property.

* ### **Geolocation in HTML.**

Geolocation is a feature in HTML that allows a web page to access and use the user's location information, such as latitude and longitude. This information can be used to provide location-based services, such as displaying nearby points of interest, weather information, or local news.  
To use geolocation in HTML, the web page must first request permission from the user to access their location information. This can be done using the navigator.geolocation object, which provides a number of methods for retrieving the user's location.  
Once the user has granted permission, the getCurrentPosition() method can be used to retrieve the user's current location. This method takes two parameters: a success callback function, which is called with the user's location information if the request is successful, and an error callback function, which is called if the request fails.  
For example, here is some sample code that retrieves the user's location and displays it on a web page:  
if (navigator.geolocation) {  
  navigator.geolocation.getCurrentPosition(function(position) {  
    var latitude \= position.coords.latitude;  
    var longitude \= position.coords.longitude;  
    document.getElementById("location").innerHTML \= "Your location: " \+ latitude \+ ", " \+ longitude;  
  }, function(error) {  
    console.log(error);  
  });  
} else {  
  console.log("Geolocation is not supported by this browser.");  
}  
This code checks if the user's browser supports geolocation, and if it does, retrieves the user's location and displays it on the web page. If geolocation is not supported, the code logs an error message to the console.  
Overall, geolocation is a powerful feature in HTML that can be used to provide location-based services and enhance the user experience of a web page.

* ### **Post and Get calls using http client.**

HTTP (Hypertext Transfer Protocol) is the protocol used for communication between web browsers and servers. In HTTP, there are two main types of requests: GET and POST. HTTP clients, such as web browsers or software applications, can use either GET or POST requests to communicate with web servers and retrieve or submit data.

Here is an overview of GET and POST requests and how they are used:

GET Requests:A GET request is used to retrieve data from a web server. When a user enters a URL into their web browser or clicks a link, the browser sends a GET request to the server to retrieve the requested web page. The server responds by sending the requested data back to the client. GET requests are typically used for simple data retrieval, such as fetching web pages, images, or other resources.  
POST Requests:A POST request is used to submit data to a web server. When a user fills out a form or performs some other action that requires submitting data, the web browser sends a POST request to the server. The server processes the data and responds with a status code indicating whether the request was successful or not. POST requests are typically used for more complex data submissions, such as submitting user information, uploading files, or performing database operations.

Overall, GET and POST requests are important concepts in HTTP client programming, and they are essential for building web applications that interact with web servers.

* ### **Event bubbling javascript?**

Event bubbling, also known as event propagation, is a mechanism in JavaScript where an event triggered on a specific element will propagate through its parent elements in the DOM hierarchy. When an event occurs on an element, such as a click event, it is first handled by that element's event handlers, and then it propagates to its parent elements in a top-down manner until it reaches the root element.

During the event bubbling process, each parent element has the opportunity to handle the event or perform some action based on it. If an event handler is registered on a parent element, it will be executed after the event handler of the child element has completed its execution.  
For example, consider the following HTML structure:

\<div id="outer"\>  
  \<div id="inner"\>  
    Click me  
  \</div\>  
\</div\>

If you click on the "Click me" text, the click event will first be handled by the inner \`\<div\>\` element's click event handler, if one is defined. After that, the event will bubble up to the outer \`\<div\>\` element, and its click event handler, if present, will be executed.

This event bubbling behaviour can be useful in situations where you want to handle events on multiple levels of nested elements. However, there may be cases where you want to stop the event from propagating further up the DOM hierarchy. In such cases, you can use the \`event.stopPropagation()\` method within an event handler to prevent the event from bubbling up.  
It's worth noting that event bubbling is the default behaviour in most modern browsers, but it can be modified using the \`event.stopPropagation()\` and \`event.preventDefault()\` methods. Additionally, the order in which event handlers are executed during event bubbling can be controlled using the \`addEventListener\` method with the \`useCapture\` parameter.

* ### **Web storage, local storage and session storage.**

Web storage is a feature of modern web browsers that enables web developers to store data on the client-side, within the user's web browser.   
There are two mechanisms for storing data: localStorage and sessionStorage.   
localStorage allows web developers to store key/value pairs on the client-side that persist even after the user closes their web browser or turns off their device. On the other hand,   
sessionStorage allows the same thing, but only until the user closes their web browser or tab. The data stored in sessionStorage is specific to the window or tab that created it and cannot be accessed by other windows or tabs within the same domain.   
These mechanisms are useful for persistently or temporarily storing data that needs to be used within a session or across multiple sessions, such as user preferences or settings.

* **what is the storage limit of local and session storage**

The storage limit for both local storage and session storage depends on the web browser being used.  
For local storage, the maximum amount of data that can be stored is typically around 5-10 megabytes (MB). However, some web browsers may allow for more or less storage, and the actual limit can also depend on factors such as the available disk space on the device and the settings configured by the user.  
For session storage, the storage limit is typically lower than local storage, and it is usually around 5-10 MB as well. However, like with local storage, the actual limit can vary between web browsers and depend on factors such as the device's available memory.  
It's important to keep in mind that using too much local or session storage can impact website performance, especially on devices with limited resources. It's generally recommended to use storage sparingly and to regularly clean up any unused data to ensure optimal website performance.

* ### **Progress and meter tag in html.**

The \<progress\> tag in HTML is used to represent the progress of a task, such as a file download or a form submission. It can be used with attributes such as value and max to define the current and maximum values of the progress bar. Here's an example:  
\<progress value="50" max="100"\>\</progress\>  
This will display a progress bar that is halfway filled, indicating that the task is 50% complete.

The \<meter\> tag is similar to the \<progress\> tag, but it is used to display a measurement within a given range. It can also be used with the value and max attributes to define the current and maximum values of the measurement. Here's an example:

\<meter value="5" min="0" max="10"\>5 out of 10\</meter\>  
This will display a meter that is halfway filled, indicating that the measurement is at 50% of the maximum value. The text "5 out of 10" will also be displayed inside the meter element.  
Both the \<progress\> and \<meter\> tags can be styled using CSS to change their appearance, such as the color and size of the bar or meter.

* ### **How does ng serve in angular works?**

ng serve is a command in the Angular CLI (Command Line Interface) that allows you to build and run your Angular application locally during development.When we run ng serve in your terminal, it performs several tasks:

- It compiles the TypeScript code of your application into JavaScript code that can be understood by the browser.  
- It bundles all of the compiled code and related assets (such as HTML and CSS files) into a single package.  
- It launches a development server that serves the compiled code and assets on your local machine. By default, the server runs on port 4200\.  
- It monitors your project files for changes and automatically recompiles and reloads your application in the browser whenever you make a change.

This allows you to see your changes in real-time and speed up your development process. You can also use additional command-line options with ng serve, such as \--open to automatically open your application in a browser window or \--port to specify a different port to use for the development server.

* ### **The bundle files that are created while serving our application are:**

When we use the ng serve command in an Angular project, it compiles the application and serves it locally in development mode. The application is compiled into multiple files that are bundled together for efficient delivery to the client's browser.  
Here's a brief overview of the bundle files that are created:

1. **main.js:** This is the main bundle file that contains the application code and all its dependencies. It includes all the components, services, modules, and other resources that are used in the application.  
2. **polyfills.js**: This bundle file contains polyfills for features that are not supported in some browsers. It ensures that the application works consistently across different browsers.  
3. **runtime.js**: This file contains the runtime code required by the Angular compiler to execute the application.  
4. **styles.css**: This bundle file contains all the styles used in the application, including global styles and component-specific styles.  
5. **vendor.js**: This file contains third-party libraries and dependencies used in the application.

These bundle files are generated by the Angular compiler and are stored in the dist directory of your project. When you run ng serve, the application is served from memory, and any changes you make to the code are automatically recompiled and served in real-time.

* ### **Cookies?**

In the context of computer technology, a cookie is a small piece of data that is sent from a website to a user's web browser. This data is stored on the user's device and is used to remember information about the user's preferences or activities on the website.

Cookies can be used for a variety of purposes, including tracking user behaviour, remembering login information, and personalising content. They can be either temporary (session cookies) or permanent (persistent cookies) and can be set by both first-party and third-party websites.

While cookies can be useful for improving the user experience on a website, they can also raise privacy concerns. Some users may choose to disable cookies in their web browsers or use tools to manage and delete cookies regularly.

* ### **New input elements introduced in html 5**

HTML5 introduced several new input types to enhance the usability and functionality of web forms. Here are some of the new input types that were introduced in HTML5:

1. **color:** This input type allows users to select a color from a color picker.  
2. **date:** This input type provides a date picker for users to select a date.  
3. **datetime-local**: This input type allows users to select a date and time from a local time zone.  
4. **email:** This input type is used for email addresses and includes email validation.  
5. number: This input type is used for numeric input, and includes features like minimum and maximum values, and step size.  
6. **range:** This input type allows users to select a value from a range of values, and is often used for sliders.  
7. **search:** This input type is used for search fields and includes a clear button for easier input.  
8. **tel**: This input type is used for telephone numbers and includes telephone number validation.  
9. **time**: This input type provides a time picker for users to select a time.  
10. **url**: This input type is used for URLs and includes URL validation.

These input types provide more user-friendly and intuitive ways for users to input data on web forms, and can help improve the overall user experience of a website.

* ### **What is pseudo class in css**

In CSS, a pseudo-class is a keyword added to a selector that specifies a special state of the selected element. Pseudo-classes allow you to apply styles to an element based on various factors such as user interaction, position, and content.  
Here are some examples of common pseudo-classes in CSS:

1. **:hover**: Applies styles to an element when the user hovers over it with the mouse.  
2. **:active**: Applies styles to an element when the user clicks on it.  
3. **:focus:** Applies styles to an element when it has focus, such as when it is selected with the keyboard.  
4. **:visited:** Applies styles to a link that has been visited by the user.  
5. **:first-child:** Applies styles to the first child element of a parent element.  
6. **:nth-child():** Applies styles to an element based on its position in the parent element, using a formula (such as :nth-child(2n+1) to select odd-numbered elements).  
7. **:not()**: Allows you to select all elements except those that match a certain selector.

These are just a few examples of the many pseudo-classes available in CSS. Pseudo-classes allow for more precise and dynamic styling of web pages, and can help improve the user experience by providing visual feedback and interactive effects.

* ### **What are pseudo elements in CSS**

Pseudo-elements are special keywords in CSS that allow you to style certain parts of an element's content without needing to add additional HTML markup. They are denoted by double colons (::) and come after the element's selector.  
Pseudo-elements can be used to style things like the first letter or line of a block of text, or to insert content before or after an element.  
Here are some examples of pseudo-elements and their uses:

* **::first-letter:** styles the first letter of the first line of text within an element  
* **::first-line**: styles the first line of text within an element  
* **::before:** inserts content before the content of an element  
* **::after:** inserts content after the content of an element

To use a pseudo-element, you would specify the element's selector followed by the double colon and the name of the pseudo-element. For example, to style the first letter of a paragraph, you would use:  
p::first-letter {  
  font-size: 2em;  
  color: red;  
}

* ### **what are the types of inheritance**

In object-oriented programming, there are several types of inheritance. The most commonly recognized types of inheritance are:

1. **Single Inheritance**: A class that derives from only one base class is said to have single inheritance.  
2. **Multiple Inheritance**: A class that derives from more than one base class is said to have multiple inheritance.  
3. **Multilevel Inheritance**: A class that derives from a derived class is said to have multilevel inheritance.  
4. **Hierarchical Inheritance**: A class that has more than one derived class is said to have hierarchical inheritance.  
5. **Hybrid Inheritance**: A combination of two or more types of inheritance is called hybrid inheritance.  
6. **Multipath Inheritance**: This is a special case of multiple inheritance where a derived class is derived from two or more classes which have a common base class.

Each type of inheritance has its own advantages and disadvantages, and it is up to the programmer to choose the appropriate type for a particular situation.

### **Why is it not recommended to use the native element property of elementRef in Angular.**

In Angular, an ElementRef is a class that grants direct access to the underlying DOM element. The nativeElement property of the ElementRef object is used to access the underlying DOM element.  
While it may seem convenient to use the nativeElement property to access and manipulate the DOM directly, it is generally not recommended to do so. Here are some reasons why:

1. **Security**: Accessing and manipulating the DOM directly using nativeElement can introduce security vulnerabilities in your application. If you're not careful, you could inadvertently introduce cross-site scripting (XSS) attacks or other security issues.  
2. **Maintainability**: Accessing the DOM directly using nativeElement can make your code more difficult to maintain. If you access the DOM directly in multiple places throughout your code, you can create a lot of duplicate code. This can make it harder to change the behaviour of your code later.  
3. **Testability**: Code that accesses the DOM directly using nativeElement can be more difficult to test. If you write tests for your Angular components, you want to test the behaviour of the component, not the behaviour of the underlying DOM element.  
4. **Cross-platform compatibility**: Finally, accessing the DOM directly using nativeElement can make your code less compatible with different platforms. For example, if you later decide to use your Angular code in a different environment, such as a native mobile app, you may need to rewrite parts of your code that depend on the DOM.

To avoid these issues, it is generally recommended to use Angular's built-in directives and services to manipulate the DOM, rather than accessing the DOM directly using nativeElement.

* ### **What do you mean by BOM?**

Browser Object Model is known as BOM. It allows users to interact with the browser. A browser's initial object is a window. As a result, you may call all of the window's functions directly or by referencing the window. The document, history, screen, navigator, location, and other attributes are available in the window object.

* ### **\*ngIf vs Hidden**

\`ngIf\` and \`hidden\` are both Angular directives used to conditionally show or hide elements in an Angular application, but they work in slightly different ways.  
**\`ngIf\`:**

* \`ngIf\` is a structural directive that removes or adds elements to the DOM based on a condition.  
* When the condition provided to \`ngIf\` is true, the element and its contents are added to the DOM. If the condition is false, the element and its contents are removed from the DOM.  
* The Angular framework will also create or destroy the associated component and its child components when the condition changes.  
* The element and its associated components are completely removed from the DOM when the condition is false, which means they won't take up any space or consume any resources.  
* Usage example: \`\<div \*ngIf="showElement"\>This element will be added or removed based on the condition.\</div\>\`

**\`hidden\`:**

* \`Hidden\` is a property binding that allows you to hide an element by setting the \`hidden\` attribute to true or false.  
* When the \`hidden\` attribute is set to true, the element is visually hidden but still occupies space in the DOM.  
* When the \`hidden\` attribute is set to false, the element is displayed normally.  
* The associated component and its child components remain in the DOM regardless of the value of the \`hidden\` attribute.  
* Usage example: \`\<div \[hidden\]="hideElement"\>This element will be visually hidden or displayed based on the attribute value.\</div\>\`

In summary, \`ngIf\` conditionally adds or removes elements from the DOM along with their associated components, while \`hidden\` simply hides or shows an element visually without affecting its presence in the DOM. The choice between the two depends on whether you want to completely remove the element or just hide it.

* ### **what are web workers**

When executing scripts in an HTML page, the page becomes unresponsive until the script is finished.  
A web worker is a JavaScript that runs in the background, independently of other scripts, without affecting the performance of the page. You can continue to do whatever you want: clicking, selecting things, etc., while the web worker runs in the background.

* ### **How can I use other ordered list sequences like a, b, c, d or roman no. etc in HTML?**

In HTML, you can use different types of ordered list sequences by specifying the \`type\` attribute on the \`\<ol\>\` (ordered list) element. Here are a few examples:

* Using alphabetic sequences (a, b, c, d):

  \<ol type="a"\>

    \<li\>Item 1\</li\>

  \</ol\>

* Using uppercase alphabetic sequences (A, B, C, D):

  \<ol type="A"\>

    \<li\>Item 1\</li\>

    \<li\>Item 2\</li\>

  \</ol\>

* Using roman numerals (i, ii, iii, iv):

  \<ol type="i"\>

    \<li\>Item 1\</li\>

    \<li\>Item 2\</li\>

  \</ol\>

* Using uppercase roman numerals (I, II, III, IV):

  \<ol type="I"\>

    \<li\>Item 1\</li\>

  \</ol\>

You can choose from other types as well, such as lowercase alphabetic (\`type="a"\`), uppercase alphabetic (\`type="A"\`), decimal (\`type="1"\`), and more. The \`type\` attribute allows you to customise the appearance of your ordered lists based on your specific requirements.

* ### **How closures work?**

Closures in JavaScript are a combination of a function and the lexical environment in which it was declared. To understand closures, let's break down the components and how they work together:

1. **Functions**: In JavaScript, functions are first-class citizens, which means they can be assigned to variables, passed as arguments to other functions, and returned as values from functions.  
2. **Lexical Environment**: The lexical environment consists of all the variables, functions, and their scopes that were present at the time the closure was created. It captures the state of the surrounding code when a function is defined.

When a function is defined inside another function, it forms a closure. The inner function has access to its own local variables, parameters, and the variables of the outer function. Even after the outer function has finished executing and its local variables are no longer in scope, the inner function maintains access to those variables through the closure. Here's an example to illustrate how closures work:  
\`\`\`javascript  
function outerFunction() {  
  const outerVariable \= 'I am from the outer function';

  function innerFunction() {  
    console.log(outerVariable);  
  }

  return innerFunction;  
}

const closure \= outerFunction();  
closure(); // Output: I am from the outer function  
\`\`\`  
In the example, the \`outerFunction\` defines an \`outerVariable\` and an \`innerFunction\`. The \`innerFunction\` is returned from \`outerFunction\`, forming a closure. When \`outerFunction\` is called and assigned to \`closure\`, it captures the lexical environment of \`outerFunction\` at that point.

When \`closure\` is invoked, it still has access to the \`outerVariable\` of the \`outerFunction\`, even though \`outerFunction\` has completed executing. This is possible because the closure retains a reference to the variables it needs from the surrounding environment.

Closures are powerful because they allow functions to access and manipulate variables that are not directly accessible to them. They provide a way to create private variables, encapsulate data, and maintain state across multiple function invocations.

It's important to note that closures can have memory implications, as they retain references to variables, potentially preventing them from being garbage collected. Care should be taken to avoid unintended memory leaks when working with closures.

* ### **Temporal dead zone.**

Temporal Dead Zone is a behaviour that occurs with variables declared using let and const keywords. It is a behaviour where we try to access a variable before it is initialised. Examples of temporal dead zone:  
x \= 23; // Gives reference error

let x;

function anotherRandomFunc(){  
  message \= "Hello"; // Throws a reference error

  let message;  
}  
anotherRandomFunc();  
In the code above, both in the global scope and functional scope, we are trying to access variables that have not been declared yet. This is called the Temporal Dead Zone.

* ### **Fibonacci series in JS**

Here's an example of how you can generate a Fibonacci series in JavaScript:  
\`\`\`javascript  
function fibonacciSeries(n) {  
  const series \= \[0, 1\]; // Initialize the series with the first two numbers: 0 and 1

  if (n \<= 2\) {  
    // If n is 1 or 2, return the initial series  
    return series.slice(0, n);  
  }

  for (let i \= 2; i \< n; i++) {  
    // Generate the subsequent Fibonacci numbers and add them to the series  
    const nextNumber \= series\[i \- 1\] \+ series\[i \- 2\];  
    series.push(nextNumber);  
  }

  return series;  
}

// Generate Fibonacci series for the first 10 numbers  
const result \= fibonacciSeries(10);  
console.log(result); // Output: \[0, 1, 1, 2, 3, 5, 8, 13, 21, 34\]  
\`\`\`  
In the above code, the \`fibonacciSeries\` function takes an input \`n\` representing the number of Fibonacci numbers to generate. It initialises the series with the first two numbers, 0 and 1\. If \`n\` is less than or equal to 2, it returns the initial series up to that point. If \`n\` is greater than 2, a loop is used to generate the subsequent Fibonacci numbers by adding the previous two numbers in the series. Each new number is then pushed to the \`series\` array. Finally, the \`series\` array is returned.

In the example, \`fibonacciSeries(10)\` generates the first 10 Fibonacci numbers and logs the result to the console. You can modify the function call and the value of \`n\` to generate a different number of Fibonacci numbers as needed.

* ### **How can components share data?**

In Angular, components can share data with each other using various techniques. Here are some common ways to share data between components:

**Parent-to-Child Communication (Input Binding):**

**Child-to-Parent Communication (Event Emitter).**

**Service (Shared Service):**

* Components can share data through a shared service by injecting the service into the components that need to communicate.  
* The shared service acts as a central place to store and manage the shared data.  
* Components can use the service to read and update the shared data. Example:   
  Shared service class:  
  @Injectable()   
  export class DataService { /\* shared data and methods \*/ }\`  
* Components inject the service and use its methods to share data.

**Route Parameters/Query Parameters:**

* Components can share data through route parameters or query parameters when navigating between routes.  
* Data can be passed as part of the URL, and the target component can read the parameters from the activated route. Example:

Route configuration: \`{ path: 'details/:id', component: DetailsComponent }\`  
Navigation: \`this.router.navigate(\['/details', id\]);\`  
Details component: \`constructor(private route: ActivatedRoute) { this.id \= this.route.snapshot.params.id; }\`

**Local Storage/Session Storage**:

* Components can share data by storing it in the browser's local storage or session storage.  
* One component stores the data, and another component retrieves it from the storage.  
* This approach allows data to persist across page refreshes or component reloads.

These are some common approaches for sharing data between components in Angular. The choice of technique depends on the specific requirements and the relationship between the components.

* ### **What is angular/CLI**

Angular CLI (Command Line Interface) is a powerful command-line tool provided by the Angular team. It is designed to simplify and streamline the development process of Angular applications. Angular CLI offers a set of commands and features that help developers create, manage, and build Angular projects efficiently.

Key features of Angular CLI include:

1\. **\*\*Project Scaffolding\*\***: Angular CLI allows you to generate the basic structure and files for a new Angular project effortlessly. It sets up the recommended project structure, configuration files, and initial dependencies, providing a solid foundation to start building an Angular application.

2\. **\*\*Development Server\*\***: Angular CLI includes a built-in development server that enables you to run and test your application locally during development. The development server automatically compiles your code, provides live reload functionality, and allows you to view your application in a web browser.

3\. **\*\*Code Generation\*\***: Angular CLI offers powerful code generation capabilities, enabling you to create various Angular components, services, modules, and more with just a few simple commands. This greatly speeds up the development process and helps maintain consistent code patterns.

4\. **\*\*Configuration Management\*\***: Angular CLI provides a central configuration file (\`angular.json\`) that allows you to manage various aspects of your project's configuration, including build settings, asset management, environment configurations, and more. This helps ensure consistency across different environments and simplifies the management of project configurations.

5\. **\*\*Build and Deployment\*\***: Angular CLI offers build optimization options for production builds, such as bundling, minification, and tree-shaking, to create optimised and efficient deployments. It also provides commands for creating build artefacts that can be deployed to various hosting platforms or servers.

6\. **\*\*Testing\*\*:** Angular CLI integrates with popular testing frameworks, such as Karma and Jasmine, and provides commands to run unit tests, end-to-end (E2E) tests, and generate code coverage reports. This promotes a robust testing strategy and facilitates the creation of high-quality Angular applications.

Angular CLI simplifies many common development tasks, automates repetitive processes, and enforces best practices, making it a valuable tool for Angular developers. It allows developers to focus more on building features and less on the setup and configuration of the development environment.

* ### **What is a json pipe?**

The \`json\` pipe is a built-in pipe in Angular that is used to transform data into a JSON string format. It is primarily used for debugging and displaying data in a human-readable format.

The \`json\` pipe takes an input value and converts it into a JSON string representation. This can be useful when you want to display complex data structures, such as objects or arrays, in a formatted way. Here's an example of using the \`json\` pipe in an Angular template:

\<p\>{{ myData | json }}\</p\>  
In the above example, \`myData\` is a variable or property that holds some data. By applying the \`json\` pipe to \`myData\`, the data will be converted into a JSON string and displayed in the \`\<p\>\` element. The resulting JSON string will be formatted with proper indentation and line breaks for readability. For instance, if \`myData\` contains an object like \`{ "name": "John", "age": 25 }\`, the rendered output will be:  
\<p\>{  
  "name": "John",  
  "age": 25  
}\</p\>  
The \`json\` pipe is commonly used in Angular templates when working with APIs, debugging data, or simply displaying data objects in a readable format.

It's important to note that the \`json\` pipe is for display purposes and does not perform any modification on the underlying data. If you need to work with JSON data programmatically, you would use JavaScript's \`JSON.parse()\` and \`JSON.stringify()\` methods.

* ### **What is the difference between dirty, pristine, touched, and untouched states of a form control?**

In the context of form controls, the terms "dirty," "pristine," "touched," and "untouched" are commonly used to describe different states or conditions of the controls. Here's what each of these terms typically refers to:

1\. Dirty: The "dirty" state indicates that the value of a form control has been changed by the user. For example, if a user types something into a text input field or selects an option from a dropdown menu, the control is considered dirty because its value has been modified since it was initially loaded or reset.

2\. Pristine: The "pristine" state, on the other hand, signifies that a form control has not been modified by the user. It represents the initial or default state of the control when the form is loaded or reset. A control is considered pristine if its value has not been changed since the form was rendered.

3\. Touched: The "touched" state indicates that a user has interacted with a form control, specifically by focusing on it and then moving away or blurring the control. It doesn't necessarily mean that the value of the control has been modified, but rather that the user has engaged with it in some way.

4\. Untouched: The "untouched" state refers to the opposite of the touched state. If a form control has not been interacted with or focused by the user, it is considered untouched. This state typically applies when a form is initially loaded, and the user has not yet interacted with any of the controls.

These states are often used in web development frameworks or libraries to implement form validation, tracking user input, and displaying feedback or error messages. By distinguishing between these states, developers can provide a more dynamic and user-friendly form experience.

* ### **List all concepts related to ‘.this’.**

In TypeScript, the \`this\` keyword refers to the current instance of an object or the object on which a method is being called. It is a special variable that allows you to access properties and methods within the scope of an object.

Here are some key concepts related to the \`this\` keyword in TypeScript:

1\. Function Scope: In regular functions, the value of \`this\` is determined by how the function is called. When a function is invoked as a standalone function, \`this\` refers to the global object (e.g., \`window\` in a browser environment or \`global\` in Node.js). However, when a function is called as a method of an object, \`this\` refers to the object itself.

1\. Function Scope: In regular functions, the value of \`this\` is determined by how the function is called. When a regular function is invoked as a standalone function, the value of \`this\` is set to the global object. In a browser environment, the global object is typically \`window\`, while in Node.js, it is \`global\`. For example:

\`\`\`javascript  
function sayHello() {  
  console.log(this); // 'this' refers to the global object  
}

sayHello(); // Output: Window object (in a browser environment)  
\`\`\`

However, when a regular function is called as a method of an object, \`this\` refers to the object itself. In other words, \`this\` inside the function will be a reference to the object on which the method was called. For example:

\`\`\`javascript  
const person \= {  
  name: 'John',  
  greet: function() {  
    console.log('Hello, ' \+ this.name \+ '\!');  
  }  
};

person.greet(); // Output: Hello, John\!  
\`\`\`

In the above example, \`this.name\` accesses the \`name\` property of the \`person\` object because the \`greet\` function is invoked as a method of \`person\`.

2\. Arrow Functions: Arrow functions, introduced in ES6, have a different behavior when it comes to the \`this\` keyword. Arrow functions have lexical scoping for \`this\`, which means they do not bind their own \`this\` value. Instead, they inherit the \`this\` value from the surrounding (enclosing) scope. This behavior is often useful in scenarios where you need to maintain the context of \`this\` or when using arrow functions as callback functions.

For example, consider the following code using a regular function expression:

\`\`\`javascript  
const obj \= {  
  name: 'Alice',  
  greet: function() {  
    setTimeout(function() {  
      console.log('Hello, ' \+ this.name \+ '\!');  
    }, 1000);  
  }  
};

obj.greet(); // Output: Hello, undefined\!  
\`\`\`

In the above code, the \`setTimeout\` callback function is a regular function expression. When it is executed after the timeout, \`this\` inside the callback function refers to the global object (e.g., \`window\` in a browser). Hence, \`this.name\` results in \`undefined\`.

Now, let's see how the behavior changes when using an arrow function:

\`\`\`javascript  
const obj \= {  
  name: 'Alice',  
  greet: function() {  
    setTimeout(() \=\> {  
      console.log('Hello, ' \+ this.name \+ '\!');  
    }, 1000);  
  }  
};

obj.greet(); // Output: Hello, Alice\!  
\`\`\`

In this modified code, the \`setTimeout\` callback function is now an arrow function. Arrow functions inherit \`this\` from their surrounding scope, which in this case is the \`greet\` method of the \`obj\` object. Therefore, \`this.name\` inside the arrow function still refers to the \`name\` property of the \`obj\` object, resulting in the expected output: "Hello, Alice\!".

Arrow functions' lexical scoping of \`this\` is particularly useful in scenarios where you need to preserve the context of \`this\`, such as when passing a function as a callback where the value of \`this\` should refer to the enclosing object rather than being determined by how the function is called.

1\. Function Scope: In regular functions, the value of \`this\` is determined by how the function is called. When a regular function is invoked as a standalone function, the value of \`this\` is set to the global object. In a browser environment, the global object is typically \`window\`, while in Node.js, it is \`global\`. For example:

\`\`\`javascript  
function sayHello() {  
  console.log(this); // 'this' refers to the global object  
}

sayHello(); // Output: Window object (in a browser environment)  
\`\`\`

However, when a regular function is called as a method of an object, \`this\` refers to the object itself. In other words, \`this\` inside the function will be a reference to the object on which the method was called. For example:

\`\`\`javascript  
const person \= {  
  name: 'John',  
  greet: function() {  
    console.log('Hello, ' \+ this.name \+ '\!');  
  }  
};

person.greet(); // Output: Hello, John\!  
\`\`\`

In the above example, \`this.name\` accesses the \`name\` property of the \`person\` object because the \`greet\` function is invoked as a method of \`person\`.

2\. Arrow Functions: Arrow functions, introduced in ES6, have a different behavior when it comes to the \`this\` keyword. Arrow functions have lexical scoping for \`this\`, which means they do not bind their own \`this\` value. Instead, they inherit the \`this\` value from the surrounding (enclosing) scope. This behavior is often useful in scenarios where you need to maintain the context of \`this\` or when using arrow functions as callback functions.

For example, consider the following code using a regular function expression:

\`\`\`javascript  
const obj \= {  
  name: 'Alice',  
  greet: function() {  
    setTimeout(function() {  
      console.log('Hello, ' \+ this.name \+ '\!');  
    }, 1000);  
  }  
};

obj.greet(); // Output: Hello, undefined\!  
\`\`\`

In the above code, the \`setTimeout\` callback function is a regular function expression. When it is executed after the timeout, \`this\` inside the callback function refers to the global object (e.g., \`window\` in a browser). Hence, \`this.name\` results in \`undefined\`.

Now, let's see how the behavior changes when using an arrow function:

\`\`\`javascript  
const obj \= {  
  name: 'Alice',  
  greet: function() {  
    setTimeout(() \=\> {  
      console.log('Hello, ' \+ this.name \+ '\!');  
    }, 1000);  
  }  
};

obj.greet(); // Output: Hello, Alice\!  
\`\`\`

In this modified code, the \`setTimeout\` callback function is now an arrow function. Arrow functions inherit \`this\` from their surrounding scope, which in this case is the \`greet\` method of the \`obj\` object. Therefore, \`this.name\` inside the arrow function still refers to the \`name\` property of the \`obj\` object, resulting in the expected output: "Hello, Alice\!".

Arrow functions' lexical scoping of \`this\` is particularly useful in scenarios where you need to preserve the context of \`this\`, such as when passing a function as a callback where the value of \`this\` should refer to the enclosing object rather than being determined by how the function is called.

2\. Arrow Functions: Arrow functions (\`() \=\> {}\`) introduced in ES6 have a lexical scoping for \`this\`. Unlike regular functions, arrow functions do not bind their own \`this\` value. Instead, they inherit the \`this\` value from the surrounding scope. This behaviour is often useful in callback functions or when you need to maintain the context of \`this\`.

3\. Method Invocation: When a method is invoked on an object, \`this\` inside the method refers to the object itself. For example:  
\`\`\`typescript  
const obj \= {  
  name: 'John',  
  sayHello: function() {  
    console.log(\`Hello, ${this.name}\!\`);  
  }  
};

obj.sayHello(); // Output: Hello, John\!  
In this example, \`this\` inside the \`sayHello\` method refers to the \`obj\` object.

4\. Explicitly Setting \`this\`: You can explicitly set the value of \`this\` using the \`call\`, \`apply\`, or \`bind\` methods provided by JavaScript. These methods allow you to invoke a function and specify the context (i.e., the value of \`this\`) explicitly.  
\`\`\`typescript  
function greet() {  
  console.log(\`Hello, ${this.name}\!\`);  
}

const person \= { name: 'Alice' };

greet.call(person); // Output: Hello, Alice\!  
In this case, \`call\` is used to invoke the \`greet\` function with the \`person\` object as the context, so \`this\` inside \`greet\` refers to \`person\`.

5\. Class Methods: When working with classes in TypeScript, methods defined within a class have \`this\` automatically bound to the instance of the class. It allows you to access properties and methods of the current object instance.

\`\`\`typescript  
class MyClass {  
  private name: string;

  constructor(name: string) {  
    this.name \= name;  
  }

  greet() {  
    console.log(\`Hello, ${this.name}\!\`);  
  }  
}  
const obj \= new MyClass('John');  
obj.greet(); // Output: Hello, John\!  
In this example, \`this\` inside the \`greet\` method refers to the instance of \`MyClass\`.

Understanding the behaviour of the \`this\` keyword is crucial in TypeScript as it determines the context in which a function is executed. It is important to note that the behaviour of \`this\` can be affected by function invocations, function binding, arrow functions, or the use of classes. Being familiar with these concepts will help you write effective and maintainable code in TypeScript.

* ### **How can we hide queryParams?**

In Angular, you can hide query parameters by utilising the \`queryParamsHandling\` option provided by the Angular Router. This option allows you to control how query parameters are preserved or discarded when navigating to a new route.

To hide query parameters, you can set the \`queryParamsHandling\` option to \`'merge'\` when defining your route. Here's an example:  
\`\`\`typescript  
import { NgModule } from '@angular/core';  
import { RouterModule, Routes } from '@angular/router';

const routes: Routes \= \[  
  {path: 'example',component: ExampleComponent, queryParamsHandling: 'merge'},  
  // other routes...  
\];

@NgModule({  
  imports: \[RouterModule.forRoot(routes)\],  
  exports: \[RouterModule\]  
})  
export class AppRoutingModule { }  
\`\`\`  
In the above example, the \`queryParamsHandling\` option is set to \`'merge'\` for the \`example\` route. This means that when you navigate to the \`example\` route, the query parameters from the previous route will be merged with the query parameters of the \`example\` route. As a result, the query parameters will be present in the URL, but they won't be visible in the address bar.

For example, if you navigate from \`/previous?param1=value1\` to \`/example?param2=value2\`, the resulting URL will be \`/example?param1=value1\&param2=value2\`. However, only \`param2=value2\` will be visible in the address bar.

By using this approach, you can effectively hide query parameters from the user while still making use of them in your Angular components.

* ### **What are tuples and why was it introduced?**

In TypeScript, a tuple is a data type that represents an ordered collection of elements of different types. It is similar to an array but has a fixed length and each element can have a different type. Tuples were introduced in TypeScript to provide developers with a way to explicitly define and enforce the type and length of arrays. The main reasons why tuples were introduced in TypeScript are:

1. **Type safety**: Tuples allow you to specify the types of each element in a fixed order. This provides better type checking at compile-time, ensuring that you don't accidentally mix up the order of elements or assign incompatible types.  
2. **Fixed length**: Unlike regular arrays, tuples have a fixed length. Once defined, the number of elements and their types cannot be changed. This can be useful in scenarios where you need to represent a specific structure with a known number of elements.  
3. **Descriptive semantics**: Tuples allow you to assign meaningful names to the elements, providing a semantic context to the data structure. This can improve code readability and self-documentation, making it easier for other developers to understand the purpose of the tuple.  
4. **Efficient memory allocation**: Since tuples have a fixed length, TypeScript can allocate memory for all the elements in advance. This can lead to more efficient memory usage compared to dynamic arrays, where memory may need to be reallocated as elements are added or removed.

Here's an example of defining and using a tuple in TypeScript:

\`\`\`typescript  
let employee: \[string, number, boolean\];  
employee \= \["John Doe", 30, true\];

console.log(employee\[0\]); // Output: "John Doe"  
console.log(employee\[1\]); // Output: 30  
console.log(employee\[2\]); // Output: true  
\`\`\`  
In the example above, the \`employee\` tuple is defined with three elements: a string for the name, a number for the age, and a boolean indicating whether the employee is currently active. The tuple enforces the types and order of the elements, providing type safety.

Overall, tuples in TypeScript provide a way to explicitly define and enforce the structure of arrays, ensuring type safety and improving code readability in scenarios where the length and types of elements are fixed.

* ### **How can we store data into local and session storage using services in angular?**

In Angular, you can store data into local and session storage using services by following these steps:

1. **Create a service**: First, create a new service using the Angular CLI command \`ng generate service \<service-name\>\`. This will generate a new service file with the specified name.  
2. **Import dependencies**: In the generated service file, import the \`Injectable\` decorator from \`@angular/core\` and the \`Observable\` class from \`rxjs\`.  
3. **Implement the service**: Within the service class, you can define methods to interact with the local and session storage.  
   \`\`\`typescript  
   import { Injectable } from '@angular/core';  
     
   @Injectable({  
     providedIn: 'root'  
   })  
   export class StorageService {  
     
     constructor() { }  
     
     // Method to set data in local storage  
     setLocalData(key: string, value: any): void {  
       localStorage.setItem(key, JSON.stringify(value));  
     }  
     
     // Method to get data from local storage  
     getLocalData(key: string): any {  
       const data \= localStorage.getItem(key);  
       return data ? JSON.parse(data) : null;  
     }  
     
     // Method to remove data from local storage  
     removeLocalData(key: string): void {  
       localStorage.removeItem(key);  
     }  
     
     // Method to clear all data from local storage  
     clearLocalData(): void {  
       localStorage.clear();  
     }  
     
     // Method to set data in session storage  
     setSessionData(key: string, value: any): void {  
       sessionStorage.setItem(key, JSON.stringify(value));  
     }  
     
     // Method to get data from session storage  
     getSessionData(key: string): any {  
       const data \= sessionStorage.getItem(key);  
       return data ? JSON.parse(data) : null;  
     }  
     
     // Method to remove data from session storage  
     removeSessionData(key: string): void {  
       sessionStorage.removeItem(key);  
     }  
     
     // Method to clear all data from session storage  
     clearSessionData(): void {  
       sessionStorage.clear();  
     }  
     
   }  
   \`\`\`  
4. **Use the service**: Inject the \`StorageService\` into the component where you want to store or retrieve data. You can then call the service methods to interact with the local and session storage.  
   \`\`\`typescript  
   import { Component } from '@angular/core';  
   import { StorageService } from 'path/to/storage.service';  
     
   @Component({  
     selector: 'app-my-component',  
     template: \`  
       \<button (click)="setData()"\>Set Data\</button\>  
       \<button (click)="getData()"\>Get Data\</button\>  
     \`  
   })  
   export class MyComponent {  
     
     constructor(private storageService: StorageService) { }  
     
     setData(): void {  
       const data \= { name: 'John', age: 30 };  
       this.storageService.setLocalData('myData', data);  
     }  
     
     getData(): void {  
       const data \= this.storageService.getLocalData('myData');  
       console.log(data);  
     }  
   }  
   \`\`\`

By using the \`StorageService\` methods, you can easily store and retrieve data from the local and session storage in your Angular application.

* ### **Data in local and session storage are stored in which format of data type?**

Data in local and session storage are stored as strings. The storage mechanisms (localStorage and sessionStorage) can only store data in the form of strings. Therefore, when storing data in local or session storage, you need to convert your data into a string format.

In the example provided earlier, the \`JSON.stringify()\` method is used to convert the data into a JSON string before storing it in the storage. When retrieving the data, the \`JSON.parse()\` method is used to parse the stored string and convert it back into its original data type. For example, when setting data in local storage using the \`setLocalData()\` method from the \`StorageService\`:  
\`\`\`typescript  
const data \= { name: 'John', age: 30 };  
this.storageService.setLocalData('myData', data);  
\`\`\`  
The \`data\` object is converted into a JSON string using \`JSON.stringify()\` before storing it in local storage. When retrieving the data using the \`getLocalData()\` method:  
\`\`\`typescript  
const data \= this.storageService.getLocalData('myData');  
\`\`\`  
The stored string is retrieved from local storage and parsed back into an object using \`JSON.parse()\` to restore its original data type.

It's important to note that the data stored in local and session storage is limited to simple data types (strings, numbers, booleans) or structured data types (objects and arrays) that can be converted to JSON. Complex data types like functions or instances of custom classes cannot be stored directly in local or session storage.

* ### **Generate random numbers every minute in JS.**

To generate random numbers every minute in JavaScript, you can use the \`setInterval()\` function to execute a code block at regular intervals and the \`Math.random()\` function to generate random numbers. Here's an example code snippet that generates a random number every minute:  
\`\`\`javascript  
function generateRandomNumber() {  
  const randomNumber \= Math.random();  
  console.log(randomNumber);  
}

setInterval(generateRandomNumber, 60000); // 60000 milliseconds \= 1 minute  
\`\`\`  
In the above code, the \`generateRandomNumber()\` function generates a random number using \`Math.random()\` and logs it to the console. The \`setInterval()\` function is then used to repeatedly call the \`generateRandomNumber()\` function every 1 minute (60000 milliseconds).

You can modify the \`generateRandomNumber()\` function to perform any desired action with the generated random number instead of just logging it to the console.

let arr \= \[  
    \[1, 2\],  
    \[3, 4\],  
    \[5, 6\]\[7, 8, 9\],  
    \[10, 11, 12, 13, 14, 15\]  
\]

* ### **How can I make my object's value unchangeable?**

In JavaScript, you can make objects' values unchangeable by using the \`Object.freeze()\` method. The \`Object.freeze()\` method prevents any modifications to the object, including adding or removing properties, and modifying existing properties. Here's how you can use it:  
\`\`\`javascript  
const myObject \= {  
  key1: 'value1',  
  key2: 'value2'  
};

Object.freeze(myObject);

// Attempting to modify the object will have no effect  
myObject.key1 \= 'new value';  
delete myObject.key2;

console.log(myObject); // { key1: 'value1', key2: 'value2' }  
\`\`\`  
As you can see in the example, after calling \`Object.freeze(myObject)\`, any attempts to modify the object are ignored, and the object remains unchanged. The \`myObject.key1 \= 'new value';\` assignment is silently ignored, and the \`delete myObject.key2;\` operation has no effect.

However, please note that \`Object.freeze()\` only provides shallow immutability. It prevents modifications to the top-level properties of an object but does not recursively freeze nested objects. If you want to achieve deep immutability, where all nested objects and arrays are also frozen, you'll need to implement a custom deep-freezing function or use third-party libraries like \`Immutable.js\` or \`Immer\`.

**Q**  
let number \= 50

function print() {  
  let square \= number \* number

  if (number \< 60\) {  
    var largerNumber \= 80  
    let anotherLargerNumber \= 100

    console.log(square)  
  }

  console.log(largerNumber)  
  console.log(anotherLargerNumber)  
}

print()

* ### **this.router.navigate(\['../'\]); where will this syntax lead to?**

The syntax \`this.router.navigate(\['../'\])\` is typically used in the context of routing in web applications, specifically when using the Angular framework. It navigates to the parent route relative to the current route.

When this syntax is executed, it will navigate to the parent route of the current route. The number of \`../\` segments determines how many levels up in the route hierarchy it will go. Each \`../\` segment represents one level up.

For example, if the current route is \`/parent/child\`, then \`this.router.navigate(\['../'\])\` will navigate to \`/parent\`. Similarly, if the current route is \`/parent/child/grandchild\`, then \`this.router.navigate(\['../'\])\` will also navigate to \`/parent\`.

It's important to note that the exact behaviour and destination of the navigation depend on the specific routing configuration of your application. The router configuration and the routes defined in your Angular application will determine the actual destination when using \`this.router.navigate(\['../'\])\`.

* ### **Define decorators and its different types?**

Decorators in Angular are design patterns or functions that modify the behaviour of Angular features. There are four types of decorators in Angular: class decorators, property decorators, method decorators, and parameter decorators. Class decorators are used to identify if a class is a component or module. Property decorators are used to decorate properties within classes. Method decorators add functionality to methods within a class. Parameter decorators are used to inject services into constructors.

Class decorators

* Class decorators in Angular are used to define if a class is a component or a module.  
* The widely used class decorators in Angular are @Component and @NgModule.

Property decorators

* Property decorators in Angular allow us to decorate properties within classes.  
* We can use property decorators such as @Input(), @Output(), @Override(), etc.  
* The @Input() decorator creates an input binding with the property name.

Method decorators

* Method decorators in Angular are used to decorate methods inside a class.  
* An example of a method decorator is @HostListener, which is used before a method.

Parameter decorators

* Parameter decorators in Angular are applied to constructor parameters.  
* They are used to inject a specific provider in a constructor with @Inject().

Using decorators in Angular

* We can use decorators in Angular to define component behaviour and handle events.  
* Decorators like @HostListener can be used to add functionality to methods.

* ### **What is a router event?**

In the Angular framework, the RouterEvent is an event emitted by the Angular Router when there are navigation-related events or changes in the router state. It allows you to track and respond to various navigation events within your Angular application.

The RouterEvent is an abstract class that serves as the base class for different types of router events. Here are some commonly used router events:

1\. NavigationStart: This event is emitted when the navigation starts. It provides information about the URL being navigated to and any navigation extras that were passed during the navigation.

2\. RouteConfigLoadStart and RouteConfigLoadEnd: These events are emitted when lazy-loaded routes are being loaded. RouteConfigLoadStart is emitted when the loading of a lazy-loaded route starts, while RouteConfigLoadEnd is emitted when the loading is completed.

3\. RoutesRecognized: This event is emitted when the router recognizes the URL and determines the corresponding route configuration. It provides access to the activated route and the future route state.

4\. GuardsCheckStart and GuardsCheckEnd: These events are emitted when route guards are being checked. GuardsCheckStart is emitted when the guard checks start, and GuardsCheckEnd is emitted when the checks are completed.

5\. ResolveStart and ResolveEnd: These events are emitted when route data resolvers are being resolved. ResolveStart is emitted when the resolver starts resolving, and ResolveEnd is emitted when the resolution is completed.

6\. NavigationEnd: This event is emitted when navigation is successfully completed. It indicates that the router has successfully navigated to the desired route.

7\. NavigationCancel: This event is emitted when navigation is cancelled, typically due to a route guard returning false or a redirection.

8\. NavigationError: This event is emitted when navigation encounters an error, such as a failed HTTP request or an invalid route configuration.

By subscribing to router events, you can perform various actions or implement custom logic based on the navigation events occurring in your Angular application. For example, you can track navigation progress, display loading spinners, handle authentication checks, or log navigation events for analytics purposes.

You can subscribe to router events by injecting the Router service in your component and using the router.events observable to listen for events emitted by the router.

* ### **What is an Http Interceptor?**

In Angular, an HTTP interceptor is a feature that allows you to intercept HTTP requests and responses at the application level. It provides a way to modify the requests or responses globally before they are sent to the server or delivered to the calling code.

HTTP interceptors are useful for various purposes, such as adding authentication headers, logging requests, handling errors, modifying request parameters, or performing caching. They can be used to implement cross-cutting concerns in your application related to HTTP communication.

To create an HTTP interceptor in Angular, you need to implement the \`HttpInterceptor\` interface provided by the \`@angular/common/http\` module. This interface defines a single \`intercept\` method that you must implement. The \`intercept\` method receives an \`HttpRequest\` object and a \`HttpHandler\` object.

Inside the \`intercept\` method, you can perform actions before sending the request, such as modifying headers or request parameters. You can then invoke the \`next\` method of the \`HttpHandler\` to continue the request chain. By doing this, you can intercept the request and its subsequent responses, allowing you to modify or handle them as needed.

Here's an example of an HTTP interceptor in Angular:  
\`\`\`typescript  
import { Injectable } from '@angular/core';  
import { HttpInterceptor, HttpRequest, HttpHandler, HttpEvent } from '@angular/common/http';  
import { Observable } from 'rxjs';

@Injectable()  
export class MyInterceptor implements HttpInterceptor {  
  intercept(request: HttpRequest\<any\>, next: HttpHandler): Observable\<HttpEvent\<any\>\> {  
    // Perform actions before sending the request  
    // For example, add headers or modify request parameters

    // Continue the request chain  
    return next.handle(request);  
  }  
}  
\`\`\`

To make the interceptor active, you need to provide it in the \`providers\` array of your Angular module. For example, if you want to use the interceptor globally throughout your application, you can provide it in the root module (\`AppModule\`):

\`\`\`typescript  
import { NgModule } from '@angular/core';  
import { HTTP\_INTERCEPTORS } from '@angular/common/http';  
import { MyInterceptor } from './my-interceptor';

@NgModule({  
  providers: \[  
    { provide: HTTP\_INTERCEPTORS, useClass: MyInterceptor, multi: true }  
  \]  
})  
export class AppModule { }  
\`\`\`

By adding the interceptor to the \`HTTP\_INTERCEPTORS\` token and setting \`multi: true\`, you allow multiple interceptors to be registered simultaneously if needed.

With this setup, the \`intercept\` method of your interceptor will be called for each outgoing HTTP request, and you can modify the requests or handle the responses based on your requirements.

* ### **Authorisation and authentication method?**

Authentication and authorization are essential aspects of building secure web applications, including those developed with Angular. Here's an overview of these concepts in Angular:

**Authentication**:  
Authentication refers to the process of verifying the identity of a user. It ensures that the user is who they claim to be. In Angular, authentication typically involves:

1. User Login: The user provides their credentials (such as username and password) through a login form.  
2. Authentication Service: An Angular service handles the login process, validates the credentials, and issues an authentication token or session for the authenticated user.  
3. Token Storage: The authentication token or session is stored on the client-side (usually in local storage or cookies) for subsequent requests.  
4. Authentication Guards: Angular route guards, such as \`CanActivate\`, are used to restrict access to certain routes or features based on the user's authentication status.

**Authorization**:  
Authorization determines what actions or resources a user is allowed to access within an application. It involves defining roles or permissions and enforcing access control. In Angular, authorization typically involves:

1. User Roles/Permissions: Assigning different roles or permissions to users based on their level of access.  
2. Role-Based or Permission-Based Access Control: Implementing mechanisms to check if a user has the necessary role or permission to access certain routes, features, or data.  
3. Authorization Guards: Angular route guards, such as \`CanActivate\`, are used to check if a user has the required roles or permissions to access a specific route or feature.

To implement authentication and authorization in Angular, you may need to consider additional components such as authentication APIs, token-based authentication (e.g., JWT), server-side authentication validation, user registration, password reset, and user management.

Frameworks and libraries, such as Angular's HttpClient, JWT Interceptors, Angular Router, and Angular's built-in route guards, can be leveraged to implement these security features effectively. Additionally, server-side validation and secure communication protocols (HTTPS) play crucial roles in ensuring a secure authentication and authorization system.

It's important to design and implement these security measures carefully to protect sensitive user data and prevent unauthorised access to your Angular application and its resources.

* ### **JWT authentication.**

JWT (JSON Web Token) based authentication is a popular approach for implementing authentication in web applications, including those developed with Angular. Here's a general overview of how JWT-based authentication can be implemented in Angular:

1. **User Registration and Login**:  
* Implement user registration and login functionality in your Angular application. Users provide their credentials (such as username and password) and the server verifies them.  
* Upon successful authentication, the server generates a JWT containing user information and a signature.

2. **Token Storage**:  
* Store the JWT securely on the client-side. Common options include local storage, session storage, or cookies. Make sure to handle security considerations, such as XSS (Cross-Site Scripting) attacks.  
* The stored token will be sent with subsequent requests to the server for authentication and authorization.

3. **Interceptor for Token Handling**:  
* Create an Angular HTTP interceptor to intercept outgoing requests.  
* In the interceptor, append the JWT to the \`Authorization\` header of each request.  
* You can use Angular's \`HttpClient\` and its interceptors to achieve this.

4. **Token Validation and User Authentication**:  
* On the server-side, implement a token validation mechanism.  
* Verify the integrity of the received JWT using the signature and ensure it is not expired or blacklisted.  
* Extract user information from the token and use it to authenticate the user for each protected request.

5. **Secure Routes with Route Guards**:  
* Implement route guards in Angular to protect certain routes or features that require authentication.  
* Use Angular's \`CanActivate\` route guard to check if the user is authenticated before allowing access to the protected routes.

6. **Token Refresh (Optional)**:  
* If JWTs have an expiration time, implement a token refresh mechanism to obtain a new token without re-authentication.  
* Refresh tokens can be issued along with the initial token and used to request new tokens when the current one expires.

It's important to note that JWT-based authentication requires careful consideration of security measures, such as protecting against token tampering, securely storing and transmitting tokens, and handling token expiration and revocation.

Several libraries, such as \`jsonwebtoken\` for server-side token handling and Angular JWT Interceptor for client-side token management, can assist in implementing JWT-based authentication in an Angular application. Additionally, server-side frameworks and libraries (e.g. Node.js with Express or ASP.NET Core) can provide guidance on token generation, validation, and integration with your Angular application.

* ### **Lazy loading and eager loading?**

Lazy loading and eager loading are two different approaches for loading and initialising components or modules in software applications, including those built with the Angular framework. Let's explore each approach:

**Lazy Loading**:  
Lazy loading is a technique where modules or components are loaded only when they are required or accessed by the user. In other words, the application loads the necessary code on-demand rather than loading everything upfront. This can significantly improve the initial loading time and overall performance of an application, especially when dealing with large or complex applications.

With lazy loading in Angular, modules are divided into separate bundles, and each bundle is loaded dynamically when it is needed. For example, if an application has multiple feature modules, they can be lazy loaded so that each module is only loaded when the user navigates to a specific route that requires that module.

Benefits of lazy loading include reduced initial loading time, faster application startup, and improved performance by loading only the necessary code. It helps to optimise the loading process and provide a better user experience, especially for applications with a large codebase or complex feature sets.

**Eager Loading**:  
Eager loading, on the other hand, is the default loading behaviour in Angular. With eager loading, all the necessary modules and components are loaded upfront when the application is launched. This means that all the code required for the initial view is loaded immediately, regardless of whether it will be used right away or not.

Eager loading is simpler to implement and suitable for smaller applications where the initial loading time is not a significant concern. It is the default behaviour in Angular, where the main module and its dependencies are loaded eagerly when the application starts.

Eager loading is often appropriate for small to medium-sized applications or when the codebase is relatively small and doesn't impact performance significantly.

Both lazy loading and eager loading have their advantages and are used based on specific application requirements. Lazy loading is often used in larger applications with modular structures, where code splitting and on-demand loading are necessary to enhance performance. Eager loading is simpler and suitable for smaller applications where the initial loading time is not a concern or when immediate access to all modules is required.

* ### **What is Angular Library?**

A library is a collection of components, services, directives etc. that can be shared across different Angular projects.  
You generate a new library just like you would a component, service or anything else:  
ng g library mylibrary  
This will generate a new library mylibrary under the projects folder of your workspace.  
FYI, if we wanted to create an application, we could also run:  
ng g application myapp  
This will generate a new application mylibrary under THE SAME projects folder of your workspace.  
Angular Library vs Application  
Unlike an application, a library doesn't generate index.html, styles.css, polyfills.ts, main.ts. These files are specific to deploying an application in the browser. Since a library is simply a collection of reusable components, it doesn't need these files.  
Additionally, a library generates a few files that an application doesn't. Let's look at these in more detail...  
public\_api.ts  
This is the main entry file for your library. It defines what parts of the library are visible externally.  
Whenever you add a new component, service, etc. to your library, you also want to add it to this file so it can be exported at the class level. While exporting a new component in your library's .module.ts file will make it visible externally, adding to this file makes it possible to reference the class instance itself like..  
myLibComponent: MyLibComponent;  
ng-package.json  
This file is the configuration for ng-packagr, a library for packaging Angular projects into a distribution-ready npm package. The Angular CLI utilizes ng-packagr for packaging and publishing your library as an npm package.  
package.json  
This file is specific to your library and represents the package.json file that will be included with your packaged library. This file tells ng-packagr what dependencies should be included with the package.json file for the packaged library.

* ### **What is Json?**

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write and for machines to parse and generate. It is commonly used for transmitting data between a server and a web application, as well as for storing and exchanging data in various contexts.

Here are some key points about JSON:

1\. Structure: JSON data is represented in a structured format using key-value pairs. The data is organized into objects, which are enclosed in curly braces {}. Each object consists of one or more key-value pairs, where the key is a string and the value can be of various types, including strings, numbers, booleans, null, arrays, or nested objects.

2\. Example: Here's an example of a JSON object representing information about a person:

\`\`\`json  
{  
  "name": "John Doe",  
  "age": 30,  
  "isEmployed": true,  
  "hobbies": \["reading", "traveling", "photography"\],  
  "address": {  
    "street": "123 Main Street",  
    "city": "New York",  
    "country": "USA"  
  }  
}  
\`\`\`

3\. Data Exchange: JSON is commonly used for data exchange between a client and a server in web applications. It is lightweight and easily parsed by different programming languages, making it a popular choice for transmitting structured data over the network.

4\. Language Independence: JSON is not tied to any specific programming language and is widely supported. It is compatible with many programming languages and platforms, allowing data to be easily consumed and generated across different systems.

5\. Human Readable: JSON data is designed to be human-readable and easy to understand. The syntax is simple and straightforward, making it easy to write, read, and edit by developers.

6\. Widely Used: JSON is widely used in various contexts, including web development, APIs, configuration files, and data storage. It has become a standard format for representing and exchanging data due to its simplicity, versatility, and wide support.

7\. JSON Schema: JSON Schema is a vocabulary that allows the definition of JSON data structures, constraints, and validations. It provides a way to describe the expected structure and properties of JSON data, enabling data validation and documentation.

Overall, JSON is a popular and widely adopted format for representing structured data. Its simplicity, language independence, and human-readability have contributed to its widespread usage in modern web development and data exchange scenarios.

### **Advantages of Aot compilers in Angular?**

Ahead-of-Time (AoT) compilation is a technique used in the Angular framework to improve performance and reduce startup time of applications. Here are some advantages of AoT compilers in Angular:

1\. Faster Startup Time: AoT compilation precompiles Angular templates and generates optimised JavaScript code during the build process. This eliminates the need for the browser to perform the compilation at runtime, resulting in faster application startup times.

2\. Improved Performance: AoT-compiled applications tend to have better runtime performance compared to Just-in-Time (JIT) compiled applications. The generated code is optimised and can be executed more efficiently by the browser or JavaScript engine.

3\. Smaller Bundle Size: AoT compilation eliminates the need to ship the Angular compiler to the client's browser, reducing the overall bundle size. This is because the template compilation is done ahead of time during the build process, resulting in smaller JavaScript payloads.

4\. Template Error Checking: AoT compilation detects errors in Angular templates during the build process rather than at runtime. This helps catch potential issues early, reducing the chances of runtime errors and improving the stability of the application.

5\. Better Tree Shaking and Dead Code Elimination: AoT compilation enables better tree shaking, a process where unused code is removed from the final bundle. This can result in smaller bundle sizes and improved loading performance, as only the necessary code is included.

6\. Security: AoT compilation can provide a security benefit by hiding sensitive information in templates. Since the templates are compiled ahead of time, any sensitive data or logic embedded in the templates is not exposed to the client's browser.

Overall, AoT compilation in the Angular framework offers several advantages, including faster startup times, improved performance, smaller bundle sizes, enhanced error checking, better tree shaking, and increased security. These benefits contribute to a better user experience and more efficient Angular applications.

* ### **What is the endpoint?**

In Angular, an endpoint refers to the URL or route that you send an HTTP request to using the HttpClient module. An endpoint represents a specific resource or service on the server that you want to interact with.  
When making an HTTP request using the HttpClient module in Angular, you typically specify the endpoint as part of the request configuration. The endpoint can be a relative or absolute URL, depending on your requirements.

* ### How to add keys in objects?

To add more keys to an object in JavaScript, you can simply assign a new value to a new or existing key using dot notation or square bracket notation. Here are a few examples:

1\. Using dot notation:  
\`\`\`javascript  
const myObject \= { key1: 'value1' };  
myObject.key2 \= 'value2';  
myObject.key3 \= 'value3';

console.log(myObject);

Output:  
\`\`\`  
{  
  key1: 'value1',  
  key2: 'value2',  
  key3: 'value3'  
}  
In the above example, we add two new keys (\`key2\` and \`key3\`) to the \`myObject\` using dot notation (\`myObject.key2\` and \`myObject.key3\`), and assign values to them.

2\. Using square bracket notation:

\`\`\`javascript  
const myObject \= { key1: 'value1' };  
myObject\['key2'\] \= 'value2';  
myObject\['key3'\] \= 'value3';

console.log(myObject);

Output:  
\`\`\`  
{  
  key1: 'value1',  
  key2: 'value2',  
  key3: 'value3'  
}  
In this example, we use square bracket notation (\`myObject\['key2'\]\` and \`myObject\['key3'\]\`) to add new keys (\`key2\` and \`key3\`) to the \`myObject\` and assign values to them.

You can add as many keys as you want to an object using either dot notation or square bracket notation. Just make sure to provide a unique key name and assign a value to it.

* ### ActivatedRoute?

In Angular, the ActivatedRoute is a service that provides access to information about a route associated with a component. It contains details about the route's parameters, query parameters, URL segments, and other route data.

The ActivatedRoute is typically used within a component that corresponds to a specific route. It allows you to retrieve information about the current route and extract data from the route's parameters or query parameters.

Here's an example of how to use ActivatedRoute in Angular:

\`\`\`typescript  
import { ActivatedRoute } from '@angular/router';

@Component({  
  // component configuration  
})  
export class MyComponent {  
  constructor(private route: ActivatedRoute) {  
    this.route.paramMap.subscribe(params \=\> {  
      // Retrieve route parameters  
      const id \= params.get('id');  
      console.log('ID:', id);  
    });

    this.route.queryParamMap.subscribe(queryParams \=\> {  
      // Retrieve query parameters  
      const searchQuery \= queryParams.get('search');  
      console.log('Search query:', searchQuery);  
    });  
  }  
}  
\`\`\`

In the above example, the \`ActivatedRoute\` is injected into the component's constructor. By subscribing to the \`paramMap\` and \`queryParamMap\` observables of the \`ActivatedRoute\`, you can access the route parameters and query parameters, respectively.

\- The \`paramMap\` provides access to the route parameters. You can use the \`get()\` method to retrieve the value of a specific parameter, such as \`id\` in the example.  
\- The \`queryParamMap\` provides access to the query parameters. Similar to \`paramMap\`, you can use the \`get()\` method to retrieve the value of a specific query parameter, such as \`search\` in the example.

By using the ActivatedRoute, you can dynamically extract and use the information associated with the current route, enabling you to build more flexible and interactive components based on the route's context.

* ### **How to share data between modules?**

In Angular, there are several ways to share data between modules. Here are a few common approaches:

1\. **Shared Service**: Create a shared service that is provided at a higher level, such as in a common parent module or in the root module (\`AppModule\`). Components from different modules can then inject and use this shared service to share data.

   \- Create a service using the Angular CLI command: \`ng generate service shared\`  
   \- Add the necessary data sharing methods or properties in the shared service.  
   \- Provide the shared service in a higher-level module (e.g., \`AppModule\` or a common parent module).  
   \- Inject the shared service into the components from different modules that need to share data.  
   Example:  
   \`\`\`typescript  
   // shared.service.ts  
   import { Injectable } from '@angular/core';

   @Injectable()  
   export class SharedService {  
     sharedData: any;

     setSharedData(data: any) {  
       this.sharedData \= data;  
     }

     getSharedData() {  
       return this.sharedData;  
     }  
   }  
   \`\`\`  
   Components from different modules can inject and use this \`SharedService\` to share data:

   \`\`\`typescript  
   // Component in Module A  
   import { SharedService } from '../shared.service';

   constructor(private sharedService: SharedService) {}

   // Setting the shared data  
   this.sharedService.setSharedData(data);

   // Getting the shared data  
   const sharedData \= this.sharedService.getSharedData();  
   \`\`\`  
2\. **Event Emitter**: Use an event emitter to communicate and share data between components from different modules. Components can emit events with the shared data, and other components can subscribe to those events to receive the shared data.

   \- Create an event emitter service or utilise a shared service with an \`EventEmitter\` property.  
   \- Emit events with the shared data from one component.  
   \- Subscribe to the events in other components to receive the shared data.

   Example: \`\`\`typescript  
   // shared.service.ts  
   import { Injectable, EventEmitter } from '@angular/core';

   @Injectable()  
   export class SharedService {  
     sharedDataEvent: EventEmitter\<any\> \= new EventEmitter();

     emitSharedData(data: any) {  
       this.sharedDataEvent.emit(data);  
     }  
   }  
   \`\`\`  
   Components can emit and receive shared data using the event emitter:  
   \`\`\`typescript  
   // Component in Module A  
   import { SharedService } from '../shared.service';

   constructor(private sharedService: SharedService) {}

   // Emitting the shared data  
   this.sharedService.emitSharedData(data);

   // Component in Module B  
   import { SharedService } from '../shared.service';

   constructor(private sharedService: SharedService) {  
     // Subscribing to the shared data event  
     this.sharedService.sharedDataEvent.subscribe((data) \=\> {  
       // Handle the shared data  
       console.log(data);  
     });  
 }  
   \`\`\`  
3\. **State Management Libraries**: Utilise state management libraries like NgRx, Ngxs, or Akita. These libraries provide centralised stores to manage and share application state across different modules. Components can dispatch actions to modify the shared state, and other components can subscribe to the state changes.

   State management libraries often follow the Flux or Redux architecture pattern, which involves defining actions, reducers, and selectors to manage the state.

   Example using NgRx:

   \- Define actions, reducers, and selectors in the state management module.  
   \- Dispatch actions from components to modify the shared state.  
   \- Subscribe to the state changes in other components to receive the shared data.

   For more details, refer to the documentation of the specific state management library you choose to use.

These are some of the commonly used methods to share data between modules in Angular. The approach you choose depends on the complexity of your application and the specific requirements of data sharing.

* ### Learn some RXJS Operators.

* ### 1\. forkjoin, 2\. switchMap, 3\. mergeMap

The **forkJoin** operator is typically used when you want to wait for multiple Observables to complete and then work with their combined results. On the other hand, 

**mergeMap** is used when you want to transform each emitted value into an inner Observable and merge the emissions from those inner Observables into a single stream.  
Note that in newer versions of RxJS (v6+), the mergeMap operator has been renamed to flatMap, but the functionality remains the same.

* ### D/f b/w **local storage, cookies and session storage**.

**Storage Capacity**:

* Local Storage: Local storage provides a larger storage capacity compared to cookies and session storage. It typically allows storing several megabytes of data per domain.  
* Cookies: Cookies have a smaller storage capacity. They can store only a few kilobytes of data per cookie and have a maximum limit (typically around 4KB per domain) imposed by browser specifications.  
* Session Storage: Session storage has a capacity similar to that of local storage, allowing storage of several megabytes per domain.

**Data Persistence**:

* Local Storage: Data stored in local storage remains persistent until explicitly cleared by the user or removed programmatically.  
* Cookies: Cookies can be persistent or session-based. Persistent cookies have an expiration date and remain stored on the client-side until they expire. Session cookies are stored only for the duration of the browser session and are deleted when the browser is closed.  
* Session Storage: Data stored in session storage is specific to the current browsing session. It is cleared when the user closes the browser or navigates away from the page.

**Automatic Sending**:

* Local Storage: Data stored in local storage is not automatically sent to the server with each HTTP request. You need to manually retrieve the data and send it if needed.  
* Cookies: Cookies are automatically sent to the server with each HTTP request for the corresponding domain. This allows server-side processing and can be used for session management or authentication.  
* Session Storage: Data stored in session storage is not automatically sent to the server with each HTTP request. Similar to local storage, you need to explicitly retrieve and send the data if required.

**Security and Accessibility**:

* Local Storage: Local storage is accessible only to the client-side code running in the same domain. It is not accessible by the server or other domains. However, it is vulnerable to cross-site scripting (XSS) attacks if the code executing in the domain is compromised.  
* Cookies: Cookies are accessible by both the client-side code and the server. They can be set with specific attributes like \`HttpOnly\` to prevent client-side access and enhance security. Cookies are also subject to cross-site request forgery (CSRF) attacks if proper security measures are not implemented.  
* Session Storage: Similar to local storage, session storage is accessible only to the client-side code running in the same domain. It is not accessible by the server or other domains. However, it is also vulnerable to XSS attacks if the code executing in the domain is compromised.

**Usage and Purpose**:

*  Local Storage: Local storage is typically used for client-side data storage needs, such as caching application data, storing user preferences, or maintaining state across browser sessions.  
* Cookies: Cookies are often used for session management, user authentication, and tracking user behaviour. They can also be used for storing small amounts of data that need to be sent to the server with each request.  
* Session Storage: Session storage is commonly used for storing data specific to the current browsing session. It is useful for scenarios where data needs to be preserved within a session but not across multiple sessions or page refreshes.

* ### **Prototype**

In JavaScript, a prototype is an internal property of objects that allows objects to inherit properties and methods from other objects. Every object in JavaScript has a prototype, except for the base object, which is the root of the prototype chain.

Here are a few key points about prototypes in JavaScript:

1\. Prototype Chain:  
   \- Each object in JavaScript has a link to another object called its prototype.  
   \- When accessing a property or method on an object, if it doesn't exist on the object itself, JavaScript looks up the prototype chain to find the property or method in its prototype.  
   \- The prototype chain forms a series of linked objects, allowing for inheritance of properties and methods.

2\. Prototype Object:  
   \- The prototype of an object is stored in its \`\[\[Prototype\]\]\` property.  
   \- The prototype itself is an object, and it can have its own prototype, forming a chain.  
   \- The \`Object.prototype\` is at the top of the prototype chain and serves as the base object for all other objects.

3\. Prototypal Inheritance:  
   \- Prototypal inheritance is a mechanism where objects can inherit properties and methods from their prototype objects.  
   \- When a property or method is accessed on an object, if it doesn't exist on the object itself, it is searched in the prototype chain until it is found or until the chain reaches the end.

4\. Constructor Functions and Prototypes:  
   \- In JavaScript, constructor functions can be used to create objects with a shared prototype.  
   \- The \`prototype\` property of a constructor function is automatically assigned as the prototype of objects created using that constructor.  
   \- Properties and methods defined on the prototype are shared by all objects created by the constructor.

Prototypes play a fundamental role in JavaScript's object-oriented programming model, providing a mechanism for code reuse and inheritance. They allow objects to inherit and share properties and methods from other objects, promoting code efficiency and reducing redundancy.

It's important to note that with the introduction of ES6 classes, JavaScript provides a more syntactic and familiar class-based approach to object-oriented programming. However, classes in JavaScript are just a syntactic sugar layer on top of prototypes, and prototypes are still present and functioning under the hood.

* ### What is the scope of our angular application?

* ### How does an array work?

* ### ViewEncapsulation at component level?

* ### How to prevent modification of object property?

* ### What is the latest version of EcmaScript?

* ### How to read or extract the last element of an array?

* ### When do we use Input and Output decorator for data sharing?

* ### How to share data between siblings components?

* What are the advantages of JIRA?  
* Code to print alternate \* and \#  
* How to pass token

* ### **Design pattern in angular**

In the context of software development, a design pattern is a reusable solution to a commonly occurring problem in software design. Design patterns provide proven approaches and best practices for structuring code, organising components, and solving specific architectural or design challenges.

In Angular, design patterns can be applied at various levels, including component architecture, module organisation, data flow management, and more. Here are a few commonly used design patterns in Angular:

1\. Singleton Pattern:

* The Singleton pattern ensures that only one instance of a particular class exists throughout the application.  
* In Angular, services registered at the root level using the \`providedIn: 'root'\` metadata act as singletons, allowing shared data and functionality across components.

2\. Observer Pattern:

* The Observer pattern establishes a one-to-many relationship between objects, where changes in one object (subject) are automatically propagated to and reflected in other dependent objects (observers).  
* In Angular, this pattern is often used for event-driven communication and data sharing between components using services, event emitters, or RxJS observables.

3\. Factory Pattern:

* The Factory pattern provides an interface for creating objects without exposing the concrete implementation details.  
* In Angular, the Factory pattern can be implemented using dependency injection, where services act as factories for creating instances of other services or components.

4\. Decorator Pattern:

* The Decorator pattern allows adding additional behaviour or functionality to an object dynamically.  
* In Angular, decorators are used extensively to provide metadata and functionality to classes, components, services, and other Angular constructs.

5\. Strategy Pattern:

* The Strategy pattern defines a family of interchangeable algorithms and encapsulates each algorithm, making them interchangeable.  
* In Angular, this pattern can be used when different implementations or strategies need to be applied based on specific conditions or configurations.

These are just a few examples of design patterns that can be applied in Angular. Angular itself is built on several design patterns, including dependency injection, component-based architecture, and the observer pattern with RxJS.

Applying design patterns in Angular helps to improve code organisation, maintainability, reusability, and promotes a modular and scalable architecture. However, it's important to choose the right pattern based on the specific requirements and context of your application.

* Gdpr & cookies

General Data Protection Regulation bill introduced by EU.

## Flexbox & media queries

* Purpose: Media Queries primarily focus on adapting the design based on device characteristics, while Flexbox is a layout mechanism for arranging and aligning elements within a container.  
* Scope: Media Queries affect the overall layout and design of the page based on device conditions, whereas Flexbox deals with the internal arrangement of elements within a specific container.  
* Usage: Media Queries are typically used at the top-level CSS to define responsive behaviour for different screen sizes or devices. Flexbox is used within specific containers to achieve flexible and dynamic layouts.  
* Compatibility: Media Queries are widely supported in modern browsers and are part of the CSS3 specification. Flexbox has good browser support but may require vendor-specific prefixes for older versions of some browsers.

Project deploying process  
Project explain  
Your role on project  
What is json  
Form validations  
External script in angular  
Git repository  
Difference between component & module

* ### **Which type of data u get from api**

When working with APIs (Application Programming Interfaces), the type of data you receive can vary depending on the API and the specific endpoint you are interacting with. Here are some common data types that can be returned by APIs:

1\. JSON (JavaScript Object Notation):

* JSON is the most commonly used format for data exchange in APIs.  
* JSON is a lightweight data-interchange format that is easy for humans to read and write, and it is also easy for machines to parse and generate.   
* APIs often return JSON-formatted data, which consists of key-value pairs and nested structures.

2\. XML (eXtensible Markup Language):

* XML is another data format that APIs may use, although its usage has decreased in favour of JSON.  
* XML uses a hierarchical structure to represent data and is more verbose compared to JSON.  
* XML data can be parsed and processed using XML parsers or libraries.

3\. Text/Plain:

* APIs may return plain text data, such as log files, raw text content, or simple responses.  
* Plain text data can be received as a string and further processed as needed.

4\. Binary Data:

* APIs can also transmit binary data, such as images, audio files, or documents.  
* Binary data is typically received as a byte stream, which can then be processed or saved as needed.

5\. Form Data:

* APIs that handle form submissions or file uploads may return data in the form of multipart/form-data.  
* Form data can include text fields, files, or other input types.

It's important to review the API documentation or consult the API provider to understand the specific data format and structure returned by each API endpoint. The documentation will provide details on the expected data types, response formats, and any additional considerations for working with the API's data.

Sass : mixins , import   
Overwrite inline css from javascript   
Angular expression vs js expression  
choosing angular over other frameworks  
Using ngif vs ngifelse  
Html 5 tags  
Projects worked on

Short discussion of 15 mins  
\[9/19, 6:52 PM\] \+91 80807 38191: 1\) import html from asset folder it will have anchor links with href replace it with click event and append it in component html , After importing do we need to sanitize it

2\) if some Boolean property on ngoninit is set to true but on some components it is not getting set to true how to detect the change  
(Change detection)

3\) with AOT compilation build with staging environment compared to prod environment will it make the app slow

Router guards, promise vs observable, reactive forms ,directives , custom directives , pipes , lazy load  
\[9/19, 7:27 PM\] \+91 80807 38191: Validation of form control with regex ,   
Apply ,bind,call methods , closures , hoisting , callbacks, promise , observables, write one example of observable and promise, pipes , write syntax of custom pipe , routing , some basic js code based on hoisting (other interview), filter array based on condition  
\[9/20, 3:56 PM\] \+91 86683 77002: 1\) What is roles and responsibilities in your project?  
2\) what is your daily routine in work time?  
3\) diff netween components and directives?  
4\) what are pipes and types?  
5\) expalin in brief angular guards?  
6\) explain in brief angular life cycle hooks and explain one by one.  
7\) why typescript is better?  
8\) what is aot and jit?  
9\) data sharing   
10\) how to achieve asynchronous operation in brief?  
11\) mvvm architecture  
12\) what are decorators.  
13\) single page app vs multipage application.  
14\) how to install third party liabrary?  
15\) Higher order components.  
16\) string interpolation.  
\[9/20, 3:56 PM\] \+91 86683 77002: 1\) what is callback function?  
2\) explain async await.  
3\) what is promises and observable?  
4\) what is  filter method and map method ? Which one is better  
5\) rxjs operator  
6\) if we have an array of object then how to push a new key value pair in each object ?  
7\) what is an object in js?  
8\) how to compare two object in js?  
9\) what is callback hell?  
\[9/20, 5:12 PM\] \+91 86683 77002: 1)Single page app vs multipage app  
2\) component communication  
3\) directive vs components  
4\) expalin in brief lifecycle hooks in angular   
5\) guards in angular  
6\) promises and observable  
7\) diff between map and filter  
8\) diff between localstorage vs session storage vs cookies  
9\) clousers in js  
10\) how to improve performance of angular app  
11\) advantages of angular  
12\) datatypes in js  
13\) why typescript  
14\) js prototypes  
15\) router in angular  
16\) html new features  
17\) how to make application responsive  
18\) diff between media query and boot strapp  
19\) box model   
20\) flexbox  
21\) what you did in your project  
22\) how to achieve asynchronous operation  
23\) what is daily routine  
\[9/20, 5:44 PM\] \+91 80807 38191: Reverse each word from sentence (Note: without using any built in function)  
i/n \-\> "my name is abc"  
o/p-\> "ym eman si cba"

let a \= "my name is abc"

let rev \= ''  
let arr \=\[\]  
for(let i=0;i\<a.length; i++){  
   
   
   
    if(a\[i\] \== ' '){  
        arr.push(rev)  
        rev \= ''  
    }else{  
        rev \+= a\[i\]  
    }  
      
}  
arr.push(rev)  
let newstr \= ''  
for(let k \=0; k\<arr.length;k++){  
    for(let j \=arr\[k\].length-1 ;j\>=0;j--){  
        newstr \+= arr\[k\]\[j\]  
    }  
    newstr \+= ' '

}

console.log(arr)  
console.log(newstr)  
\[9/22, 10:04 AM\] \+91 94219 49590: 1\) What is interceptor ?  
2\) What is json ?  
3\) Explain Project in details \-  
4\) Roles & responsibilities in project ?  
5\) Explain all about pipe ?  
6\) explain in details decorators ?

my interview questions \-  
\[9/22, 11:15 AM\] Priti Velocity: 1Observable,  
2What use for authentication,  
3How to manage session storage  
4Directive,  
5Statement management  
6Filter data without using any filter program   
7Behavioural subject  
8The ways of share data between components  
9How can manage the user data when session is expired  
10.When we route one page to another their is page loading  
11What  is module and it's types  
12.lazyloading working  
13.what is data mapping

\[05/02, 8:59 pm\] Amol Reddy: 1.What is single page application  
2.life cycle hooks difference bet ngoninit & constructor   
3\. Detailed explanation about ngoninit, ngdocheck, ngonchange   
4.what is authentication & authorisation   
5\. Why we use JWT token   
6\. What is the difference between observable , promise and subject  
7.why we use route guards explain canactivate , canload, candeactivate  
8.what is http interceptor   
9.what is service, why & how it is use in ur application   
10\. difference between angular and angularJS  
11\. Angular versions & difference bet each one  
12.what are directives and decorator  
13\. In how many ways we can bind data in SPA  
14\. Where do u use @input & @output decorator   
15.tell me about reactive form & template driven form

\[05/02, 8:59 pm\] Amol Reddy: 1\) What is roles and responsibilities in your project?  
2\) what is your daily routine in work time?  
3\) diff netween components and directives?  
4\) what are pipes and types?  
5\) expalin in brief angular guards?  
6\) explain in brief angular life cycle hooks and explain one by one.  
7\) why typescript is better?  
8\) what is aot and jit?  
9\) data sharing   
10\) how to achieve asynchronous operation in brief?  
11\) mvvm architecture  
12\) what are decorators.  
13\) single page app vs multipage application.  
14\) how to install third party liabrary?  
15\) Higher order components.  
16\) string interpolation.

\[05/02, 8:59 pm\] Amol Reddy: 1\) What is roles and responsibilities in your project?  
2\) what is your daily routine in work time?  
3\) diff netween components and directives?  
4\) what are pipes and types?  
5\) expalin in brief angular guards?  
6\) explain in brief angular life cycle hooks and explain one by one.  
7\) why typescript is better?  
8\) what is aot and jit?  
9\) data sharing   
10\) how to achieve asynchronous operation in brief?  
11\) mvvm architecture  
12\) what are decorators.  
13\) single page app vs multipage application.  
14\) how to install third party liabrary?  
15\) Higher order components.  
16\) string interpolation.

\[05/02, 8:59 pm\] Amol Reddy: 1\) what is callback function?  
2\) explain async await.  
3\) what is promises and observable?  
4\) what is  filter method and map method ? Which one is better  
5\) rxjs operator  
6\) if we have an array of object then how to push a new key value pair in each object ?  
7\) what is an object in js?  
8\) how to compare two object in js?  
9\) what is callback hell?

\[05/02, 8:59 pm\] Amol Reddy: What are observables in angular?  
Promise in javascript.  
Lifecycle hooks in angular.  
Difference between library and framework.  
How does angular application bootstrap.  
Git and GitHub related questions.  
Custom pipes in angular.  
Different types of subject.  
Difference between observables and subject.  
How to pass data from child to parent component.  
Why are services used in angular.  
Hoisting in javascript.  
Difference between javascript and typescript.  
Ng serve and ng build difference.  
Arrow function in typescript.  
View child and view children in angular.

\[05/02, 8:59 pm\] Amol Reddy: 1)Single page app vs multipage app  
2\) component communication  
3\) directive vs components  
4\) expalin in brief lifecycle hooks in angular   
5\) guards in angular  
6\) promises and observable  
7\) diff between map and filter  
8\) diff between localstorage vs session storage vs cookies  
9\) clousers in js  
10\) how to improve performance of angular app  
11\) advantages of angular  
12\) datatypes in js  
13\) why typescript  
14\) js prototypes  
15\) router in angular  
16\) html new features  
17\) how to make application responsive  
18\) diff between media query and boot strapp  
19\) box model   
20\) flexbox  
21\) what you did in your project  
22\) how to achieve asynchronous operation  
23\) what is daily routine

\[05/02, 8:59 pm\] Amol Reddy: what is array  
how we can access element of array  
what is map method  
for each  
what is difference between map and for each  
what is html  
how to creat dropdown  
what is selector  
what is decorator and its types  
difference between observable and observer  
what is fork joint  
\----------------------------------------------------

### **How to access html tag in typescript file** 

Template Reference Variables:

* Add a template reference variable to the HTML element by using the \# symbol followed by a name, such as \<div \#myElement\>\</div\>.  
* In the TypeScript code, access the element using @ViewChild or @ViewChildren decorators. For example:  
  import { Component, ViewChild, ElementRef } from '@angular/core';  
    
  @Component({  
    // ...  
  })  
  export class MyComponent {  
    @ViewChild('myElement', { static: true }) myElementRef: ElementRef;  
      
    ngAfterViewInit() {  
      console.log(this.myElementRef.nativeElement);  
    }  
  }

### **What is diff between CSS & SCSS**

CSS (Cascading Style Sheets) and SCSS (Sassy CSS) are both style sheet languages used for styling web pages. However, there are some key differences between them:

CSS:  
\- CSS is the standard style sheet language for the web and is supported by all modern web browsers.  
\- It uses a simple syntax with a set of predefined properties and values.  
\- CSS files have a \`.css\` extension.  
\- It does not support variables, functions, or nested rules out of the box.  
\- CSS requires writing repetitive code for things like vendor prefixes and inheritance.  
\- It is not as modular or reusable as SCSS.

SCSS:  
\- SCSS is a superset of CSS that extends its functionality and provides additional features.  
\- SCSS files have a \`.scss\` extension.  
\- It introduces new features like variables, nesting, mixins, functions, and inheritance.  
\- SCSS allows you to write more modular, reusable, and maintainable styles.  
\- It supports nested rules, which makes the structure of the styles more clear and organized.  
\- SCSS provides the ability to use variables to store and reuse values, making it easier to maintain consistent styles.  
\- It allows the use of functions and mixins to encapsulate and reuse styles or perform calculations.  
\- SCSS needs to be compiled into plain CSS before it can be used in a web browser. This can be done using tools like Sass or by configuring build processes in frameworks like Angular or React.

In summary, SCSS is an extension of CSS that provides additional features, such as variables, nesting, and mixins, to make styling more modular and reusable. It needs to be compiled into CSS before it can be used in web browsers, while CSS is the standard style sheet language natively understood by web browsers.

### **What is EC2 in AWS?**

Amazon Elastic Compute Cloud (Amazon EC2) is a web service provided by Amazon Web Services (AWS) that allows you to create and manage virtual servers, known as instances, in the cloud. EC2 provides scalable computing capacity and enables you to quickly provision virtual machines with various operating systems and configurations.

Here are some key features and concepts related to Amazon EC2:

1\. Instances: These are virtual machines running in the cloud. You can launch instances with different specifications, such as CPU, memory, storage, and networking capacity, based on your requirements.

2\. Amazon Machine Images (AMIs): AMIs are pre-configured templates that contain the necessary operating system, software, and configurations required to launch an instance. AWS provides a wide range of AMIs, including popular operating systems and pre-installed software.

3\. Instance Types: EC2 offers a variety of instance types optimized for different use cases, such as general-purpose, compute-optimized, memory-optimized, and storage-optimized instances. Each instance type has its own combination of CPU, memory, storage, and networking capabilities.

4\. Regions and Availability Zones: EC2 is available in multiple geographic regions worldwide. Each region consists of multiple isolated data centers called Availability Zones (AZs). You can choose the region and AZs where your instances are deployed to achieve high availability and fault tolerance.

5\. Elastic IP Addresses: An Elastic IP address is a static, public IPv4 address that can be associated with an EC2 instance. It allows you to have a persistent IP address for your instance, even if it is stopped or restarted.

6\. Security Groups: Security groups act as virtual firewalls for your instances. They control inbound and outbound traffic by specifying rules that allow or deny access based on protocols, ports, and source IP ranges.

7\. Auto Scaling: EC2 Auto Scaling automatically adjusts the number of instances based on predefined conditions, such as increased traffic or CPU utilization. It helps ensure that your applications have the right amount of compute capacity at all times.

8\. Load Balancers: Elastic Load Balancing (ELB) distributes incoming traffic across multiple EC2 instances to improve application availability and scalability. It automatically scales with your traffic and provides fault tolerance by routing requests only to healthy instances.

Amazon EC2 is widely used for various purposes, including web hosting, running applications, batch processing, machine learning, and more. It provides a flexible and scalable infrastructure that allows businesses to easily provision and manage virtual servers in the cloud, paying only for the resources they consume.

### What is a Deployment pipeline?

\#\# Deployment Pipeline Overview

* A deployment pipeline is a system of automated processes for moving new code additions and updates from version control to production.  
* Automation in deployment pipelines reduces manual tasks, allowing for quicker and more accurate code updates.

\#\# Main Stages of a Deployment Pipeline

* The main stages of a deployment pipeline include version control, acceptance tests, independent deployment, and production deployment.  
* Each stage focuses on automated processes to ensure code quality and functionality.

\#\# Benefits of a Deployment Pipeline

* Deployment pipelines enable faster release of product updates and features.  
* They reduce the chance of human error by eliminating manual steps, and facilitate troubleshooting and rollback to previous versions.

\#\# How to Build a Deployment Pipeline

* Building a deployment pipeline requires upfront planning and creation of tests.  
* The primary goals are eliminating manual steps and automating compilation, testing, and deployment of code.

\#\# Continuous Integration (CI) and Continuous Delivery (CD) Pipelines

* CI/CD pipelines continuously compile, validate, and deploy new code updates, enabling faster and more frequent updates.  
* They introduce automated steps for improved accuracy and efficiency.

\#\# Deployment Pipeline Tools

* Useful tools for building a deployment pipeline include Jenkins, Azure DevOps, CodeShip, and PagerDuty.  
* These tools help automate and optimise the pipeline process.

\#\# Additional Resources

* PagerDuty offers additional resources, including blog posts, support documentation, and customer stories.  
* They also provide solutions for specific industries and use cases.

\#\# Privacy Settings

* You can choose not to allow some types of cookies.  
* Blocking some types of cookies may impact your site experience.

\#\# Cookie Types

* Strictly Necessary Cookies: Necessary for website functionality.  
* Performance Cookies: Help measure and improve site performance.

### **What does the HTML meta tag contain?**

The HTML meta tag is an element used in the head section of an HTML document to provide metadata about the document. It includes information such as character encoding, viewport settings for responsive web design, page description, keywords, author and copyright information, and options for refreshing or redirecting the page. The meta tag is essential for providing additional context and instructions to browsers and search engines.

