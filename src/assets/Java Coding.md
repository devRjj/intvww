# Java Coding

# Which method will be called?

class A {  
    static void add(int a, int b) {  
   	 System.out.println("Class a "+ a+b);  
    }  
}

class B extends A {

    static void add(int a, int b) {  
   	 System.out.println("Class b "+ a+b);  
    }  
}

public class C extends B {

    public static void main(String args\[\]) {  
   	 A b \= new B();  
   	 b.add(4, 6);  
    }  
}

# Find the 2nd largest number from the given array using Java8

1. int x\[\] \= { 51, 34, 70, 4, 26, 55, 4, 19, 55, 23, 17, 70, 42, 57, 51, 70 };

   	 Set\<Integer\> st \= new TreeSet\<Integer\>();

   	 for (int i=0; i\<x.length; i++) {  
   		 st.add(x\[i\]);  
   	 }

   	 List\<Integer\> li \= new ArrayList\<\>();  
   	 li.addAll(st);

   	 Integer integer \= li.get(li.size() \- 2);

   	 System.out.println(integer);	

2. List\<Integer\> ls \= Arrays.asList( 51, 34, 70, 4, 26, 55, 4, 19, 55, 23, 17, 70, 42, 57, 51, 70);  
     
       	Optional\<Integer\> secondLargest \= ls.stream()  
               	.distinct()  
               	.sorted(Collections.reverseOrder())  
               	.skip(1)  
               	.findFirst();  
     
       	System.out.println(secondLargest);

# Write a program to print the length of each string in a list of strings.

List\<String\> stringList \= Arrays.asList("Hello", "World", "Java", "Programming", "OpenAI");

for (String str : stringList) {  
   System.out.println("String: \\"" \+ str \+ "\\" has length: " \+ str.length());  
}  
Rotate an array by right using case steps.

# Write a java program to find the length of a String without using length, size.

public class StringLengthWithoutLengthMethod {  
    public static void main(String\[\] args) {  
        String str \= "Hello, World\!";  
          
        int length \= getStringLength(str);  
          
        System.out.println("The length is \\"" \+ str \+ "\\" is: " \+ length);  
    }

    public static int getStringLength(String str) {  
        int count \= 0;

        // Iterate through the string until we reach the null character  
        while (true) {  
            try {  
                // Accessing each character by its index  
                char c \= str.charAt(count);  
                count++;  
            } catch (IndexOutOfBoundsException e) {  
                // Break the loop when we go out of bounds  
                break;  
            }  
        }  
          
        return count; // Return the total count  
    }  
}

# String str \= "JAVA"; write the program to print non repeated values (O/P: J,V).

public static void nonRepeatedChar(String str){  
    	Map\<Character, Integer\> uniqueChar \= new HashMap\<\>();

    	for(char c: str.toCharArray()){  
        	uniqueChar.put(c, uniqueChar.getOrDefault(c, 0\) \+ 1);  
    	}

    	for(char c: uniqueChar.keySet()){  
        	if(uniqueChar.get(c) \== 1){  
            	System.out.println(c+ " ");  
        	}  
    	}  
}  
\=================================for Integer list  
public static void nonRepeatedInteger(List\<Integer\> num){  
    	Map\<Integer, Integer\> uniqueInt \= new HashMap\<\>();

    	for(int i: num){  
        	uniqueInt.put(i, uniqueInt.getOrDefault(i, 0\) \+1);  
    	}

    	for(int j: uniqueInt.keySet()){  
        	if(uniqueInt.get(j) \== 1){  
            	System.out.println(j+ " ");  
        	}  
    	}  
}  
\==================================with StreamApi  
public static void nonRepeatedIntegerWithStream(List\<Integer\> num) {  
    	// Count occurrences using Streams  
    	Map\<Integer, Long\> uniqueInt \= num.stream()  
            	.collect(Collectors.groupingBy(i \-\>   
i, Collectors.counting()));

    	// Print non-repeated integers  
    	uniqueInt.entrySet().stream()  
            	.filter(entry \-\> entry.getValue() \== 1\)  
            	.map(Map.Entry::getKey)  
            	.forEach(System.out::println);  
}

# Sort a map by value where String is key, Integer is value.

15\. File having 10L lines of text, read and store it in Hashmap

# Write a program to achieve Runtime polymorphism.

To demonstrate runtime polymorphism in Java, we can create a simple example using method overriding. In this example, we'll define a base class and a couple of derived classes that override a method from the base class. When we call the overridden method using a reference of the base class type, the actual method that gets executed will depend on the object type at runtime.

