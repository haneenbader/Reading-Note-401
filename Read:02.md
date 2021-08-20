#  Arrays, Loops, Imports

## Packages and Import

**Package declaration :**

The statement order is as follows. Comments can go anywhere.

1- Package statment (optional).

2- Imports (optional).

3- Class or interface definitions.

**Imports: three options :**

-import javax.swing.;* : To make all classes visible altho only one is used.

-import javax.swing.JOptionPane; : To ake a single class visible.

-We can the fully qualified class name without an import. :


class ImportTest {

    public static void main(String[] args) {

        javax.swing.JOptionPane.showMessageDialog(null, "Hi");

        System.exit(0);

    }

}

## A Guide to Java Loops

Here are the types of loops that we can find in Java:

* Simple for loop: A for loop is a control structure that allows us to repeat certain operations by incrementing and evaluating a loop counter.

* Enhanced for-each loop.

* While loop: The while loop is Java's most fundamental loop statement. It repeats a statement or a block of statements while its controlling Boolean-expression is true.

* Do-While loop:The do-while loop works just like the while loop except for the fact that the first condition evaluation happens after the first iteration of the loop.

