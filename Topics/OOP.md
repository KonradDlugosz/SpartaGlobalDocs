# Object Oriented Programming



### Index:

1. [**Java concepts**](#Java-Concepts:)
   1. [What is OOP ?](#What-is-OOP-?)
   2. [Strings](#Strings)
   3. [Data types](#Data-types)
   4. [Classes/Objects](#Classes/Objects)
   5. [Class methods](#Class-methods-(Static---Non-Static))
   6. [Java constructors](#Java-Constructors)
   7. [Modifiers](#Modifiers)
   8. [Encapsulation](#**Encapsulations**) 
   9. [Inheritance](#**Inheritance** ) 
   10. [Polymorphism](#Polymorphism) 
   11. [Abstract](#Abstract)
   12. [Interfaces](#**Interfaces**) 
   13. [Recursion](#Recursion) 
   14. [Regular Expression](#**Regular Expression** )
   15. [SOLID](#SOLID)
   16. [Collections](#Collections)
   17. [Iterator](#Iterator)
2. [**Design patterns**](#Design-patterns)

### Java Concepts:

1. #### **What is OOP ?** 

   OOP stands for **Object-Oriented Programming**.

   Procedural programming is about writing procedures or methods that perform operations on the data, while object-oriented programming is about creating objects that contain both data and methods.

   Object-oriented programming has several advantages over procedural programming:

   - OOP is faster and easier to execute
   - OOP provides a clear structure for the programs
   - OOP helps to keep the Java code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
   - OOP makes it possible to create full reusable applications with less code and shorter development time

   **Tip:** The "Don't Repeat Yourself" (DRY) principle is about reducing the repetition of code. You should extract out the codes that are common for the application, and place them at a single place and reuse them instead of repeating it.

   

   Classes and objects are the two main aspects of Object-Oriented Programming.

   Example one:

   `Class: Fruit` 

   `Object: Apple, Banana, Mango`

   

   Example two:

   `Class: Car` 

   `Object: Volvo, Audi, Toyota`

   

2. #### Strings

   `Strings` object are immutable and can be shared by storing them in a pool of strings.

   String can be created from `String` literal unlike any other classes. 

   `String s = "hello World!"`

   `String s1 = "hello World!"`

   `s == s1`  - This would be true as the string already exists in the pool string therefore the reference would be the same. 

   `s.equals(s1)` is a standard way of comparing string 

   `==` to compare string object references. 

   Once string is over written it simply creates new string and reassigns the reference to that string. 

   

   ##### Functions: 

   `.toCharArray` - Converts string to array of chars

   `.comapreTo` - Compares two strings lexicographically (alphabetical)

   `.concat`- Adds new string at end of other string.

   `.matches` - [Regular expression](#**Regular Expression** ) 

   

   ##### String Builder:

   A mutable sequence of characters.  Faster than string buffer. Used in single thread.

   **Not thread safe**

   ```java
   //String builder
   String konrad = "Konrad";
   StringBuilder sb = new StringBuilder(konrad);
   sb.append(" Dlugosz");
   System.out.println(sb); // Converts to string builder to string automaticlly
   //Konrad Dlugosz
   ```

   Using array to store string as set of bytes. When is full, it automatically increases size.

   `.trimToSize()` - get rid of extra space

   

   ##### String Buffer: 

   **Thread safe**, therefore, is slower than string builder. Used in multi thread. 

   ```Java
   String ernesto = "ernesto";
   StringBuffer sbu = new StringBuffer(ernesto);
   sbu.append("Dlugosz");
   sbu.insert(7, " ");
   System.out.println(sbu);
   // ernesto Dlugosz
   ```

   ##### Why use ? 

   More efficient when using in loops and large data as it doesn't create many strings in the string pool. 

   *String builder* provides improved efficiency and it also provides extra functionalities like `insert`, `append`, `trimToSize` etc

   Use of `String builder` and `buffer` when using loops to avoid performance issues. 

    

3. #### Data types

   - Primitive data types - includes `byte`, `short`, `int`, `long`, `float`, `double`, `boolean` and `char`

   - Non-primitive data types - such as [String](https://www.w3schools.com/java/java_strings.asp), [Arrays](https://www.w3schools.com/java/java_arrays.asp) and [Classes](https://www.w3schools.com/java/java_classes.asp)

     eg. The `Integer` class wraps a value of the primitive type `int` in an object

     

4. #### **Classes/Objects**

   Everything in Java is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an object. The car has **attributes**, such as weight and color, and **methods**, such as drive and brake.

   

5. #### **Class methods (Static - Non Static)**

   You learned from the Java Methods chapter that methods are declared within a class, and that they are used to perform certain actions:

   ````Java
   public class Main {
     static void myMethod() {
       System.out.println("Hello World!");
     }
   
     public static void main(String[] args) {
       myMethod();
     }
   }
   
   // Outputs "Hello World!"
   ````

   Static vs Non static 

   You will often see Java programs that have either `static` or `public` attributes and methods.

   In the example above, we created a `static` method, which means that it can be accessed without creating an object of the class, unlike `public`, which can only be accessed by objects:

   ````java
   public class Main {
     // Static method
     static void myStaticMethod() {
       System.out.println("Static methods can be called without creating objects");
     }
   
     // Public method
     public void myPublicMethod() {
       System.out.println("Public methods must be called by creating objects");
     }
   
     // Main method
     public static void main(String[] args) {
       myStaticMethod(); // Call the static method
       // myPublicMethod(); This would compile an error
   
       Main myObj = new Main(); // Create an object of Main
       myObj.myPublicMethod(); // Call the public method on the object
     }
   }
   ````

   

6. #### **Java Constructors**

   A constructor in Java is a **special method** that is used to initialize objects. The constructor is called when an object of a class is created. It can be used to set initial values for object attributes:

   ````Java
   // Create a Main class
   public class Main {
     int x;  // Create a class attribute
   
     // Create a class constructor for the Main class
     public Main() {
       x = 5;  // Set the initial value for the class attribute x
     }
   
     public static void main(String[] args) {
       Main myObj = new Main(); // Create an object of class Main (This will call the constructor)
       System.out.println(myObj.x); // Print the value of x
     }
   }
   
   // Outputs 5
   ````

   

7. #### **Modifiers** 

   The `public` keyword is an **access modifier**, meaning that it is used to set the access level for classes, attributes, methods and constructors.

   We divide modifiers into two groups:

   - **Access Modifiers** - controls the access level

   - **Non-Access Modifiers** - do not control access level, but provides other functionality

     

   ##### Access Modifiers 

   For **classes**: 

   `public` - The class is accessible by any other class

   `default` - The class is only accessible by classes in the same package. This is used when you don't specify a modifier.

   

   For **attributes, methods and constructors**:

   `public` -  The code is accessible for all classes

   `private`  - The code is only accessible within the declared class

   `default` - The code is only accessible in the same package. This is used when you don't specify a modifier.

   `protected` -  The code is accessible in the same package and **subclasses**

   

   ##### Non-access Modifiers 

   For **Classes**: 

   `final` - The class cannot be inherited by other classes

   `abstract` - The class cannot be used to create objects (To access an abstract class, it must be inherited from another class.

   

   For **attributes, methods and constructors**:

   `final`  - Attributes and methods cannot be overridden/modified

   `static`  -  Attributes and methods belongs to the class, rather than an object

   `abstract` -  Can only be used in an abstract class, and can only be used on methods. The method does not have a body, for example **abstract void run();**. The body is provided by the subclass (inherited from).

   `transient` - Attributes and methods are skipped when serializing the object containing them

   `synchronized` - Methods can only be accessed by one thread at a time

   `volatile` - The value of an attribute is not cached thread-locally, and is always read from the "main memory"

   

8. #### **Encapsulations**

   The meaning of **Encapsulation**, is to make sure that "sensitive" data is hidden from users.  

   To achieve this, you must:

   - declare class variables/attributes as `private`
   - provide public **get** and **set** methods to access and update the value of a `private` variable

   ````java
   public class Person {
     private String name; // private = restricted access
   
     // Getter
     public String getName() {
       return name;
     }
   
     // Setter
     public void setName(String newName) {
       this.name = newName;
     }
   }
   ````

   The `name` variable is declared as `private`, we **cannot** access it from outside this class:

   ````java
   //This will return error
   public class Main {
     public static void main(String[] args) {
       Person myObj = new Person();
       myObj.name = "John";  // error
       System.out.println(myObj.name); // error 
     }
   }
   ````

   Instead, we use the `getName()` and `setName()` methods to access and update the variable:

   ````java
   public class Main {
     public static void main(String[] args) {
       Person myObj = new Person();
       myObj.setName("John"); // Set the value of the name variable to "John"
       System.out.println(myObj.getName());
     }
   }
   
   // Outputs "John"
   ````

   ##### Why Encapsulation?

   - Better control of class attributes and methods

   - Class attributes can be made **read-only** (if you only use the `get` method), or **write-only** (if you only use the `set` method)

   - Flexible: the programmer can change one part of the code without affecting other parts

   - Increased security of data

     

9. #### **Inheritance** 

   In Java, it is possible to inherit attributes and methods from one class to another. We group the "inheritance concept" into two categories:

   - **subclass** (child) - the class that inherits from another class
   - **superclass** (parent) - the class being inherited from

   To inherit from a class, use the `extends` keyword.

   In the example below, the `Car` class (subclass) inherits the attributes and methods from the `Vehicle` class (superclass):

   ````java
   class Vehicle {
     protected String brand = "Ford";        // Vehicle attribute
     public void honk() {                    // Vehicle method
       System.out.println("Tuut, tuut!");
     }
   }
   
   class Car extends Vehicle {
     private String modelName = "Mustang";    // Car attribute
     public static void main(String[] args) {
   
       // Create a myCar object
       Car myCar = new Car();
   
       // Call the honk() method (from the Vehicle class) on the myCar object
       myCar.honk();
   
       // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
       System.out.println(myCar.brand + " " + myCar.modelName);
     }
   }
   ````

   Did you notice the `protected` modifier in Vehicle?

   We set the **brand** attribute in **Vehicle** to a `protected` [access modifier](https://www.w3schools.com/java/java_modifiers.asp). If it was set to `private`, the Car class would not be able to access it.

   ##### Why And When To Use "Inheritance"?

   \- It is useful for code reusability: reuse attributes and methods of an existing class when you create a new class.

   **Tip:** Also take a look at the next chapter, [Polymorphism](https://www.w3schools.com/java/java_polymorphism.asp), which uses inherited methods to perform different tasks.

   

10. #### **Polymorphism** 

    Polymorphism means "many forms", and it occurs when we have many classes that are related to each other by inheritance.

    Like we specified in the previous chapter; [**Inheritance**](https://www.w3schools.com/java/java_inheritance.asp) lets us inherit attributes and methods from another class. **Polymorphism** uses those methods to perform different tasks. This allows us to perform a single action in different ways.

    For example, think of a superclass called `Animal` that has a method called `animalSound()`. Subclasses of Animals could be Pigs, Cats, Dogs, Birds - And they also have their own implementation of an animal sound (the pig oinks, and the cat meows, etc.):

    ````Java
    class Animal {
      public void animalSound() {
        System.out.println("The animal makes a sound");
      }
    }
    
    class Pig extends Animal {
      public void animalSound() {
        System.out.println("The pig says: wee wee");
      }
    }
    
    class Dog extends Animal {
      public void animalSound() {
        System.out.println("The dog says: bow wow");
      }
    }
    
    //Main class create object and call the animalSound()
    class Main {
      public static void main(String[] args) {
        Animal myAnimal = new Animal();  // Create a Animal object
        Animal myPig = new Pig();  // Create a Pig object
        Animal myDog = new Dog();  // Create a Dog object
        myAnimal.animalSound();
        myPig.animalSound();
        myDog.animalSound();
      }
    }
    ````

       ##### Why And When To Use "Inheritance" and "Polymorphism"?

       \- It is useful for code reusability: reuse attributes and methods of an existing class when you create a new class.

    

11. #### **Abstract**

    Data **abstraction** is the process of hiding certain details and showing only essential information to the user.
    Abstraction can be achieved with either **abstract classes** or [**interfaces**](#Interfaces).

    The `abstract` keyword is a non-access modifier, used for classes and methods:

    - **Abstract class:** is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).
    - **Abstract method:** can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from).

    An abstract class can have both abstract and regular methods:

    ````Java
    abstract class Animal {
      public abstract void animalSound();
      public void sleep() {
        System.out.println("Zzz");
      }
    }
    
    Animal myObj = new Animal(); // will generate an error
    ````

    To access the abstract class, it must be inherited from another class. Let's convert the Animal class we used in the [Polymorphism](https://www.w3schools.com/java/java_polymorphism.asp) chapter to an abstract class:

    ````Java
    // Abstract class
    abstract class Animal {
      // Abstract method (does not have a body)
      public abstract void animalSound();
      // Regular method
      public void sleep() {
        System.out.println("Zzz");
      }
    }
    
    // Subclass (inherit from Animal)
    class Pig extends Animal {
      public void animalSound() {
        // The body of animalSound() is provided here
        System.out.println("The pig says: wee wee");
      }
    }
    
    class Main {
      public static void main(String[] args) {
        Pig myPig = new Pig(); // Create a Pig object
        myPig.animalSound();
        myPig.sleep();
      }
    }
    ````

    ##### Why And When To Use Abstract Classes and Methods?

    To achieve security - hide certain details and only show the important details of an object.

    **Note:** Abstraction can also be achieved with [Interfaces](https://www.w3schools.com/java/java_interface.asp), which you will learn more about in the next chapter.

    

12. #### **Interfaces**

    Another way to achieve [abstraction](https://www.w3schools.com/java/java_abstract.asp) in Java, is with interfaces.

    An `interface` is a completely "**abstract class**" that is used to group related methods with empty bodies:

    ````java
    // interface
    interface Animal {
      public void animalSound(); // interface method (does not have a body)
      public void run(); // interface method (does not have a body)
    }
    ````

    To access the interface methods, the interface must be "implemented" (kinda like inherited) by another class with the `implements` keyword (instead of `extends`). The body of the interface method is provided by the "implement" class:

    ````Java
    // Interface
    interface Animal {
      public void animalSound(); // interface method (does not have a body)
      public void sleep(); // interface method (does not have a body)
    }
    
    // Pig "implements" the Animal interface
    class Pig implements Animal {
      public void animalSound() {
        // The body of animalSound() is provided here
        System.out.println("The pig says: wee wee");
      }
      public void sleep() {
        // The body of sleep() is provided here
        System.out.println("Zzz");
      }
    }
    
    class Main {
      public static void main(String[] args) {
        Pig myPig = new Pig();  // Create a Pig object
        myPig.animalSound();
        myPig.sleep();
      }
    }
    ````

    ##### Notes on Interfaces:

    - Like **abstract classes**, interfaces **cannot** be used to create objects (in the example above, it is not possible to create an "Animal" object in the MyMainClass)
    - Interface methods do not have a body - the body is provided by the "implement" class
    - On implementation of an interface, you must override all of its methods
    - Interface methods are by default `abstract` and `public`
    - Interface attributes are by default `public`, `static` and `final`
    - An interface cannot contain a constructor (as it cannot be used to create objects)

    ##### Why And When To Use Interfaces?

    \1) To achieve security - hide certain details and only show the important details of an object (interface).

    \2) Java does not support "multiple inheritance" (a class can only inherit from one superclass). However, it can be achieved with interfaces, because the class can **implement** multiple interfaces. **Note:** To implement multiple interfaces, separate them with a comma (see example below).

    ##### Multiple Interfaces

    To implement multiple interfaces, separate them with a comma:

    ````java
    interface FirstInterface {
      public void myMethod(); // interface method
    }
    
    interface SecondInterface {
      public void myOtherMethod(); // interface method
    }
    
    class DemoClass implements FirstInterface, SecondInterface {
      public void myMethod() {
        System.out.println("Some text..");
      }
      public void myOtherMethod() {
        System.out.println("Some other text...");
      }
    }
    
    class Main {
      public static void main(String[] args) {
        DemoClass myObj = new DemoClass();
        myObj.myMethod();
        myObj.myOtherMethod();
      }
    }
    ````

    

    

    

13. #### **Recursion**

    Recursion is the technique of making a function call itself. This technique provides a way to break complicated problems down into simple problems which are easier to solve.

    ##### Recursion Example

    Adding two numbers together is easy to do, but adding a range of numbers is more complicated. In the following example, recursion is used to add a range of numbers together by breaking it down into the simple task of adding two numbers:

    ```Java
    public class Main {
      public static void main(String[] args) {
        int result = sum(10);
        System.out.println(result);
      }
      public static int sum(int k) {
        if (k > 0) {
          return k + sum(k - 1);
        } else {
          return 0;
        }
      }
    }
    ```

    `k + sum(k - 1);`

    When the `sum()` function is called, it adds parameter `k` to the sum of all numbers smaller than `k` and returns the result. When k becomes 0, the function just returns 0. When running, the program follows these steps:

    `10 + sum(9)`
    `10 + ( 9 + sum(8) )`
    `10 + ( 9 + ( 8 + sum(7) ) )`
    `...`
    `10 + 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 + sum(0)`
    `10 + 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 + 0`

    

14. #### **Regular Expression** 

    its a patter that matches phone number: 

    ```java
    String myNumber =  "07393775789";
    
    if (myNumber.matches("[0-9]{5}\s*[0-9]{3}\s*[0-9]{3}")) {
        System.out.println("Phone number found.");
    }
    ```

     [regex101](https://regex101.com/) - tool for testing regex

    Java.util.regex package is used for large data however, for single match `.matches` is sufficient from String library.

    `.split` is used to separate data for example from CSV file. 

    ```Java
    /**
     * Split funciton needed to read data from CSV file
     */
    String allNames = "Anthony, Yefri, George, Kamil, Talal, Alex, Konrad, Pruthvi, " +
            "Nikolaos, Ishmael, Jakub, Mihai, Ed, Mark, Ignas, Leo, Ria";
    
    for(String nextName: allNames.split(", ")){
        System.out.println(nextName);
    }
    ```

     

15. #### SOLID

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

    

16. #### Collections

    The Java collections framework is a set of classes and interfaces that implement commonly reusable collection data structures. Although referred to as a framework, it works in a manner of a library. The collections framework provides both interfaces that define various collections and classes that implement them. 

    ![](images/collectionHierarchy.PNG)

    

    **List Interface:** 

    * **Array List** 

      The `ArrayList` class is a resizable array.

      The difference between a built-in array and an `ArrayList` in Java, is that the size of an array cannot be modified (if you want to add or remove elements to/from an array, you have to create a new one). While elements can be added and removed from an `ArrayList` whenever you want.

      ```java
      ArrayList<String> cars = new ArrayList<String>();
      ```

      **Methods in ArrayList:**

      `EnsureCapacity()`, `TrimToSize()`

    * LinkedList 

    * Ques 

      * First in first out (FIFO) data structure
      * add() / offer()
      * Remove() / poll()
      * element() / peak()

    * Stack

      * Last in first out (LIFO) data structure. Example would be stack of cards. 
      * Push() - Add 
      * pop() - Remove

    * Vector 

      * Its like array list but its safe in multithreaded envoriemnt where array list is not thread safe

      

    **Set interface:** 

    *Things are not stored by index unlike List interface.*  It uses similar methods to list interface.

    Main concept of set:

    * Doesn't have index

    * in hash set, elements will be ordered by hashcode. 

    * Tree Set, alphabetical order in string example. 

    * No duplicates, doesn't add same data. 

      

    **Map interface:** 

    An object that maps keys to values. A map cannot contain duplicate keys; each key can map to at most one value.

    Map (Key, value)

    

17. #### Iterator

    An `Iterator` is an object that can be used to loop through collections, like [ArrayList](https://www.w3schools.com/java/java_arraylist.asp) and [HashSet](https://www.w3schools.com/java/java_hashset.asp). It is called an "iterator" because "iterating" is the technical term for looping.

    The `iterator()` method can be used to get an `Iterator` for any collection:

    ````java
    // Import the ArrayList class and the Iterator class
    import java.util.ArrayList;
    import java.util.Iterator;
    
    public class Main {
      public static void main(String[] args) {
    
        // Make a collection
        ArrayList<String> cars = new ArrayList<String>();
        cars.add("Volvo");
        cars.add("BMW");
        cars.add("Ford");
        cars.add("Mazda");
    
        // Get the iterator
        Iterator<String> it = cars.iterator();
    
        // Print the first item
        System.out.println(it.next());
      }
    }
    ````

    To loop through a collection, use the `hasNext()` and `next()` methods of the `Iterator`:

    ````Java
    while(it.hasNext()) {
      System.out.println(it.next());
    }
    ````

    Iterators are designed to easily change the collections that they loop through. The `remove()` method can remove items from a collection while looping.

    ````Java
    import java.util.ArrayList;
    import java.util.Iterator;
    
    public class Main {
      public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<Integer>();
        numbers.add(12);
        numbers.add(8);
        numbers.add(2);
        numbers.add(23);
        Iterator<Integer> it = numbers.iterator();
        while(it.hasNext()) {
          Integer i = it.next();
          if(i < 10) {
            it.remove();
          }
        }
        System.out.println(numbers);
      }
    }
    ````

    **Note:** Trying to remove items using a **for loop** or a **for-each loop** would not work correctly because the collection is changing size at the same time that the code is trying to loop.

    

18. #### Error handling exceptions

    All Exceptions apart from runtime are checked/caught 

    RuntimeExceptions are uncaught/unchecked

    ![](/images/exeptions.PNG)

19. #### Log4j

    ```
    property.filename=logs 
    appender=console, file
    appender.console.type=Console
    appender.console.name=STDOUT
    appender.console.layout.type=PatternLayout
    appender.console.layout.pattern=[%level] %d %t %c - %msg%n
    
    appender.file.type=File
    appender.file.name=LOGFILE
    appender.file.layout.type=PatternLayout
    appender.file.layout.pattern=[%level] %d %t %c - %msg%n
    appender.file.fileName=myLogfile.log
    
    rootLogger.level=debug
    rootLogger.appenderRefs=console, file
    rootLogger.appenderRef.console.ref=STDOUT
    rootLogger.appenderRef.file.ref=LOGFILE
    ```

    log4j2.property configuration.

20. #### Concurrency and multithreading 

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

    



### Design patterns

1. #### Creational patterns

   1. ##### Factory method

      The **factory method pattern** is a [creational pattern](https://en.wikipedia.org/wiki/Creational_pattern) that uses factory methods to deal with the problem of [creating objects](https://en.wikipedia.org/wiki/Object_creation) without having to specify the exact [class](https://en.wikipedia.org/wiki/Class_(computer_programming)) of the object that will be created. This is done by creating objects by calling a factory method—either specified in an [interface](https://en.wikipedia.org/wiki/Interface_(object-oriented_programming)) and implemented by child classes, or implemented in a base class and optionally [overridden](https://en.wikipedia.org/wiki/Method_overriding) by derived classes—rather than by calling a [constructor](https://en.wikipedia.org/wiki/Constructor_(object-oriented_programming)).

      

   2. ##### Model-View-Controller

      **Model–view–controller** (**MVC**) is a [software design pattern](https://en.wikipedia.org/wiki/Software_design_pattern)[[1\]](https://en.wikipedia.org/wiki/Model–view–controller#cite_note-1) commonly used for developing [user interfaces](https://en.wikipedia.org/wiki/User_interface) that divide the related program logic into three interconnected elements. This is done to separate internal representations of information from the ways information is presented to and accepted from the user

      Eg. 

      **Model** - processing like sorting object selection  

      **Controller** - separate class - receive input from user. use model to archive task.

      **View** - shows the results of the model processing. 

      
      
      

2. #### Structural Patterns

   1. **Data access object (DAO)** creates interfaces per table or junction table to perform CRUD operations which are select, insert, update, delete. 

   2. **Data access layer (DAL)** is the layer of a system that exists between the business logic layer and the persistence / storage layer. A DAL might be a single class, or it might be composed of multiple Data Access Objects (DAOs). It may have a facade over the top for the business layer to talk to, hiding the complexity of the data access logic. It might be a third-party object-relational mapping tool (ORM) such as Hibernate.

      *DAL is an architectural term, DAOs are a design detail.*

   3. **Data transfer object (DTO)** transfers some bits of the business object though network or other part of the application. This will reduce number of methods called. 

   4. **Business object (BO)** represents real world object in the application. For example, employee class

      

3. #### Behavioral patterns 
