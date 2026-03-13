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
- Explain: Java multithreading
- Explain: Java distributed computing

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
- classes can have only public or default access
- a class with default access can be seen only within the same package
- a class with public access can be seen by all classes from all packages
- class visibility resolves around whether code in one class can
    - create an instance of another class
    - extend (or sublclass) another class
    - access methods an variables of another class







TODO...71














# A: Links
https://mylearn.oracle.com/ou/exam/java-se-8-programmer-i-1z0-808/105037/110679/170387


https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet
