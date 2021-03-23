# Java Meeting topics

## Concepts
- Environment: PATH, CLASSPATH, JAVA_HOME, command vs flag vs argument
- Platform Independence of the JVM
- Memory memory model: stack, heap, String Pool, Garbage collector, threads
- Compile-time vs Runtime: source code vs bytecode
- OOP: Polymorphism, Encapsulation, Inheritance, Abstraction
- Source Code Management: Git
- Project, dependency, and build management: Gradle
- Unit testing: Test Driven Development, Red-Green refactoring

## Tools
- JDK: `javac`, `java`, `jar`
- Git: `init`, `add`, `commit`, `checkout`, `merge`, `remote`, `clone`, `push`, `pull`
- Gradle

## Language Features
- Default Constructor
- Overloading and Overriding
- Checked vs Unchecked Exceptions
- Variable scopes: class/global, object/instance, method, block/loop, bracket
- Interfaces: functional vs marker, default fields & methods
- Abstract Classes
- Anonymous Classes
- Lambdas & Streams
- Generics: type inference, type erasure, bounded types

## Language Syntax
- Package & Import
- Class & method signatures: parameters, access modifiers, return types, constructors, varargs
- Access modfiers: public, protected, (default), private
- Non-access modifiers: static, final, abstract, synchronized
- Control statements: if, if else, else, while, do/while, for, switch, continue, break
- Primitive types: byte, short, int, long, char, boolean, float, double
- Reference types: Classes, Enums, Interfaces, Arrays
- Inheritance: extends, implements
- Exception handling: try, catch, finally

