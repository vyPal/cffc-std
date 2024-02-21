# The standard library CaffeineC
This is the GitHub repository of the official standard library for the [CaffeineC](https://github.com/vyPal/CaffeineC) programming language.

# Packages
## I/O
```go
import "vyPal/cffc-std/io";
```
### **Function `printf(fmt: *i8): i32`**
The printf function that is builtin to clang
### **Function `sprintf(str: *i8, fmt: *i8): i32`**
The sprintf function that is builtin to clang
### **Function `print(format: *i8): void`**
Same as printf
### **Function `println(format: *i8): void`**
Same as printf, but adds an additional newline character
### **Function `input(prompt: *i8): *i8`**
Prints prompt and reads user input from command line until a newline character is received (or the __256 character limit__ is reached)
## Random
```go
import "vyPal/cffc-std/rand";
```
### **Function `initRandom(): void`**
Uses the `srand()` function from clang to initialize the random number generator
### **Function `randInt(min: i32, max: i32): i32`**
Generates a random 32-bit integer from min to max (both inclusive)
## Strings
```go
import "vyPal/cffc-std/strings";
```
### **Class `String`**
```yaml
string: *i8
```
#### **Method `constructor(s: *i8): void`**
Creates a new instance of the `String` class and sets the value of the `string` field to `s`
#### **Method `length(): i32`**
Returns the length of the string (not counting the null terminator)
#### **Method `parseI32(): i32`**
Uses the clang `atoi()` function to parse an `i32` from the instance of the `String` class
#### **Method `parseF32(): f32`**
Uses the clang `atof()` function to parse an `f32` from the instance of the `String` class
#### **Operator `==`**
Defines the comparison function for equals operator when used on two instances of this class
#### **Operator `+`**
Defines the function for addition operator when used on two instances of this class
#### **Getter `*i8`**
Defines the function for when an instance of this class is requested as a `*i8`
#### **Getter `i32`**
Same as `parseI32()`
#### **Getter `f32`**
Same as `parseF32()`