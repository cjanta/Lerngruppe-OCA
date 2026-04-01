```java
// Alle Angaben ohne Gewähr.  
// OCA Java SE 8 
```

# Lerngruppe-OCA
Key-Points Zusammenfassung

## Chapter 1

### Java Features and Benefits (OCA Objective 1.5)

## Explain: Java supports oop in general
As software systems get larger, they get more difficult to test and enhance.
For the last serveral decades, OO programming has been the dominant software design approach for large systems.
OO Design also offers a natural way to think about how the components in a system should be constructed and how they should interact.
The classes, objects, system state and behaviors in well-designed OO systems are easy to map conceptually to their counterparts in the real world. 

## Explain: Java Encapsulation
Encapsulation is a key concept in OO programming. 
Encapsulation allows a software component to hide its data from other components, 
protecting the data from being updated without the components approval or knowledge.
Java makes encapsulation far easier to archieve than in non-OO languages.

## Explain: Java automatic memory management
Unlike some of its competitors (C and C++) Java provides automatic memory management,
keeping track of memory through pointers is quite complex. 
Further, tracking down bugs related to memory management (often called memory leaks) is a common,
error-prone, and time consuming process.

## Explain: Java comes with a large API
Java has an enormous library of prewritten, well tested and well supported code.
This code is easy to include in your java applications and is well documented via the Java API.
Throughout this book we will explore some of the most used (and most useful) members of Java' standard
core library.

## Explain: Java Bult-in security features
When compiled Java Code is executed, it runs inside the Java Virtual Machine (JVM). 
The JVM provides a secure "sandbox" for your Java code to run in.
The JVM makes sure that nefarious programmers cannot write Java code that will cause trouble
on other peoples machines when it runs.

## Explain: Java multiplatform compatibility
Write once and run anywhere. One of the goals of Java is that much of Java code you write can run on many platforms, 
ranging from tiny IoT-devices, to phones, to laptop computers, to large servers.
Another common phrase for this ability to run on many devices is "cross-platform".

## Explain: Java strong typing
A strongly typed language usually requires the programmer to explicity declare the types of the data
and objects being used in a program. Strong typing allows the java compiler to catch many potential programming errors
before your code even compiles.
At the other end of the spectrum are dynamicly typed languages. Dynamicly languages can be less verbose[de=übermäßig detailliert], 
faster to code initialy and are often preferred in enviroments where small teams and rapid prototyping are the norm.
But strongly typed languages like Java come into their own in large software shops with many teams of programmers and the need for more

## Explain: Java multithreading
Java provides built-in language features and API's that allow programs to use many operating-system processes at the same time.
As system grow to handle more computationally intensive problems and larger data sets, the ability to use all of a computer's core processors becomes essential.
Multithreaded programming is never simple, but Java provides a rich toolkit to make it as easy as possible

## Explain: Java distributed computing
Another way to tackle big programming problems is to distribute the workload across many machines. The Java API provides several ways to simplify tasks related
to distributed computing. One such example is *serialization*, a process in which a Java object is converted to a portable form.
Serialized Objects can be sent to other machines, deserialized, and then used as a normal Java Object.

### Identifiers (OCA Objective 2.1)
- Identifiers can begin with
    - a letter:
    ```regex
        "\\p{L}" or only A-Z: "[a-zA-Z]"
    ```
    - an underscore
    ```regex
        "_"
    ```
    - a currency character € or $
    ```regex
       "\\p{Sc}"
    ```
- After the first character, indentifiers can also include digits
    ```regex
       "\\d"
    ```

### Executable Java Files and main() (OCA Objective 1.3)
- compile with javac.exe, execute with java.exe, both programms support many cli options
- only version of main signature:
```java
public static void main(String[] args)
``` 
- main() can be overloaded

### Imports (OCA Objective 1.4)
- an import statements only job is to save keytrokes
- you can use an asterix to search through the contents of a single package
- although referred to as "static imports" the syntax is: import static ...
- you can import API classes and/or custom classes

### Source File Declaration Rules (OCA Objective 1.2)
- a source code file can have only one public class
- if the source file contains a public class, the filename must match the public class name
- a file can have only one package statement, but it can have multiple imports
- the package statement(if any) must be the first (noncomment) line in a source file
- the import statements(if any) must come after the package statement(if any) and before the first class declaration
- if there is no package statement, import stements must be the first (noncomment) statements in a soruce file
- package and import statements apply to all classes in the file
- a file can have more than one nonpublic class
- file with no public classes have no naming restrictions

### Class Access Modifiers (OCA Objective 6.4)
- there a three access modifiers: public, protected, private
- there are **four** access levels:
    - public
    - protected
    - default
    - private
