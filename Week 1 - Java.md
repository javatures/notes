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