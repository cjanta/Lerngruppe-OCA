```java
// Alle Angaben ohne Gewähr.  
// OCA Java SE 8 
```

# Lerngruppe-OCA
Key-Points Zusammenfassung

## Chapter 1

### Java Features and Benefits (OCA Objective 1.5)

- Explain: Java supports oop in general
- Explain: Java Encapsulation
- Explain: Java automatic memory management
- Explain: Java comes with a large API
- Explain: Java Bult-in security features
- Explain: Java multiplatform compatibility
- Explain: Java strong typing
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
