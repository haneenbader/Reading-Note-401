## Java Basics 

**Variables**

Kinds of variables:

- Instance Variables (Non-Static Fields) :  Declared without the static keyword.

- Class Variables (Static Fields) : Declared with the static modifier.

- Local Variables : There is no special keyword designating a variable as local.

- Parameters : Parameters are always classified as "variables" not "fields".


**Naming**:

A variable's name can be any legal identifier — an unlimited-length sequence of Unicode letters and digits, beginning with a letter, the dollar sign "$", or the underscore character "_". 

**Primitive Data Types**

A primitive type is predefined by the language and is named by a reserved keyword.

Kinds of primitive data:

1- byte : The byte data type is an 8-bit signed two's complement integer. It has a minimum value of -128 and a maximum value of 127 (inclusive).

2- short : The short data type is a 16-bit signed two's complement integer. It has a minimum value of -32,768 and a maximum value of 32,767 (inclusive). 

3- int : By default, the int data type is a 32-bit signed two's complement integer, which has a minimum value of -231 and a maximum value of 231-1.

4- long : The long data type is a 64-bit two's complement integer. The signed long has a minimum value of -263 and a maximum value of 263-1.

5- float : The float data type is a single-precision 32-bit IEEE 754 floating point. 

6- double : The double data type is a double-precision 64-bit IEEE 754 floating point

7- boolean : The boolean data type has only two possible values: true and false.

8- char : The char data type is a single 16-bit Unicode character. It has a minimum value of '\u0000' (or 0) and a maximum value of '\uffff' (or 65,535 inclusive).

**Arrays**

An array is a container object that holds a fixed number of values of a single type. The length of an array is established when the array is created. After creation, its length is fixed. Each item in an array is called an element, and each element is accessed by its numerical index.


## ELI5: What does it mean to compile code?

When you compile code, the compilor (usually another program) takes the program the human wrote, and converts it into the program the computer can understand (i.e. converts from Java to machine language). The very short version could be, yes, compile means to make the code executable.


## Making Sense of Java’s API Documentation

Java has a whole collection of grammatical features, but Java is much more than just a big set of grammar rules.

**Searching for a term**

Java has a method named System.out.println. What follows describes two ways to look up the System.out.println method:

1- Using the index.

2- Using the list of classes.