## Standard Library
- [java.lang](https://docs.oracle.com/javase/8/docs/api/java/lang/package-summary.html)
  - [Object](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html): `toString()`, `hashcode()`, `equals()`, `finalize()`, `notify()`
  - [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html), [StringBuilder](https://docs.oracle.com/javase/8/docs/api/java/lang/StringBuilder.html) & [StringBuffer](https://docs.oracle.com/javase/8/docs/api/java/lang/StringBuffer.html)
  - Wrapper Classes: [Integer](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html), [Double](https://docs.oracle.com/javase/8/docs/api/java/lang/Double.html), etc.
  - [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html): `forEach()`
  - [Comparable](https://docs.oracle.com/javase/8/docs/api/java/lang/Comparable.html): `compareTo()`
  - [AutoCloseable](https://docs.oracle.com/javase/8/docs/api/java/lang/AutoCloseable.html) (try-with-resources): close()
  - [System](https://docs.oracle.com/javase/8/docs/api/java/lang/System.html): `in`, `out`, `getenv()`, `gc()`
  - [Runnable](https://docs.oracle.com/javase/8/docs/api/java/lang/Runnable.html) & [Thread](https://docs.oracle.com/javase/8/docs/api/java/lang/Thread.html): `run()`, `start()`, `isAlive()`, `join()`
  - Reflection: [java.lang.reflect](https://docs.oracle.com/javase/8/docs/api/java/lang/reflect/package-summary.html), [Class](https://docs.oracle.com/javase/8/docs/api/java/lang/Class.html)
  - [Throwable](https://docs.oracle.com/javase/8/docs/api/java/lang/Throwable.html): [Error](https://docs.oracle.com/javase/8/docs/api/java/lang/Error.html), [Exception](https://docs.oracle.com/javase/8/docs/api/java/lang/Exception.html), [RuntimeException](https://docs.oracle.com/javase/8/docs/api/java/lang/RuntimeException.html)
- [java.io](https://docs.oracle.com/javase/8/docs/api/java/io/package-summary.html)
  - [File](https://docs.oracle.com/javase/8/docs/api/java/io/File.html)
  - InputStream/OutputStream vs Reader/Writer
  - [BufferedReader](https://docs.oracle.com/javase/8/docs/api/java/io/BufferedReader.html) & [BufferedWriter](https://docs.oracle.com/javase/8/docs/api/java/io/BufferedWriter.html)
  - [Serializable](https://docs.oracle.com/javase/8/docs/api/java/io/Serializable.html)
  - [ObjectInputStream](https://docs.oracle.com/javase/8/docs/api/java/io/ObjectInputStream.html) & [ObjectOutputStream](https://docs.oracle.com/javase/8/docs/api/java/io/ObjectOutputStream.html)
- [java.util](https://docs.oracle.com/javase/8/docs/api/java/util/package-summary.html)
  - [StringTokenizer](https://docs.oracle.com/javase/8/docs/api/java/util/StringTokenizer.html)
  - [Scanner](https://docs.oracle.com/javase/8/docs/api/java/util/Scanner.html)
  - [Properties](https://docs.oracle.com/javase/8/docs/api/java/util/Properties.html)
  - [Java Collections Framework](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/index.html):
    - [Arrays](https://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html)
    - [Collections](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html)
    - [Collection](https://docs.oracle.com/javase/8/docs/api/java/util/Collection.html):
      - [Map](https://docs.oracle.com/javase/8/docs/api/java/util/Map.html): [Hashtable](https://docs.oracle.com/javase/8/docs/api/java/util/Hashtable.html), [HashMap](https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html), [TreeMap](https://docs.oracle.com/javase/8/docs/api/java/util/TreeMap.html)
      - [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html): [ArrayList](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html)
      - [Set](https://docs.oracle.com/javase/8/docs/api/java/util/Set.html)/[SortedSet](https://docs.oracle.com/javase/8/docs/api/java/util/SortedSet.html): [HashSet](https://docs.oracle.com/javase/8/docs/api/java/util/HashSet.html), [TreeSet](https://docs.oracle.com/javase/8/docs/api/java/util/TreeSet.html)
      - [Queue](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html)
      - [Deque](https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html)
    - [Iterator](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html)
    - [Comparator](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html)

## Design patterns
  - Singleton
  - Factory
  - Dependency Injection
  - Data Access Object

# Questions
- What is Java?
- What are the benefits of Java?
- What is the difference betwwen the JRE, JDK, and JVM?
- What happens during the compilation process?
- What is a constructor?
- What are the primitive datatypes?
- What is a no args constructor?
- What is the default ocnstructor?
- What are the scopes of a variable in java?
- What are the different access modifiers?
- What are the different control statements and how are they different?
- How do you create an array in java?
- What are varargs?
- What are packages and imports?
- What is a static import?
- What is static?
- What are Strings?
- What are some string methods?
- What is the difference between String, StringBuilder, and StringBuffer?
- What is the String Pool?
- What is the difference between the stack and the heap?
- What is an exception?
- What is the difference between exception and error?
- What are the ways one can handle an exception?
- What are checked exceptions and unchecked exceptions?
- How many catch blocks can be used in a try catch?
- What does the finally block do?
- How do I create a custom exception?
- What is autoboxing?
- What is a wrapper class?
- What is garbage collection?
- How do I perform garbage collection?
- what is the difference between final, finally, and finalize?
- What is the reflection API?
- What are the pillars of object oriented programming?
- What is the different between an abstract class and an interface?
- What is transient? Volatile?
- What are the differences between FileinputeStream, FileReader, and bufferedReader (and their output counterparts)?
- What is Scanner?
- What is serializaiton?
- How do I serialize an object?
- What is a marker interface?
- How do I prevent some data from getting serialized?
- What is the difference between Collection and Collections
- What are the various input/delete/get methods for List, Set, and Queue?
- What is an iterator?
- What are generics? Why use them?
- What is the diffence between Comparator and Comparable?
- What is the purpose of the Object class?
- What is the difference between  == and .equals?
- What is the purpose of hashcode?
- What is the difference between HashMap and Hashtable?
- How does one iterate through a HashMap?
- What is multithreading and why do we use it?
- What are the different ways to create a thread, what is different about them?
- What are the JVM recognized states of a thread?
- What are various methods that threads have?
- What is synchronization?
- What are the risks of synchronization?
- What is deadlock, livelock and thread starvation? (Consumer/Producer)
- What is JUnit?
- What are the annotations of JUnit?
- What are the different assert methods of JUnit?
- How do I create a test case and test suite in JUnit?
- What is Maven?
- what is the maven lifecycle?
- What is the purpose of the pom.xml?
- What are the purposes of a maven repository among projects?
- What is the difference between Singleton and Factory?
- What is the difference between implicit and explicit casting?

# Mehrab's notes
Java is an object-oriented programming language and a platform developed by Sun Microsystems (eaten by Oracle). Using the principle of **WORA** (Write Once, Run Anywhere), a Java application can be compiled and executed on any platform supported by Java. Flexible, popular, and well-supported, Java has helps developers write scalable client-server web applications, desktop and mobile applications, and frameworks and libraries.

## Features
- **Platform independence** The compiler converts source code to bytecode, then the JVM executes that bytecode. While each operating system has their own JVM implementation, so every JVM can execute bytecode regardless of origin of said code.

- **Clear, verbose syntax** Java has C-like syntax like C++ and C#, many syntax elements of the language are readable and widely used in programming. The Java API (Application Programming Interface) is also written using verbose, descriptive naming conventions making it simple to parse large code bases.

- **Multi-paradigm** While Java is object-oriented, it supports multiple paradigms such as imperative, generic, concurrent, and functional.

- **Garbage collection** The JVM performs automatic memory deallocation of unused objects at runtime. Programs are written without the need for complex memory management.

- **Multithreading** Java supports multithreading at both language and the standard library levels. It allows concurrent and parallel execution of several parts of a Java program.

## Programming and Compiling
Most Java applications only require the **JRE** (Java Runtime Environment). But to write and compile you need the **JDK** (Java Development Kit). While the JRE provides Java's standard libraries and exceptions as well as a JVM, the JDK provides all the above as well as *javac*, the compiler. Java source code is written in text files labeled with *.java* extension. It is then compiled into bytecode in *.class* files by *javac*. Then the bytecode is executed by the JVM, which translates the Java commands into low-level instructions to the operating system.

Since Java 6, all Java programs not run inside a container (such as a Servlet Web Container) start and end with the main method. The class containing the main method can have any name, but the method itself should always be named *main*

```java
class Example {
    public static void main(String[] args) {
        System.out.println("Num args:" + args.length);
    }
}
```

- *public* is a Java access modifier keyword that means the `main` method can be accessed from any method during the program's execution.
- *static* is a Java keyword that means the method can be invoked without creating an instance of the class that contains it, making it a global method.
- *void* is a Java return type keyword that means the method doesn't return any values of any data type.
- *args* is a Java variable of type String array which means the method can take command line arguments as an array of Strings

We can compile this code into a *.class* file of the same name:
>javac Example.java

And to run the resulting `Example.class` file:
>java Example

The `java` and `javac` commands require the full directory path or class path to any source code or binary file respectively. If you have a package `com.demo` in the first line of Example, then you would nest the java file into a `com/demo/` directory and then run:
>javac com/demo/Example.java 

>java com.demo.Example

From here we can add packages and imports, expanding the application into a set of interacting objects. By default, the *javac* compiler implicitly imports several base packages from the standard library. the `-help` flag can display available options. For example, the following will compile using UTF-8 encoding while conforming to Java 1.8 features:
>javac -encoding UTF-8 -source 8 -target 8 Example.java

## Object-Oriented Programming
Although Java accommodates several paradigms, OOP is the foundation for most applications. In OOP, a program is organized into objects encapsulating related fields (representing its *state*) and methods (usually to control that state or perform related functions). When defining objects, Java reserves the keyword *class* (not to be confused with the *.class* file extension) which serves as their blueprint. An object in Java represents an instance in memory of a class, and also every class implicitly inherits from the *Object* superclass which provides useful convenience methods such as *equals()* and *toString()*. Java popularized several 'Pillars' of OOP design theory. While the numbers vary between OOP languages, Java focuses on four:

- **Abstraction** By simplifying objects to a set of useful features, we hide irrelevant details, reduce complexity, and increase efficiency. Abstraction is important at all levels of software and computer engineering, but essential to designing useful objects. Complicated real-world objects are reduced to simple representations.

- **Encapsulation** Objects should group together related variables and functions and be in complete control over them. So the state of an object should only change, if ever, through the object itself. Also known as data hiding, because the object has sole responsibility for its fields, and no outside object or function should interfere.

- **Inheritance** Code reuse is an important principle of programming (DRY - Don't Repeat Yourself), and new classes can reuse code from existing ones. This establishes a superclass-subclass (or parent-child) relationship where the derived classes inherit (and sometimes change) fields and methods from its parent.

- **Polymorphism** With inheritance, an object of a derived class can be referenced as instances of its parent class. This provides flexibility when invoking inherited methods with varying implementations in derived classes.

## Variables
A value is stored and identified in memory by a variable. Variables have a name that makes it possible to access the value, and a type that defines what sort of value it stores.
```java
int variableName = 64;
String txtVar = "Hello World";
```

## Primitive data types
Java handles two kinds of datatypes: primitives and references. Primitives are variables that store simple values. There are eight in Java.
- Integer types: **byte**, **short**, **int**, and **long** (42)  
- Floating-point types: **float**, and **double** (3.1415)  
- Logical types: **boolean** (true)  
- Character type: **char** ('x')

## Reference types
Reference types store the memory address location of more complex data types in the heap. Reference types include:
- Classes
- Interfaces
- Enums
- Arrays

## Naming variables
- Case sensitivity
- Can only use letters, numbers, and *$* or *_* characters
- Cannot begin with a number
- Cannot be a reserved Java keyword

## Scopes of a variable
A variable's reference will only exist within the context of its declared scope, which is based on the location of its declaration.

- **Static** or class scoped variables are visible to all instances of a related class.
- **Instance** or object scoped variables are visible to only that object instance.
- **Local** or method scoped variables are visible only within a method.
- **Block** or loop scoped variables are visible only within a block statement.

Be aware of *shadowing*: when two variables in different scopes share names.

## Methods
Methods accept a list of arguments known as *parameters* and return some value. They are used to implement repeatable, consistent actions on variable input, much like math functions.
```java
public int myMethod(int a, int b);
public int myMethod(int a);
```

## Constructors
Classes not only define object fields and methods, but how it should be instantiated through special methods called constructors. Constructors must have no return type and share the same name as its class. Java will automatically give you a *noargs* constructor. However, if you define any constructor, you will lose the automatically given constructor.

While a constructor may be *private*, used for singletons, it may not be *final*, *static*, or *abstract*.

## Access modifiers
- **private** - accessible only within the context of that class
- **default** - accessible within the context of a package, has no associated keyword so is set when no modifier is used
- **protected** - accessible to the package, but also to derived child classes outside of the package
- **public** - accessible anywhere

Classes should only be public or default. There are no cascading access levels, and unspecified fields will be default. Subclasses can only change inherited fields to be less restrictive.

## Arrays
### Declaration
Java Arrays are special reference types that store similarly typed data iteratively. A pair of brackets define an array of some data type, and can be written anywhere after the type:
```java
// One-Dimensional Arrays
int[] arrayOne;
int []arrayTwo;
int arrayThree[];

// Two-Dimensional Arrays
int[][] 2DArrayOne;
int 2DArrayTwo[][];
int []2DArrayThree[];
```

### Definition
While Java does not allow direct memory access to its arrays like other languages, they are still of fixed size once defined by the `new` keyword or by an array literal.
```java
// One-Dimensional Arrays
int[] instancedArray = new int[3];
int[] literalArray = {1, 2, 3};

// Two-Dimensional Arrays
int[][] instanced2DArray = new int[3][4];
int[][] literal2DArray = { { 1, 2 }, { 3, 4 }, { 5, 6 } };
```

### Iteration
Java for loops can iterate through arrays like most other languages:
```java
// One-Dimensional Arrays
for (int i = 0; i < arrayOne.length; i++) {
    System.out.print(arrayOne[i]);
}

// Two-Dimensional Arrays
for (int i = 0; i < 2DArrayOne.length; i++) {
    for (int j  =0; j < 2DArrayOne[i].length; j++) {
        System.out.print(2DArrayOne[i][j]);
    }
}

// Foreach loops
for (int i : arrayOne) {
    System.out.print(i);
}
```

### Manipulation
The `java.util.Arrays` class provides various methods for manipulating arrays.

```java
int[] messyArray = {234, 5346, 3, 64};
Arrays.sort(messyArray);
System.out.println(Arrays.toString(messyArray));
```

### Varargs
Varargs is a special parameter that can accept multiple arguments of the same type into a dynamically constructed array, and denoted by an ellipsis (...) instead of brackets. A varargs parameter must be the last or only parameter in a method signature. 
```java
varArgMethod("m", 1, 2, 5, 35, 346, 345, 4634);

...

public static void varArgDemo(String m, int... intArgs) {
    for (int i : intArgs) {
        System.out.print(i);
    }
}
```

## Exception Handling
When an something wrong occurs during execution, the current stack frame will throw an exception. If the exception is not handled, or thrown up the stack to be handled elsewhere, the program will crash. Good exception handling helps a program continue execution. Common issues which can throw exceptions involve stack or heap memory overflow, an array iterating out of bounds, or an interrupted stream or thread.

### Hierarchy
Exception and error objects extend Throwable and are either checked or unchecked.
* Throwable (checked)
    * Exception (checked)
        * RuntimeException (unchecked)
    * Error (unchecked)

Checked exceptions
Unchecked exceptions / Runtime exceptions
Errors
Runtime and unchecked exceptions refer to the same thing. We can often use them interchangeably. 

Checked Exceptions are compile-time issues that must be handled or thrown before the compiler can build, such as `IOException`. Unchecked Exceptions occur at runtime, so the compiler cannot predict them and does not force they be handled. Most unchecked exceptions extend RuntimeException, such as `NullPointerException`. Errors are serious issues and should not be handled, such as `StackOverflowError`.

### Throws
The `throws` keyword re-throws an exception up the stack to the method that called the throwing method. If the exception is continually thrown and never handled, the compiler will be satisfied in the case of checked exceptions but any issues will still break the program.
```java
public void methodThatThrows() throws IOException {
    // throw (singular) will throw a new exception every time.
    throw new IOException();
}

public void methodThatCalls() {
    methodThatThrows(); // IOException must now be handled here, or methodThatCalls() must use throws as well
}
```

### Try-Catch
The most basic form of exception handling is the try-catch:
```java
public void methodThatThrows() throws IOException {
    try {
        throw new IOException();
    } catch (IOException exception) {
        // Do something with the exception
        logger.warn("IOException thrown");
    }
}
```

A try block must be followed by at least one catch (or finally) block, but there can be any number of catch blocks for specific (or broad) exceptions. Catch blocks must be ordered from most specific to least specific Exception objects else later catch blocks catching subclasses of exceptions caught in catch blocks above it will become unreachable code.

Multiple exceptions can also be handled in one catch block:
```java
public void methodThatThrows() throws IOException {
    try {
        throw new IOException();
    } catch (IOException ex1 | ServletException ex2) {
        // Do something with the exception
        logger.warn("IOException thrown");
    }
}
```

### Finally
Try blocks can be followed by one finally block, and can either replace the mandatory single catch block or follow one or more catch blocks. They are always guaranteed to execute, even if no exceptions are thrown, and are useful for closing resources that may be left open in memory due to an interruption from a thrown exception.
```java
public void methodThatThrows() throws IOException {
    try {
        throw new IOException();
    } finally {
        System.out.println("Will always run");
    }
}
```

### Try-with-resources
Declaring and defining a resource - any object that implements AutoCloseable - within a pair of parenthesis after the try keyword removes the necessity of a finally block to close that resource.
```java
public void methodThatThrows() throws IOException {
    try (FileReader fr = new FileReader()) {
        throw new IOException();
    } catch (IOException exception) {
        logger.warn("IOException thrown");
    }
}
```

## I/O
### InputStream/OutputStream -> BufferedReader/BufferedWriter
The JVM can connect to external datasources such as files or network ports. InputStream/OutputStream and its implementations stream this data as an array of bytes whereas Reader/Writer and its implementations wrap InputStream/OutputStream to stream data as a char array. BufferedReader/BufferedWriter wraps Reader/Writer to stream several characters at a time, minimizing the number of I/O operations needed.

```java
// Overloaded BufferedReader constructors
BufferedReader sbr = new BufferedReader(new StringReader("Bufferedreader vs Console vs Scanner in Java"));
BufferedReader fbr = new BufferedReader(new FileReader("file.txt"));
BufferedReader isbr = new BufferedReader(new InputStreamReader(System.in));

// Autoclosable, works with try-with-resources syntax
try (BufferedReader reader = new BufferedReader(new FileReader("input.txt"))) {
	return readAllLines(reader);
}

// Prone to throwing IOExceptions
public String readAllLines(BufferedReader reader) throws IOException {
	StringBuilder content = new StringBuilder();
	String line;
	while ((line = reader.readLine()) != null) {
		content.append(line);
		content.append(System.ineSeparator());
	}
	return content.toString();
}
```

### Scanner
BufferedReader provides many convenient methods for parsing data. Scanner can achieve the same, but unlike BufferedReader it is not thread-safe. It can however parse primitive types and Strings with regular expressions. Scanner has a buffer as well but its size is fixed and smaller than BufferedReader by default. BufferedReader requires handling IOException while Scanner does not. Thus, Scanner is best used for parsing input into tokenized Strings.

```java
Scanner sc = new Scanner(new File("input.txt"));
Scanner issc = new Scanner(new FileInputStream("input.txt"));
Scanner csc = new Scanner(System.in);
Scanner strsc = new Scanner("A B C D");
```

### Properties
Load properties as key-value pairs from a file
//app.properties
```
key=value
```

```java
Properties props = new Properties();
props.load(new FileInputStream("app.properties");
String value = props.getProperty("key", "defaultValue");
```

## Generics
When passing objects into methods and data structures, a developer can overload or extend for its specific type or cast the object up and down its inheritance heirarchy. In contrast a generic type improves code reuse and type safety, reducing code by allowing methods and data structures to accept any type without risking dynamic runtime exceptions. Generic type parameters act as placeholders in a method signature while diamond operators specify the type for the compiler to enforce at compile time:

```java
ArrayList<String> list = new ArrayList<>();

public <T> String genericToString(T a) {   
    return a.toString();
}


public <T, E> String genericToStrinCat(T a, E b) {   
    return a.toString() + b.toString();
}
```

The type parameters T and E will be replaced by the compiler through type erasure:
```java
String s1 = genericToString(1);
String s2 = genericToString("Hello", 3.5);
```

## Collections Framework
Java's collections framework provides an API and reference implementations for common data structures

- **List** is an ordered collection of elements. A user has the ability to place an element anywhere in the list. The elements are accessable by their index. Unlike **Set**, **List** typically allows for duplicate elements such that element1.equals(element2). In addition to duplicates, **List** allow for multiple null elements to be stored.  
  
- **Set** is a collection of non duplicate elements meaning there will never exist a situation where element1.equals(element2). In addition to this, it is implied that there can only exist one null element due to the no duplicates rule. Some implementations also use **SortedSet** for proper ordering.

- **Queue** is a collection of elements who in essence cannot be iterated, instead the **Queue** follows the **FIFO** (First In First Out) rule. When an element is added to the **Queue** it is placed at the back and when an element is pulled it is pulled from the from the front (index :0).  
  
- **Deque** extends **Queue** but augments the ability to insert and remove elements at either end. The name is short for "Double Ended Queue" and is pronounced "Deck". Can be used as a LIFO (Last In First Out) Stack.
  
- **Map** is an interface which stores data with a key. A map cannot contain duplicate keys; each key can map to at most one value. **Map** can be visualized like a dictionary where only one word is paired with one definition. Unlike most other interfaces in the Collections Framework, it does not implement Collection nor Iterable. 

### Comparable vs Comparator
Comparable is a functional interface used to define a 'natural ordering' between instances of a class, commonly used by sorted collections such as TreeSet.

Comparator is another functional interface used in a dedicated utility class that can compare two different instances passed to it. It can be passed to a sort method, such as Collections.sort() or Arrays.sort(), or to sorted collections.

For example, to automatically sort a TreeSet of type Person according to age. We can either make the object class comparable or pass the constructor a comparator.

#### Comparable
```java
class Person implements Comparable<Person>{
	int age;
 
	Person(int age) {
		this.age = age;
	}
 
	@Override
	public int compareTo(Person o) {
		return o.age - this.age;
	}
}
 
public static void main(String[] args) {
	TreeSet<Person> persons = new TreeSet<Person>();
	persons.add(new Person(43));
	persons.add(new Person(25));
	persons.add(new Person(111));
}
```

#### Comparator
```java
class Person {
	int age;
 
	Person(int age) {
		this.age = age;
	}
}
 
class PersonAgeComparator implements Comparator<Person> {
	@Override
	public int compare(Person a, Person b) {
		return a.age - b.age;
	}
}
 
public static void main(String[] args) {
	TreeSet<Person> persons = new TreeSet<Person>(new PersonAgeComparator());
	persons.add(new Person(43));
	persons.add(new Person(25));
	persons.add(new Person(111));
}
```


## Reflection
Reflection allows one to examine or modify runtime behavior of a program. Java's Reflection API mostly allows introspection of structure, while modifying is only allowed on access modifiers of methods and fields. Many frameworks such as JUnit, Application/Servlet Containers, and Spring use reflection to examine class fields, construct objects, and invoke methods at runtime.

```java
Class<?> c = Class.forName("classpath.and.classname");
Object o = c.newInstance();
Method m = c.getDeclaredMethod("aMethod", new Class<?>[0]);
m.invoke(o);
```

## Threads
A *thread* is a unit of program execution that runs independently from other threads. Java programs can consist of multiple threads of execution that behave as if they were running on independent CPUs.

- `java.lang.Thread` is the Thread class representing a thread, which you can extend and then override its run() method. Afterwards, you call start().
- `java.lang.Runnable` is a functional interface (meaning only one method) which you can implement and then override run(). Afterwards, you can pass the object to a Thread instance and run start().
- The `synchronized` keyword is a modifier that can be used to write blocks of code, methods, or other resources to protect it in a multithreaded environment.
- `wait()` and `notify()` or `notifyAll()` methods of `java.lang.Object` can be used to suspend or wake up threads.

Besides the main thread, developers can instantiate their own when:

1. A custom class extends the `Thread` class 
2. A `Thread` is passed an implemented `Runnable` instance

Override the `run()` method in both cases to define the program to be run concurrently in the new thread, then call the Thread instance's `start()` method.

### Extend `Thread`
```java
public class CustomThread extends Thread {
    @Override
    public void run() {
        // Do something
    }

    public static void main(String[] args) {
        new CustomThread().start();
    }
}
```

### Implement `Runnable`
```java
public class CustomRunnable implements Runnable {
    @Override
    public void run() {
        // Do something
    }

    public static void main(String[] args) {
        new Thread(new CustomRunnable()).start();
    }
}
```

### Anonymous `Runnable` Class
```java
new Thread(new Runnable() {
        public void run() {
            // Do something
        }
    }).start();
```

### `Runnable` Lambda
```java
new Thread(
    () -> { /* Do something */ };
    ).start();
```

## Password Security & Authentication
Storing plain text passwords is a very bad idea. Often times security breaches leak spreadsheets and database dumps revealing user account information, including these passwords, which compromises not only these accounts but any others shared by users on other sites where these passwords may be reused. A basic solution hashes passwords, such as SHA, but there are easy ways to reverse them. A better approach is to add a few random bytes of data known as a 'salt' to make it harder to reverse. An even better solution however is to use encryption such as PBKDF2 or BCrypt

```java
String passwordToHash = "p4ssw0rd";

// Generate random salt
SecureRandom random = new SecureRandom();
byte[] salt = new byte[16];
random.nextBytes(salt);

// Option 1: Hash password using SHA + salt
MessageDigest md = MessageDigest.getInstance("SHA-512");
md.update(salt);
byte[] hashedPassword = md.digest(passwordToHash.getBytes(StandardCharsets.UTF_8));

// Option 2: Hash password using PBKDF2 + salt
KeySpec spec = new PBEKeySpec(passwordToHash.toCharArray(), salt, 131072, 128);
SecretKeyFactory factory = SecretKeyFactory.getInstance("PBKDF2WithHmacSHA1");
byte[] hashedPassword = factory.generateSecret(spec).getEncoded();
```

Using either option, both the hashed password and the salt should be saved in a database for future authentication.

```java
public String hashingMethod(String password, byte[] salt) {
    // return hash using SHA/Encryption + salt
}

public void createUser(String user, byte[] salt, byte[] hashedPassword) {
    String sql = "insert into users (username, salt, hash) values (?, ?, ?)";

    try (PreparedStatement pstmt = connection.prepareStatement(sql)) {
        pstmt.setString(1, user);
        pstmt.setBytes(2, salt);
        pstmt.setBytes(3, hashedPassword);
        pstmt.executeUpdate();
    } catch(NoSuchAlgorithmException | SQLException | UnsupportedEncodingException ex) {
        // log errors
    }
}

public boolean authenticateUser(String user, String password) {
    String hashedPassword;
    String salt;
    String sql = "select salt, hash from users where username = ?";
    
    try(PreparedStatement pstmt = connection.prepareStatement(sql)) {
        pstmt.setString(1, user);
        ResultSet resultSet = pstmt.executeQuery();

        resultSet.next();
        salt = resultSet.getBytes("salt");
        hashedPassword = new String(resultSet.getBytes("hash"));

        if (hashedPassword.equals(hashingMethod(password, salt))) {
            return true;
        } else {
            return false;
        }
    } catch(NoSuchAlgorithmException | SQLException | UnsupportedEncodingException ex) {
        return false;
    }
}
```
## Resources
### Articles
- [Data Structures and Algorithms in Java](https://www.javaworld.com/article/3527188/data-structures-and-algorithms-in-java-a-beginners-guide.html)
- [SOLID Java](https://filippobuletto.github.io/solid-java/#)
- [Java Versions and Features](https://www.marcobehler.com/guides/a-guide-to-java-versions-and-features)
- [Java Programming Cheatsheet](https://introcs.cs.princeton.edu/java/11cheatsheet/)
- [Structure of Java Virtual Machine](https://jakubstransky.com/2017/11/27/structure-of-java-virtual-machine-jvm/)
- [JVM Internals](https://blog.jamesdbloom.com/JVMInternals.html)
- [JVM Performance Optimization](https://www.javaworld.com/article/2078623/core-java-jvm-performance-optimization-part-1-a-jvm-technology-primer.html)
- [How the JVM Handles Exceptions](https://www.javaworld.com/article/2076868/how-the-java-virtual-machine-handles-exceptions.html)
- [How the JVM Performs Thread Synchronization](https://www.javaworld.com/article/2076971/how-the-java-virtual-machine-performs-thread-synchronization.html)

### Books
- [Think Java](https://books.trinket.io/thinkjava/index.html)
- [Wikibooks - Object Oriented Programming](https://en.wikibooks.org/wiki/Object_Oriented_Programming)
- [Wikibooks - Java Programming](https://en.wikibooks.org/wiki/Java_Programming)
- [Introduction to Programming Using Java, Eighth Edition](http://math.hws.edu/eck/cs124/javanotes8/)
- [Java Notes for Professionals](https://goalkicker.com/JavaBook/)
- [Open Data Sructures (in Java)](http://opendatastructures.org/ods-java/)
- [Inside the Java Virtual Machine](https://www.artima.com/insidejvm/ed2/)

### Documentation
- [Java Platform Standard Edition 8 Documentation](https://docs.oracle.com/javase/8/docs/index.html)
- [Java Platform Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/index.html)
- [Enhancements in Java SE 8](https://docs.oracle.com/javase/8/docs/technotes/guides/language/enhancements.html)
- [Java Virtual Machine and Language Specifications](https://docs.oracle.com/javase/specs/index.html)
- [The java.lang.* and java.util.* Packages](https://docs.oracle.com/javase/8/docs/technotes/guides/lang/index.html)
- [The Collections Framework](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/index.html)
- [Java I/O](https://docs.oracle.com/javase/8/docs/technotes/guides/io/index.html)
- [Java Generics](https://docs.oracle.com/javase/tutorial/extra/generics/)
- [Java Archive (JAR) Files](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/index.html)
- [Java Networking](https://docs.oracle.com/javase/8/docs/technotes/guides/net/index.html)
- [OpenJDK 8 documentation](https://devdocs.io/openjdk~8/)
- [OpenJDK 8 Standard Library](https://hg.openjdk.java.net/jdk8/jdk8/jdk/file/687fd7c7986d/src/share/classes/java)
- [JUnit 5](https://junit.org/junit5/docs/current/user-guide/)

### Tutorials
- [Oracle Java Tutorials](https://docs.oracle.com/javase/tutorial/index.html)
- [Java SE 8 Programmer I Exam Prep](https://docs.oracle.com/javase/tutorial/extra/certification/javase-8-programmer1.html)
- [IBM Intro to Java Programming](https://developer.ibm.com/series/intro-to-java-programming/)
- [Learn X in Y - Java](https://learnxinyminutes.com/docs/java/)
- [Baeldung](https://www.baeldung.com/)
- [Jenkov](http://tutorials.jenkov.com/)
- [Tutorialspoint](https://www.tutorialspoint.com/java/index.htm)

### Design Patterns
- [Java Design Patterns](https://java-design-patterns.com/)
- [The Catalog of Design Patterns](https://refactoring.guru/design-patterns/catalog)