- classes can have only public or default access (inner-classes can have all 4 access levels)
- a class with default access can be seen only within the same package
- a class with public access can be seen by all classes from all packages
- class visibility resolves around whether code in one class can
    - create an instance of another class
    - extend (or sublclass) another class
    - access methods an variables of another class

### Class Modifiers (Nonaccess) (OCA Objective 1.2, 7.1 and 7.5)
- classes can also be modified with final, abstract or strictfp
- a class cannot be both final and abstract
- a final class cannot be subclassed
- an abstract class cannot be instantiated
- a single abstract method in a class means the whole class must be abstract
- an abstract class can have both abstract and nonabstract methods
- the first concrete class to extend an abstract class must implement all of its abstract methods
  
### Interface Implementation (OCA objective 7.5)
- Usually, interfaces are contracts for what a class can do, but they say nothing about the way in which the class must do it.
- Interfaces can be implemented by any class from any inheritance tree
- Usually, an interface is like a 100 percent abstract class and is implicity abstract whether or not you type the abstract modifier in the declaration
- Usually interfaces have only abstract methods
- Interface methods are by default public and usually abstract - explicit declaration of these modifiers is optional
- Interfaces can have constants, which are always implicitly public, static and final
- Interface constant declarations of public, static and final are optional in any combinations
- As of Java8, interfaces can have concrete methods declared as either default or static
- A legal nonabstract implementing classs has the following properties:
      - It provides concrete implementations for the interfaces methods
      - It must follow all legal override rules for the methods it implements
      - It must not declare any new checked exceptions for an implementation method
      - It must not declare any checked exceptions that are broarder than the exceptions declared in the interface method
      - It may declare runtime exceptions on any interface method implementation regardless of the interface declaration
      - IT must maintain the exact signature (allowing for covariant returns) and return type of the methods it implements (but does not have to declare the            exceptions of the interface)
  - A class implementing an interface can itself be abstract
  - An abstract implementing class does not have to implement the interface methods (but the first concrete subcluss must)
  - A class can extend only one class (no multiple inheritans), but it can implement many interfaces
  - Interfaces can extend one or more othe interfaces
  - Interfaces cannot extend a class ir implement a class or interface
  - **Exam-Tip:Verify that interfaces and class declarations are legal before verifying other code logic**
    
### Member Access Modifiers (OCA Objective 6.4)
- Methods and instance(nonlocal) variables are known as "members"
- Members can use all four access levels: public, protected, default and private
- Member access comes in two forms:
      - Code in one class can access a member of another class
      - A subclass can inherit a member of its superclass
- If a class cannot be accessed, its members cannot be accessed
- Determine class visibility before determining member visibility
- public members can be accessed by all other classes, even in other packages
- If a superclass member is public, the subclass inherits it - regardeless of package
- Members accessed without the dot operator (.) must belong to the same class
- this. always referes to the currently executing object
- this.aMethod() is the same as just invoking aMethod()
- private members can be accessed only by code in the same class
- private members are not visible to subclasses, so private members cannot be inherited
- Default and protected members differ only when subclasses are involved:
      - Default members can be accessed only by classes in the same package
      - Protected members can be accessed by other classes in the same package, plus subclasses, regardless of package
      - protected = package + subclasses
      - For subclasses outside the package, the protected member can be accessed only through inheritance,
        a subclass outside the package cannot access a protected member by using a reference to a subclass instance
       (In other words, inheritance is the only mechanism for a subclass outside the package to access a protected member of its superclass)
### Local Variables (OCA Objectives 2.1 and 6.4)
- Local (method, automatic or stack) variable declarations cannot have access modifiers
- final is the only modifier available to local variables
- Local variables don't get default values, so they must always be initialized before use

### Other Modifiers-Members (OCA Objectives 7.1 and 7.5)
- final methods cannot be overriden in a subclass
- abstract methods are declared with a signature, a return type and an optional throws clause but they are not implemented
- abstract methods end in a semicolon- no curly braces
- Three ways to spot a nonabstract method:
      - the method is not marked abstract
      - the method has curly braces
      - the method **might** have code between the curly braces
- the first nonabstract (concrete) class to extend an abstract class must implement all of the abstract class's abstract methods
- the synchronized modifier applies only to methods and code blocks
- synchronized methods can have any access control and can also be marked final.
- abstraced methods must be implemented by a subclass so they must be inheritable. For that reason:
    - abstract methods cannot be private
    - abstract methods cannot be final
- the native modifier applies only to methods
- the strictfp modifier applies only to classes and methods
### Methods with var-args (OCA Objective 1.2)
- Methods can declare a parameter that accepts from the zero to many arguments, a so-called var-arg methods
- A var-arg parameter is declared with the syntax type... name; (example: doStuff(int... x))
- a var-arg method can have only one var-arg parameter
- in methods with normal parameters and a var-arg, the var-arg must come last
### Contructors (OCA Objectives 1.2 and 6.3)
- Contructors must have the same as the class
- Contructors can have arguments but they cannot have a return type
- Contructors can use any access modifiers(even private)
### Variable Declarations (OCA Objective 2.1)
- Instance variables can:
      - have any access control
      - be marked final or transient
