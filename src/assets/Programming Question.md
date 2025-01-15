# **Programming Question**

# Find nth non-repeating character.

import java.util.HashMap;  
import java.util.LinkedHashMap;  
import java.util.List;  
import java.util.Map;

public class SecondNonRepeatingCharacter {  
	public static void main(String\[\] args) {  
    	String str \= "ahellohworld";

    	Map\<Character, Integer\> mp \= new LinkedHashMap\<\>();  
//    	Map\<Character, Integer\> mp \= new HashMap\<\>();  
//    	This will HashMap() is not suitable for solving this qeustion because.  
    	char\[\] charArray \= str.toCharArray();

    	for(char c: charArray){  
        	mp.put(c, \!mp.containsKey(c)?1:mp.get(c)+1);  
    	}

    	Character nonRepeating \= mp.entrySet().stream()  
            	.filter(e-\>e.getValue()==1)  
            	.skip(1)  
            	.findFirst()  
            	.get()  
            	.getKey();

    	System.out.println(ls);  
}  
}  
**Order of Iteration:**

* **LinkedHashMap**: Preserves the insertion order of key-value pairs. This means the order in which you put elements into the map is the order in which they will be iterated over.  
* **HashMap**: Does not guarantee any specific order of iteration. The order may vary unpredictably across different Java versions or even between different runs of the same program.

**Use Cases:**

* **LinkedHashMap:** Suitable when the order of elements is important. For example:  
  * Maintaining the order of elements in a cache.  
  * Implementing a Least Recently Used (LRU) cache.  
  * Creating ordered logs or history.  
* **HashMap:** Generally more efficient for general-purpose key-value storage where order is not a concern. Offers faster insertion and retrieval times compared to LinkedHashMap.

In the above code:

* **Using LinkedHashMap:** The nonRepeating variable will always hold the second non-repeating character encountered in the string. This is because LinkedHashMap maintains the order of insertion, so the skip(1) operation will skip the first non-repeating character and return the second one.  
* **Using HashMap:** The ls variable will hold an arbitrary non-repeating character. Since the order of iteration is not guaranteed, the skip(1) operation will skip an unpredictable character, and the result will be non-deterministic.

**In summary:** If you need to maintain the order of elements as they were inserted, use LinkedHashMap. If order is not a concern and you prioritize performance, use HashMap.

# Sum of list of numbers using stream

# Find Average of list of numbers

# Square of each number

# Find numbers that starts with 2

# Find duplicate elements from the list

# Find maximum and minimum

# Sort numbers in ascending and descending

# Find duplicate characters in a string.

# Elements and their count in string.

# Maximum marks of students.

al.stream().collect(Collectors.maxBy(Comparator.comparing(Student::getMarks)))  
.isPresentOrElse(  
e-\>System.out.println(“Highest marks: ”+e.getMarks()),   
	()-\>System.out.println(“Marks not found”))