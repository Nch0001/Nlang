# Access Modifiers
### public
>Accessible from other files
### private
>Accessible to only local file
### protected 
>Accessible to sub-classes only
    
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
>true or false

***

# Type inline
### byte
### short
### int
### long
### float
### double
### string
### bool
### void
>returns null

***

# Constants
### null
### true
### false

***

# Conditionals
### if
>Checks argument against conditionals
### elif
>If check against previous conditional is not true
### else
>If all previous conditionals failed

***

# Operands
### ^
>Exponential operator
### %
>Modulo operator

***

# Command Line Handlers
### in ""
>Reads an input with a given prompt.
### out ""
>Outputs a message with a newline added on the end.
### write ""
>Outputs a message directly.
### read #
>Reads from input the given amount of characters.

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
>`import nlang.file.Path;`

`Path path = new Path("directory")`

`Path[] Path.list()`

***

# Exceptions
### throw
>Outputs Exception
```
throw (new Exception())
```
Will stop the running of the code with the Exception provided.
### try
>Attempts to run something and automatically handles exceptions if no catch is supplied.
```
try {
    throw (new Exception());
}
```
Outputs: `ExceptionType: Exception Stacktrace`
### catch (Exception)
>Handles upon errors
```
try {
    print "Hello World!";
}catch (e as Exception) {
    print e.toString();
}
```

***

