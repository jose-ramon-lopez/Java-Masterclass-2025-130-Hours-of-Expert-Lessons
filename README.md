# Java-Masterclass-2025-130-Hours-of-Expert-Lessons

## Información general
java distingue entre mayúsculas y minúsculas

## jshell 
[JShell](https://docs.oracle.com/en/java/javase/21/jshell/introduction-jshell.html#GUID-630F27C8-1195-4989-9F6B-2C51D46F52C8)

<pre>
shell
|  Welcome to JShell -- Version 21.0.7
|  For an introduction type: /help intro


Listado de módulos cargados
/list -all

  s1 : import java.io.*;
  s2 : import java.math.*;
  s3 : import java.net.*;
  s4 : import java.nio.file.*;
  s5 : import java.util.*;
  s6 : import java.util.concurrent.*;
  s7 : import java.util.function.*;
  s8 : import java.util.prefs.*;
  s9 : import java.util.regex.*;
 s10 : import java.util.stream.*;

Listado de variables
jshell> /var
|    int result = 2
|    int previousResult = 3

 /exit
</pre>

 ## Your First Java Program: Displaying "Hello World" and Basic Error Handling
 jshell> System.out.print("Hello world");
Hello world

## Introduction to Variables, Keywords, and the Integer (int) Data Type
### keyworks
[keywords](https://docs.oracle.com/javase/specs/jls/se17/html/jls-3.html#jls-3.9)

### variables
Definir una variable <br>
dataType varName = value;

<pre>
ijshell> int intVar = 5;
intVar ==> 5

shell> System.out.print("la variable es " + intVar);
la variable es 5

intVar = 1 + 1;
</pre>

## Using Variables in Java Expressions: A Comprehensive Introduction
<pre>
int myFirstNumber = 35;
int mySecondNumber = 12:
int myThirdNumber = 6;

jshell> myFirstNumber = mySecondNumber + mythirdNumber
myFirstNumber ==> 35

jshell> /var
|    int myFirstNumber = 35
|    int mySecondNumber = 12
|    int myThirdNumber = 6

shell> int myTotal = myFirstNumber + mySecondNumber + myThirdNumber;
myTotal ==> 53
</pre>

## Exploring Java Primitive Types: Integer Ranges and Wrapper Classes
### primitive types
- byte 
- short
- int: 
- long
- float
- double
- char
- boolean

<pre>
int myMinIntValue = Integer.MIN_VALUE
myMinIntValue ==> -2147483648

int myMaxIntValue = Integer.MAX_VALUE
myMaxIntValue ==> 2147483647

</pre>

### Wrapper class
Proporciona operaciones simples e información para los 8 privitive types  
- Primitive: Wrapper Class
- byte: Byte
- short: Short
- int: Integer
- long: Long
- float: Float
- double: Double
- char: Character
- boolean: Boolean

Wrapper class
- .MIN_VALUE
- .MAX_VALUE
- ...

Warp around
- overflow
- underflow

Improve readability:
int myMaxInt = 2_147_483_647

## Understanding Byte, Short, and Long Data Types and Their Width in Java
Primitive data types para números enteros
- byte: Byte 8 bits 
- short: Short 16 bits
- int: Integer 32 bits
- long: Long 64 bits  

long myLong = 100 // es un int dentro de un long *Mal*
long myLong = 100L // L o l son válidos

## Understanding and Using Casting with Numeric Primitive Types in Java
short myMinShortValue = Short.MIN_VALUE; int myMinIntValue = Integer.MIN_VALUE
myMinShortValue ==> -32768
myMinIntValue ==> -2147483648

byte myMinByteValue = Byte.MIN_VALUE, myMaxBytevalue = Byte.MAX_VALUE
myMinByteValue ==> -128
myMaxBytevalue ==> 127

### casting
Java convierte a int (myMinByteValue / 2)
<pre>
byte myNewByteValue = (myMinByteValue / 2);
|  Error:
|  incompatible types: possible lossy conversion from int to byte
|  byte myNewByteValue = (myMinByteValue / 2);
</pre>

casting en convertir un tipo a otro
byte myNewByteValue = (byte)(myMinByteValue / 2);
myNewByteValue ==> -64

## Working with Float and Double: Precision in Floating Point Numbers
- float: Float: 32 bits sufijo F/f
- double: Double 64 bits sufijo D/d, tipo por defecto para floating point 

int myIntValue = 5; float myFloatValue = 5 ; double myDoubleValue = 5;
myIntValue ==> 5
myFloatValue ==> 5.0 
myDoubleValue ==> 5.0 

## Understanding Floating-Point Precision: A Practical Challenge in Java
jshell> int myIntValue = 5; float myFloatValue = 5f ; double myDoubleValue = 5d
myIntValue ==> 5
myFloatValue ==> 5.0
myDoubleValue ==> 5.0

jshell> myIntValue = 5 / 2 ;
myIntValue ==> 2

jshell> myFloatValue = 5f / 2f;
myFloatValue ==> 2.5

jshell> myDoubleValue = 5d / 2d;
myDoubleValue ==> 2.5

Para operaciones muy precisas usar la clase **BigDecimals**

## Exploring Character (char) and Boolean Primitive Data Types in Java
- char: 16bits comillas simples ''
- string: comillas dobles ""

### Unicode symbl.cc
jshell> char myUnicode = '\u0044';
myUnicode ==> 'D'

jshell> char myDecimalCode = 68;
myDecimalCode ==> 'D'

### boolean 
Puede ser true/false

## Recap of Primitive Types and Introduction to the String Class in Java
### string
Es una **clase** que Java deja trabajar de forma diferente, alberga hasta Integer.MAX_VALUE caracteres a entre comillas dobles
Es inmutable, los cambios destruyen el string y lo recrean.

String myString = "This is a string";

Operadores en string
- + concatenar

jshell> {
   ...>     String numberString = "250.55";
   ...>     numberString = numberString + "49.45";
   ...>     System.out.print(numberString);
   ...> }
250.5549.45


jshell> String lastString = "10"; int myInt=50;
lastString ==> "10"
myInt ==> 50

jshell> System.out.pri
print(     printf(    println(   
jshell> System.out.print(lastString + my
myInt      myString   
jshell> System.out.print(lastString + myInt)
1050

## Mastering Operators, Operands, and Expressions in Java Programming
### Operators
- = asignación
- + suma
- - resta
- * multiplicación

### Comentarios
- // comentario de línea

## Simplifying Java Code: Using Abbreviated Operators for Concise Operations
- variableName = variebleName + 1 // implicit cast a tipo variableName
- variableName++
- variableName -=1
- variableName--
-