Example: Runtime Polymorphism in Java  
\`\`\`java  
// Base class  
class Animal {  
	public void makeSound() {  
    	System.out.println("Animal makes a sound");  
	}  
}

// Derived class Dog  
class Dog extends Animal {  
	@Override  
	public void makeSound() {  
    	System.out.println("Dog barks");  
	}  
}

// Derived class Cat  
class Cat extends Animal {  
	@Override  
	public void makeSound() {  
    	System.out.println("Cat meows");  
	}  
}

// Main class to test polymorphism  
public class Main {  
	public static void main(String\[\] args) {  
    	// Creating references of type Animal  
    	Animal animal1 \= new Animal(); // Animal object  
    	Animal animal2 \= new Dog(); 	// Dog object  
    	Animal animal3 \= new Cat(); 	// Cat object

    	// Calling the makeSound method on each object  
    	animal1.makeSound(); // Output: Animal makes a sound  
    	animal2.makeSound(); // Output: Dog barks  
    	animal3.makeSound(); // Output: Cat meows  
	}  
}  
\`\`\`  
Explanation:

1. Base Class (\`Animal\`)\*\*: This class has a method \`makeSound()\` that prints a generic message.  
2. Derived Classes (\`Dog\` and \`Cat\`): Both classes extend \`Animal\` and override the \`makeSound()\` method to provide specific implementations for dogs and cats.  
3. Main Class: In the \`main\` method, we create references of type \`Animal\` that point to objects of \`Animal\`, \`Dog\`, and \`Cat\`.

When we call \`makeSound()\` on these references, the Java Virtual Machine (JVM) determines which method to execute based on the actual object type at runtime, not the reference type.

Output: When you run this program, you will see the following output:  
\`\`\`  
Animal makes a sound  
Dog barks  
Cat meows  
\`\`\`

* Runtime Polymorphism\*\*: This is achieved through method overriding. The method that gets executed is determined at runtime based on the actual object type.  
* Dynamic Method Dispatch\*\*: This is another term for runtime polymorphism, where the call to an overridden method is resolved during execution.  
* Flexibility\*\*: This allows for more flexible and reusable code since you can work with base class references while still invoking subclass behavior.

This example effectively illustrates how runtime polymorphism works in Java through inheritance and method overriding.  
4\. Write a pgm to check string2 is substring of string1 or not

# How to create custom exceptions.

// Custom exception class  
class InvalidAgeException extends Exception {  
    public InvalidAgeException(String message) {  
        super(message);  
    }  
}

// Class for age validation  
class AgeValidator {  
    public static void validateAge(int age) throws InvalidAgeException {  
        if (age \< 0\) {  
            throw new InvalidAgeException("Age cannot be negative: " \+ age);  
        }  
        System.out.println("Valid age: " \+ age);  
    }  
}

// Main class to test the custom exception  
public class Main {  
    public static void main(String\[\] args) {  
        try {  
            AgeValidator.validateAge(-5); // This will throw InvalidAgeException  
        } catch (InvalidAgeException e) {  
            System.out.println("Caught exception: " \+ e.getMessage());  
        }

        try {  
            AgeValidator.validateAge(25); // This will be valid  
        } catch (InvalidAgeException e) {  
            System.out.println("Caught exception: " \+ e.getMessage());  
        }  
    }  
}

# Reverse a string without any predefined methods.

String str \= "devraj";  
    	String res \= "";  
    	for(int i=str.length()-1; i\>=0; i--){  
        	res \+= str.charAt(i);  
    	}  
System.out.println("Reverse is "+ res);

Write a native query to fetch EmpName, EmpDesignation using EmpID

# List\<Integer\> numbers \= Arrays.asList(10, 15, 8, 49, 25, 98, 32, 10);

## **Find Even Numbers**

To filter out even numbers from the list:  
List\<Integer\> evenNumbers \= numbers.stream()  
    .filter(num \-\> num % 2 \== 0\)  
    .collect(Collectors.toList());

System.out.println("Even Numbers: " \+ evenNumbers);

## **2\. Find Duplicate Values**

To find duplicate values in the list:  
List\<Integer\> duplicates \= numbers.stream()  
    .filter(num \-\> Collections.frequency(numbers, num) \> 1\)  
    .distinct() // To avoid listing the same duplicate multiple times  
    .collect(Collectors.toList());

System.out.println("Duplicate Values: " \+ duplicates);

## **4\. Find Values That Start With "1"**

Since we are dealing with integers, we will convert them to strings to check if they start with "1":  
java  
List\<Integer\> startsWithOne \= numbers.stream()  
    .filter(num \-\> String.valueOf(num).startsWith("1"))  
    .collect(Collectors.toList());

System.out.println("Values that start with '1': " \+ startsWithOne);

find the num of occurnces of each letter in below String using java8  
String str \= "hyujikoyhfrtuj";  
18\. Employee object \-\> sort the by employee name using Java8 and explain  
19\. Employee object \-\> group by gender using Java8 and explain  
What is the o/p of below code  
public class StringBasics {  
public static void main(String\[\] args) {   
String s1 \= "hello";  
String s2 \= new String("hello");  
String s3 \= "hello";

if (s1 \== s2) {  
System.out.println("s1 and s2 equal");  
} else {  
System.out.println("s1 and s2 not equal");  
 }

if (s1 \== s3) {  
System.out.println("s1 and s3 equal"); \--  
} else {  
System.out.println("s1 and s3 not equal");  
}  
}  
}

# How many objects will b created by below code 

String s1 \= new String("javaguides");  
String s2 \= "javaguides";

* Two objects will be created.

convert below string array to list  
String\[\] str \= { "hello", "world", "how", "are", "you", "I", "am", "fine" };  
Find min length of string in above array using java8.

Check "A11" is exist in this arrays or not using java8  
String\[\] str1 \= new String\[\] { "A01", "A02", "A01" };  
String\[\] str2 \= new String\[\] { "A11", "A12", "A13" };

Is the below code correct ?  
@FunctionalInterface interface Test{  
void say(String msg);  
// Object class methods. int hashCode();  
}  
The code you provided is almost correct, but it contains a misunderstanding regarding the use of the `@FunctionalInterface` annotation in Java.

## **Explanation of the Code**

1. **Functional Interface**: A functional interface is an interface that contains exactly one abstract method. This allows instances of functional interfaces to be created using lambda expressions or method references.  
2. **Object Class Methods**: The `Object` class methods (like `hashCode()`, `equals()`, etc.) are not considered abstract methods in the context of a functional interface. They are inherited from the `Object` class and do not count against the single abstract method requirement.

## **Corrected Code**

Here’s how you can define a functional interface correctly:  
java  
`@FunctionalInterface`  
`interface Test {`  
    `void say(String msg); // This is the single abstract method.`  
    `// The following line is commented out because it would cause a compilation error.`  
    `// Object class methods like hashCode() should not be declared here.`  
    `// int hashCode(); // This line should be removed or commented out.`  
`}`

## **Key Points**

* **Single Abstract Method**: The interface `Test` has one abstract method `say(String msg)`, which is correct for a functional interface.  
* **Inherited Methods**: Methods from the `Object` class (like `hashCode()`, `equals()`, etc.) do not count as abstract methods for the purposes of defining a functional interface. You do not need to declare them explicitly in your interface.  
* **Compilation Error**: If you include `int hashCode();` as an explicit method in your interface, it will cause a compilation error because it would then have two abstract methods (the one you defined and the one inherited from `Object`).

## **Example Usage**

Here’s how you might use this functional interface with a lambda expression:  
java  
`public class Main {`  
    `public static void main(String[] args) {`  
        `Test test = msg -> System.out.println("Message: " + msg);`  
        `test.say("Hello, Functional Interface!");`  
    `}`  
`}`

## **Summary**

The corrected definition of your functional interface should only include the unique abstract method you want to define, without explicitly declaring methods inherited from the `Object` class. The rest of your code regarding usage and definition was on the right track\!

8\. Print the emp name whose salary is \>10000 in sorted order without any duplicates.

Print the name of the employee whose salary is \>20000 using streams api.

2\. Print num of occurrences of each word in a given string.  
String str \= “big black bug bit a big black dog on his big black nose”

Print the values which starts with 1 in the given below list.  
list (10,15,8,49,25,98,98,32,15)

Write a java program to check if any number given as input is the sum of 2 prime numbers.

# Check if the number is an Armstrong number.

class HelloWorld {  
	public static void main(String\[\] args) {  
    	int x \= 407;  //0, 1, 153, 370, 371 and 407 are the Armstrong numbers.  
    	int z \= x;  
    	int arms \= 0;

    	while(x\>0){  
   		 int y \= x%10;  //remender \-\> 2  
   		 arms \+= y\*y\*y; //arms \= arms \+ y^3  
   		 x \= x/10;  
    	}  
   	   
    	if(z==arms){  
       	System.out.print("This is an Armstrong number");  
    	} else{  
        	System.out.print("This is not an Armstrong number");  
    	}  
	}  
}

# Palindrome number.

int x \= 1441;    
    	int p \= x;  
    	int rev \= 0;  
   	   
    	while(x \> 0){  
        	int z \= x%10;  
        	rev \= rev\*10 \+ z;  
        	x \= x/10;  
    	}  
   	   
    	if(p==rev){  
       	System.out.print("This is a pallindrome number");  
    	} else{  
        	System.out.print("This is not a Pallindrom number");  
    	}