- Instance variables can't be abstract, synchronized, native or strictfp
- It is legal to declare a local variable with same name as an instance variable this is called: "shadowing"
- final variables have the following properties:
    - final variables cannot be reassigned once assigned a value
    - final reference varables cannot refer to a different object once the object has been assigned to the final variable
    - final variables must be initialized before the contructor completes
    - There is no such thing as a final object. An object reference marked final does NOT mean the object itself can't change
    - the trasient modifier applies only to instance variables
    - the volatile modifier applies only to instance variables
### Array Declaration (OCA Objectives 4.1 and 4.2)
- Arrays can hold primitives or objects but the array itself is always an object
- When you declare an array, the brackets can be to the left or to he right of the variable name
- it's never legal to include the size of an array in the declaration
- an array of objects can hold any object that passes the IS-A(or instanceof) test for the declared type of array.(Example: If Horse extends Animal then a Horse object can go into an Animal array)
### Static Variables and Methods (OCA Objective 6.2)
- they are not tied to any particular instance of a class
- no class instances are needed in order to use static members of the class or interface
- there is only one copy of a static variable/class and all instances share it
- static methods do not have direct access to nonstatic members
### enums (OCA Objective 1.2)
- an enum specifies a list of constant values assigned to a type
- an enum is NOT a String or an int; an enum contant's type is the enum type. (Example: SUMMMER adn FALL are of the enum type Season)
- an enum can be declared outside or inside a class but not in a method
- an enum declared outside a class must NOT be marked static,final,abstract,protected or private
- enums can contain contructors, methods, variables and constant-specific class bodies
- enum constants can be send arguments to the enum contrucor using the syntax: BIG(8)
- enum contructors can have arguments and can be overloaded
- enum contructors can **never** be invoked directly in code. There always called automatically when an enum is initialized
- the semicolon at the end of an enum declaration is optional. These are legal:
      - enum Foo{ONE, TWO, THREE}
      - enum Foo{ONE, TWO, THREE};
- MYEnum.values() returns an array of MYEnum's values

### Explanations, KeyWords

#### transient
Meaning: Marks a field tthat should not be serialized
Usage: When an object is written to a stream (e.g. ObjectOutputStream), fields marked as transient are skipped
Use it when: You want to exclude sensitive or temporary data from serialization.
#### strictfp
Meaning: Forces strict IEEE-754 floating-point behaviour, ensuring the same result on all platforms.
Usage: Apply it to classes, interfaces or methods
Use it when: You need consistent floating-point calculations across different CPUs/architectures
#### synchronized
Meaning: Ensures that only one thread at a time can execute a method or block
```java       
public synchronized void increment() {
    count++;
}
```
```java       
synchronized (this) {
    count++;
}
```
Use it when: Multiple threads access and modify shared data — prevents race conditions.
#### native
Meaning: Declares a method whose implementation is not written in Java, but in a native language (like C/C++) via JNI
Java only knows the method signature - the actual logic is defined in a nativ library
Use it when: You need OS-level access, hardware interaction or to call legacy C/C++ code

#### volatile
Meaning: Ensures a variable is always read directly from main memory and not from threads local cache
Whithout volatile, threads may see outdated values.
Use it when: You have simple shared state flags updated by multiple threads(e.g. running, shutdown, ready) and don't need full synchronization


## Chapter 2 Object Orientation

### Encapsulation, IS-A, Has-A* (OCA Objective 6.5)
- Encapsulation helps hide implementation behind an interface (or API)
- Encapsulated code hast two features:
      - Instance variables are kept protected (usually with the private modifier)
      - Getter and Setter methods provide access to instance variables
- IS-A refers to inheritance or implementation
- IS-A is expressed with the keyword extends or implements
- IS-A, "inherits from" and "is subtype of" are all equivalent expressions
- HAS-A means an instance of one class "has a" reference to an instance of anothr class or another instance of the same class [HAS-A is not in exam but good to know]

### Inheritance (OCA Objective 7.1)
- Inheritance allows a type to be a subtype of a supertype and thereby inherit public and protected variables and methods of the supertype
- Inheritance is a key concept that underlies IS-A, polymorphism, overriding, overloading and casting
- All classes (except class Object) are subclass of type Object and therefor they inherit Object's methods.



TODO: Polymorphism p:157

















# A: Links
https://mylearn.oracle.com/ou/exam/java-se-8-programmer-i-1z0-808/105037/110679/170387


https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet
