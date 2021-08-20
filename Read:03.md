# Maps, primitives, File I/O

##  Java Primitives versus Objects

**Java Type System**

Java has a two-fold type system consisting of primitives such as int, boolean and reference types such as Integer, Boolean. Every primitive type corresponds to a reference type.


**Pros and Cons**

The primitive type variables have the following impact on the memory:

* boolean – 1 bit.

* byte – 8 bits.

* short, char – 16 bits.

* int, float – 32 bits.

* long, double – 64 bits.

**Performance**

The performance of a Java code is quite a subtle issue, it depends very much on the hardware on which the code runs, on the compiler that might perform certain optimizations, on the state of the virtual machine, on the activity of other processes in the operating system.

## Exceptions

**What Is an Exception?**

Definition: An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

**The Catch or Specify Requirement**

* A try statement that catches the exception. The try must provide a handler for the exception.

* A method that specifies that it can throw the exception. The method must provide a throws clause that lists the exception.


*The Three Kinds of Exceptions :*

1- Checked exception.

2- Error exception.

3- Runtime exception.

## Scanning

Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.

**Breaking Input into Tokens**

- Scanner uses white space to separate tokens.

-  ScanXan invokes Scanner's close method when it is done with the scanner object. 

- To use a different token separator, invoke useDelimiter(), specifying a regular expression. 
