# What is Nlang?
Nlang is a language based on Java/C++ syntax, with many frameworks built in, and is not expected to be functional anytime soon.

# Features of Nlang
```js
"Lol, nothing yet, it's not real!" /* True statement */
```
Only for now, of course.

# How to obtain/build Nlang

```js
"Well, just make it yourself, since there's no way to do it." // TODO: Implement language
```

***

> Before starting, please have a base understanding of programming languages. (Mainly `C++` and `Java`).

# Access Modifiers

### public

>Accessible from other files

<em><strong>oneFile.nl</strong></em>
```java
public string testString = "Hello World!"; 
```

<em><strong>anotherFile.nl</strong></em>
```java
import oneFile;

out(oneFile.testString; // Would output "Hello World!\n" to the terminal.
```

### private
>Accessible to only local file

<em><strong>oneFile.nl</strong></em>
```java
private string testString = "Hello World!"; 
```

<em><strong>anotherFile.nl</strong></em>
```java
import oneFile;

out(oneFile.testString; // Would throw a PrivateAccess error.
```

### protected 
>Accessible to sub-classes only

<em><strong>oneFile.nl</strong></em>
```java
protected string testString = "Hello World!"; 
```

<em><strong>anotherFile.nl</strong></em>
```java
import oneFile;

out(testString; // Would throw a PrivateAccess error.
```

<em><strong>anotherFile2.nl</strong></em>
```java
import oneFile;

public class e() extends oneFile {
  out(oneFile.testString); // Would output "Hello World!\n" to the terminal.
}
```
    
***

# Member Modifiers
### static
>Static Class Member
### final
>Unchanging
### const
>Static and Final

***

# Class Definition Types
### class

>Defined

### abstract

>Partially Defined

### facade

>Empty functions

***

# Logical Operators

### is

>Memory Address Check

### or

>Boolean Or

### not

>Boolean Inversion

***

# Types

### NullType

>Unbound value

### Class

>Unconstructed Class

### Number

>Superclass for all Numerical Types
- Byte
  - >8  bits
- Short
  - >16 bits
- Integer
  - >32 bits
- Long
  - >64 bits
- Float
  - >32 bit floating point single precision
- Double
  - >64 bit floating point double precision

### String

>"" or ''

### Boolean

>true or false (1 or 0)

***

# Type inline

### byte

>returns a 8 bit number. (-128 to 127 if signed, 0 to 256 if unsigned.)
### short
>returns a 16 bit number. (-32768 to 32767 if signed, 0 to 65535 if unsigned)
### int
>returns a 32 bit number. (-2147483648 to 2147483647, or 0 to 4294967295)
### long
>returns a 64 bit number. (Negative to positive ~9.22 Quintillion, or 0 to ~18.45 Quintillion)
### float
>returns a 32 bit floating point single precision number.
### double
>returns a 64 bit floating point double precision number.
### string
>returns a string object.
### bool
>returns a value indicating true or false (1 or 0).
### void
>returns null

***

# Constants
### null
> A value representing none, like the friends you have.
### true
> A value representing 1.
### false
> A value representing 0, also representing the amount of friends you have.

***

# Conditionals
### if
>Checks argument against conditionals
```java
if (null is null) {
  out("Hello World!");
}
```
### elif
>If check against previous conditional is not true
```java
if (null is true) {
  out("I'm a failure :(");
}elif (null is null) {
  out("Are you proud of me, dad?");
}
```
### else
>If all previous conditionals failed
```java
if (null == true) {
  out("I'm a failure :(");
}elif (true == null) {
  out("I'm a failure, too! :(");
}else {
  out("Hello World!"); 
} // In this instance "Hello World!" will output to the terminal, due to the fact null cannot equal true.
```

***

# Operands
### ^
>Exponential operator
```java
out(4 ^ 2); // outputs 16
```
### %
>Modulo operator
```java
out(5 % 3); // outputs 2
```
***

# Command Line Handlers
### in(" ")
>Reads an input with a given prompt.

```java
string input = in("Please enter a name: ");
```
### out(" ")
>Outputs a message with a newline added on the end.

```java
out("Hello World!"); // Outputs "Hello World!\n" to the terminal.
```

### write " "
>Outputs a message directly.

```java
write "Hello World!"; // Outputs "Hello World!" to the terminal.
```

### read #
>Reads from input the given amount of characters.
```java
string lines = read 4;
out(lines);
```
***

# System Library Management (nlang.lang.SysLib)

***

# File Library (nlang.file.File)
`BinaryFile/StringFile File.open(Path path, String mode)`

Mode can be `read (r)` `write (w)` `binary (b)` `append (a)` or a combination such as `rwb`, `ab`, `r`, `rw`, etc.

`String StringFile.read(long characters)`

`Byte[] BinaryFile.read(long characters)`
>Reads the file and returns an output. What else did you expect?


***

# Path Library (nlang.file.Path)
> To import the path library, do:
>
> `import nlang.file.Path;`

`Path path = new Path("directory")`

`Path[] Path.list()`

***

# Exceptions
### throw
>Outputs Exception
```Java
throw (new Exception())
```
Will stop the running of the code with the Exception provided.
### try
>Attempts to run something and automatically handles exceptions if no catch is supplied.
```Java
try {
    throw (new Exception());
}
```
Outputs: `ExceptionType: Exception Stacktrace`
### catch (Exception)
>Handles upon errors
```Java
try {
    out("Hello World!");
}catch (e as Exception) {
    out(e.toString());
}
```

***

