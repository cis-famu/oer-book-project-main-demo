# Introduction to C++ Programming

## Objectives
After completing this chapter students will be able to:
1. Identify basic components of a C++ program, including functions, special symbols, and identifiers
2. Classify simple data types and use them in assignment statements
3. Use arithmetic operators, precedence, and expressions
4. Create assignment and input statements and the use of variables within statements.
5. Differentiate between type conversion and type casting
6. Develop output results using output statements
7. Identify syntax errors and debugging techniques
8. Write a basic C++ program

## Introduction
In this chapter, we explore the fundamental elements of C++ programming, providing a comprehensive foundation for aspiring programmers. We begin by understanding the basic components of a C++ program, including the significance of functions, special symbols, and identifiers. Functions act as modular blocks of code, enhancing code organization, while special symbols and identifiers define variables and entities within the program for efficient data manipulation.

Next, we delve into data types and assignment statements, crucial for storing and manipulating different data in C++. Learning how to use simple data types in assignment statements allows programmers to initialize and modify variables with ease. Additionally, we explore arithmetic operators, their precedence, and expressions, enabling the creation of complex mathematical computations in C++ programs.

Furthermore, we delve into input and output statements, providing interactive capabilities and result display to users. Handling user input and formatting output are essential skills for creating user-friendly programs. We differentiate between type conversion and type casting, understanding their distinct purposes and applications in ensuring data integrity. Lastly, we identify common syntax errors and explore debugging techniques to resolve issues and ensure smooth program execution.

Through hands-on experience, readers will write their own basic C++ program, solidifying their understanding and empowering them to tackle more advanced programming challenges with confidence. This chapter equips learners with essential skills and knowledge to harness the full potential of C++ programming and embark on a rewarding coding journey.

## Basic Elements
As aspiring programmers embark on their journey to learn C++, they encounter several foundational elements that form the building blocks of this powerful and versatile programming language. This section explores four fundamental components of C++: comments, reserved words, identifiers, and functions.

Functions are essential elements of C++ that enable programmers to encapsulate blocks of code and execute them when needed. They facilitate modular programming, where code is organized into smaller, reusable components, enhancing code readability and maintainability. Functions can accept arguments, perform specific tasks, and return values to the caller. Understanding comments, reserved words, identifiers, and functions empowers developers to write clean, efficient, and well-structured C++ code that serves as a solid foundation for creating sophisticated applications and software solutions. As programmers master these basic elements of C++, they lay a solid groundwork to explore the language’s more advanced features and tackle complex programming challenges. We will go into more detail on this topic in a later chapter.

### Comments
Comments play a crucial role in any programming language, providing a means for programmers to annotate their code. They are non-executable lines of text intended for human readers and are ignored by the compiler during code compilation. Comments serve as documentation, explanations, or reminders for the code logic, making it easier for developers to understand, maintain, and collaborate on projects.

C++ allows for two styles of comments. The first is the in-line comment. This is done by using  `//` (two foraward slashes). All text following this symbol is part of the comment.

For example:

```cpp
int name; //student name
tax = cost * 0.12; //tax amount on cost
```

The second type of comment allowed is multiple-line comments. This allows the programmer to write longer comments that cover multiple lines. Multiple-line comments are enclosed in /* and */. 

For example:

```cpp
/* 
    Comments can be written
    on multiple lines as needed.
*/
```
### Reserved Words (Keywords)

Reserved words, also known as **keywords**, are specific words with predefined meanings in the C++ language. They serve as the building blocks for creating instructions, expressions, and program structures. Since they are reserved for specific purposes, programmers cannot use them as identifiers (variable names, function names, etc.) for their code. Understanding these reserved words is essential as they form the backbone of C++ syntax and define the language's grammar. 

For example:

```cpp
    int, float, double, bool, if, else, do, while, return, const
```

*Note: Reserve words are usually highlighted in different color by the IDE.*

### Identifiers

In the world of programming, identifiers play a crucial role in defining and accessing various entities in a codebase. In C++, an identifier is a name given to a program element such as variables, functions, classes, objects, labels, and user-defined types. These names act as labels, allowing programmers to reference and manipulate these entities within their code.

This section aims to provide a comprehensive understanding of identifiers in C++, their rules, best practices, and how they contribute to the overall structure and readability of a C++ program.

#### Rules for Naming Identifiers

C++ imposes certain rules and conventions for naming identifiers to maintain code clarity and avoid conflicts. It's essential to follow these rules to ensure code readability and portability across different platforms and compilers. The rules for naming C++ identifiers are as follows:

1. Valid Characters: Identifiers can consist of letters (both uppercase and lowercase), digits, and underscores (_). The first character must be a letter or an underscore. C++ is case-sensitive, meaning identifiers "myVariable" and "MyVariable" are distinct.
2. Reserved Keywords: C++ has a set of reserved keywords that cannot be used as identifiers since they have predefined meanings in the language. Examples of such keywords are "if," "else," "while," "class," "int," and "return."
3. Length Limitation: Identifiers can be of any length, but only the first few characters are significant. Most compilers limit the length of an identifier, often to 255 characters.
4. Unicode Support: C++ supports Unicode characters in identifiers, allowing for a more extensive range of naming possibilities.
5. Namespace Scope: Identifiers within a namespace scope should have unique names. To avoid naming conflicts, use descriptive names that reflect the content or purpose of the entity.
6. Global Scope: Identifiers in the global scope should be used judiciously to prevent name clashes in large projects. It's a good practice to use unique prefixes or namespaces for global identifiers.
7. Underscore Convention: Identifiers beginning with an underscore followed by a capital letter (e.g., "_MyIdentifier") and identifiers containing two consecutive underscores are reserved for the compiler and standard library. Avoid using such names to prevent unintended behavior.


| Valid Identifier Names | Invalid Identifier Names |
|-----------------------|-------------------------|
| age                   | 123num                  |
| userName              | float                  |
| _count                | for                    |
| MyVariable            | break                  |
| MAX_SIZE              | while                  |
| isValid               | if                     |
| _value1               | 1_value                 |
| TotalSales            | double                 |
| num_students          | my-variable            |
| PI                    | 3.14                   |


<details>
    <summary>Explanation</summary>
    
1. Valid Identifier Names:
    - Valid identifiers consist of letters (both uppercase and lowercase), digits, and underscores (_).
    - They must start with a letter or an underscore.
    - They cannot be C++ keywords, as they have predefined meanings in the language.
    - Examples: "age," "userName," "_count," "MyVariable," "MAX_SIZE," "isValid," "_value1," "TotalSales," "num_students," and "PI."

2. Invalid Identifier Names:
    - Invalid identifiers have spaces, special characters, or start with digits.
    - They cannot be C++ keywords.
    - Examples: "123num" (starts with a digit), "float" (a C++ keyword), "for" (a C++ keyword), "break" (a C++ keyword), "while" (a C++ keyword), "if" (a C++ keyword), "1_value" (starts with a digit), "my-variable" (contains a hyphen), and "3.14" (contains a decimal point).
</details>


#### Best Practices for Naming Identifiers

While adhering to the rules is essential, adopting certain best practices for naming identifiers can significantly enhance the maintainability and comprehensibility of C++ code.

1. Descriptive Names: Choose meaningful and descriptive names for variables, functions, and classes. The name should convey the purpose or content of the entity. For instance, use "numStudents" instead of "n" to represent the number of students.
2. CamelCase: For multi-word identifiers, follow the CamelCase convention, where the first letter of each word is capitalized (e.g., "calculateGrossSalary").
3. Avoid Abbreviations: Minimize the use of abbreviations, as they can be ambiguous and unclear to other programmers. Prioritize readability over brevity.
4. Consistency: Maintain a consistent naming style throughout the codebase. Consistency simplifies code reviews and makes it easier for developers to understand the code written by others.
5. Avoid Hungarian Notation: In the past, Hungarian Notation was a popular naming convention, but it has fallen out of favor. Avoid using prefixes that denote the data type of a variable, such as "i" for integers or "sz" for zero-terminated strings.
6. Use Function Names as Actions: When naming functions, use verbs to indicate actions, such as "calculate," "initialize," or "print."

Identifiers are the building blocks of a C++ program, allowing programmers to create, reference, and manipulate various entities. By following the rules and best practices for naming identifiers, developers can write clean, readable, and maintainable code that is less prone to errors and easier to collaborate on within a team. Taking the time to choose descriptive and meaningful names for identifiers will go a long way in making your codebase more robust and comprehensible.

### Review Questions

1. True/False: Functions in C++ are used primarily to enhance code readability and maintainability by organizing code into smaller, reusable components.

2. Which of the following elements are explored as foundational components of C++ in this section?

   a) Loops, arrays, pointers, and classes
   b) Comments, reserved words, identifiers, and functions
   c) Variables, constants, conditionals, and libraries
   d) Inheritance, polymorphism, encapsulation, and abstraction
   
3. Functions in C++ can accept _______ , perform specific tasks, and return values to the caller.

*Answers: 1. true  2. b  3. arguments*

## Data Types

In C++, data types are fundamental building blocks that define the type of data a variable can hold. They play a crucial role in determining the size and behavior of variables during program execution. Understanding basic data types in C++ is essential for writing efficient, platform-independent, and error-free code.

This section provides an in-depth exploration of the basic data types available in C++, their memory representation, and the range of values they can hold.

### Built-in Data Types

C++ provides several built-in or fundamental data types that can be broadly categorized into the following groups:

1. Integer Types:
   - `int`: Represents signed integers and typically uses 4 bytes on most systems. The range of values is approximately -2 billion to +2 billion.
   - `short`: Represents short signed integers and uses 2 bytes. The range is usually -32,768 to +32,767.
   - `long`: Represents long signed integers and uses 4 bytes (or 8 bytes on some systems). The range is platform-dependent but is typically larger than that of `int`.
   - `long long`: Represents very long signed integers and uses 8 bytes. Introduced in C++11, it provides a larger range than `long`.

2. Floating-Point Types:
   - `float`: Represents single-precision floating-point numbers using 4 bytes. It has approximately 7 decimal digits of precision.
   - `double`: Represents double-precision floating-point numbers using 8 bytes. It has approximately 15 decimal digits of precision.
   - `long double`: Represents extended-precision floating-point numbers, which provide even higher precision than `double`.

3. Character Types:
   - `char`: Represents a single character and uses 1 byte. It can hold ASCII characters or small integer values.

4. Boolean Type:
   - `bool`: Represents a Boolean value, which can be either `true` or `false`. It uses 1 byte internally to store the value.

### Strings

In C++, strings are a fundamental data type used to store sequences of characters, such as words, sentences, or even entire paragraphs. String variables play a crucial role in handling textual data, enabling developers to work with human-readable information in their programs.


To work with strings in C++, we must include the `<string>` header. String variables can be declared and initialized using different methods. For instance:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    // Method 1: Using string literals
    string name = "John";

    // Method 2: Using the constructor
    string message("Hello, C++!");

    // Method 3: Using assignment
    string fruit;
    fruit = "apple";

    return 0;
}
```

In this example, we demonstrate three ways to declare and initialize string variables.

### Review Questions

1. Multiple Choice: Which of the following is NOT a basic data type in C++?
   a) int
   b) float
   c) string
   d) double
   
2. Completion: This data type in C++ is used to store single characters, such as 'A', '5', or '&'. _______
3. True/False: The "bool" data type in C++ is used to represent boolean values and can have two possible states: true or false.

*Answers: 1. c   2. char   3. true*

## Variable Declaration and Initilizations 

Variables are fundamental components of any programming language, including C++. They are used to store and manipulate data during program execution. In C++, variables must be declared before they are used, indicating their data type and providing a name that acts as a reference to access and modify their values.

This section explores the process of declaring variables in C++, their initialization, and the significance of proper initialization for ensuring predictable behavior and avoiding potential bugs.

### Variable Declaration

In C++, variable declaration is the process of specifying the data type and name of a variable. The general syntax for variable declaration is as follows:

```cpp
data_type variable_name;
```

For example:

```cpp
int age;
double salary;
char grade;
```

Variables must be declared before they are used in a program. By declaring variables at the beginning of a function or a code block, programmers ensure that all the necessary variables are known to the compiler before they are referenced.

### Variable Initialization

Variable initialization is the process of assigning an initial value to a variable at the time of declaration. It is essential to initialize variables before using them to avoid undefined behavior and potential bugs that may arise from accessing uninitialized memory.

There are different ways to initialize variables in C++:

1. Direct Initialization:

```cpp
int count = 0;
double pi = 3.14159;
char grade = 'A';
```

2. Copy Initialization:

```cpp
int score = count;
```

3. Uniform Initialization (C++11 and later):

```cpp
int quantity{10};
double temperature{98.6};
char initial{'J'};
```

4. Default Initialization:

```cpp
int age{};      // Initializes 'age' to 0 (for built-in types)
double weight{}; // Initializes 'weight' to 0.0
char letter{};  // Initializes 'letter' to '\0' (null character)
```

### Importance of Initialization

Proper initialization of variables is crucial for several reasons:

1. Preventing Undefined Behavior: Accessing the value of an uninitialized variable leads to undefined behavior, which may result in unexpected program crashes or incorrect results.
2. Deterministic Behavior: Initialization provides a predictable starting point for variables, ensuring consistent behavior across different environments and compilers.
3. Avoiding Bugs: Uninitialized variables are a common source of bugs, and thorough initialization practices can help catch potential issues early in the development process.
4. Code Readability: Initializing variables explicitly enhances code readability and makes it easier for other developers to understand the code's intent.


### Review Questions

1. In C++, variable declaration refers to:
   a) Assigning a value to a variable
   b) Creating a new variable with a name and data type
   c) Changing the value of an existing variable
   d) Printing the value of a variable to the console


2. True/False: In C++, it is mandatory to initialize a variable at the time of declaration.

3. When declaring and initializing a variable in C++, the value assigned to the variable must be of the same data type as the variable itself. For example, to declare and initialize an integer variable "age," which of the following statements is correct?
a) int age = "25";
b) int age = '25';
c) int age = 25;
d) int age = 25.0;

*Answers: 1. b   2. false   3. c*

## Assignment Statements

Assignment statements are fundamental to programming in C++ and many other programming languages. They allow programmers to assign values to variables, modify existing values, and update the state of a program during its execution. Understanding how to use assignment statements effectively is crucial for manipulating data and controlling program flow.

This section explores the syntax of assignment statements in C++, their usage for different data types, and common pitfalls to avoid.

### Basic Syntax of Assignment Statements

In C++, the assignment operator (`=`) is used to assign a value to a variable. The general syntax of an assignment statement is as follows:

```cpp
variable_name = value;
```

For example:

```cpp
int age = 30;
double pi = 3.14159;
char grade = 'A';
```

The value on the right side of the assignment operator is assigned to the variable on the left side.

### Modifying Variables with Assignment

Assignment statements are not limited to initializing variables. They can also be used to modify the values of existing variables. For instance:

```cpp
int count = 10;
count = count + 1; // Incrementing 'count' by 1
```

This code snippet increments the value of the `count` variable by 1 using the assignment statement. Similarly, various mathematical and logical operations can be performed on variables using the assignment operator.

### Assignment with Expressions

C++ allows more complex expressions on the right-hand side of the assignment operator. These expressions can involve multiple variables, constants, and arithmetic or logical operators. For example:

```cpp
int a = 5, b = 3, c = 7;
a = b + c; // Assigning the sum of 'b' and 'c' to 'a'
```

In this example, the value of `b + c` is calculated and assigned to the variable `a`.

### Chained Assignment

C++ supports chained assignment, which allows multiple variables to be assigned the same value in a single statement:

```cpp
int x, y, z;
x = y = z = 10; // All variables are assigned the value 10
```

Here, `z` is assigned the value 10 first, and then that value is assigned to `y`, and finally, the same value is assigned to `x`.

### Review Questions

1. Multiple Choice: In C++, which symbol is used to assign a value to a variable in an assignment statement?
   a) ==
   b) =
   c) :
   d) ->

2. Write the correct assignment statement to assign the value 7 to a variable named "count." __________

3. True/False: In C++, the left side of an assignment statement must always be a variable.

*Answers: 1. b &nbsp;&nbsp; 2. count = 7 &nbsp;&nbsp;3. true*

## Arithmetic Operators, Precedence, and Expressions

Arithmetic operators are fundamental components of C++ that allow programmers to perform various mathematical computations on numeric data types. These operators enable the manipulation of variables and constants to solve mathematical problems and make numerical calculations within a program.

This section explores the common arithmetic operators in C++, their usage, and how to create expressions to perform complex mathematical operations.

### Common Arithmetic Operators

C++ provides the following arithmetic operators:

1. Addition (`+`): Adds two operands together.
2. Subtraction (`-`): Subtracts the right operand from the left operand.
3. Multiplication (`*`): Multiplies two operands.
4. Division (`/`): Divides the left operand by the right operand.
5. Modulus (`%`): Calculates the remainder when the left operand is divided by the right operand.

For example:

```cpp
int a = 5, b = 3;
int sum = a + b; // sum will be 8
int difference = a - b; // difference will be 2
int product = a * b; // product will be 15
int quotient = a / b; // quotient will be 1
int remainder = a % b; // remainder will be 2
```

### Precedence of Arithmetic Operators

In C++, arithmetic operators have different precedence levels, determining the order of evaluation when multiple operators appear in a single expression. The following table presents the precedence of arithmetic operators, from highest to lowest:

| Operator | Description                   |
|----------|-------------------------------|
| `()`     | Parentheses                   |
| `*`, `/`, `%` | Multiplication, Division, Modulus |
| `+`, `-` | Addition, Subtraction          |

For example:

```cpp
int result = 5 + 4 * 2; // result will be 13 (4 * 2 is evaluated first, then added to 5)
int anotherResult = (5 + 4) * 2; // anotherResult will be 18 (5 + 4 is evaluated first, then multiplied by 2)
```

### Creating Expressions

Expressions in C++ consist of variables, constants, and operators combined to perform computations. Using arithmetic operators, programmers can create expressions to solve complex mathematical problems within their code.

For example:

```cpp
// Area of a rectangle
int length = 5, width = 3;
int area = length * width;

// Celsius to Fahrenheit conversion
double celsius = 30.0;
double fahrenheit = (celsius * 9.0 / 5.0) + 32.0;
```

In the first example, the expression `length * width` calculates the area of a rectangle. In the second example, the expression `(celsius * 9.0 / 5.0) + 32.0` converts a temperature in Celsius to Fahrenheit.

### Compound Assignment Operators

C++ also provides compound assignment operators that combine arithmetic operations with assignment in a single statement. These operators can simplify code and make it more concise. Some common compound assignment operators are:

- `+=` (Addition and assignment)
- `-=`` (Subtraction and assignment)
- `*=` (Multiplication and assignment)
- `/=` (Division and assignment)
- `%=` (Modulus and assignment)

For example:

```cpp
int value = 10;
value += 5; // equivalent to value = value + 5
value *= 2; // equivalent to value = value * 2
```

### Review Questions

1. In C++, which arithmetic operator is used for the remainder (modulus)?
   a) ^
   b) **
   c) %
   d) *

Answer: a) ^

2. What is the result of the following expression in C++? `int result = 10 + 5 * 2;` ________

3. True/False: In C++, parentheses are used to specify the order of evaluation and override the default operator precedence.

*Answers: 1. c 2. 20 3. true*

## Type Casting and Conversions

In C++, type casting and conversions play a vital role in manipulating data of different types within a program. Type casting allows programmers to explicitly change the data type of a variable, while type conversions automatically occur when data of one type is assigned to another type.

This section explores the concepts of type casting and conversions in C++, their various forms, and the importance of handling them carefully to ensure data integrity and program correctness.

### Implicit Type Conversions

Implicit type conversions, also known as type coercion, occur automatically when the compiler converts data from one type to another. These conversions are performed when the assignment or operation is considered safe and will not result in a loss of data.

For example:

```cpp
int num1 = 10;
double num2 = num1; // Implicitly converts int to double
```

In this example, the integer value `10` is implicitly converted to a double before being assigned to `num2`.

### Explicit Type Casting

Explicit type casting, also called type casting or type conversion, allows programmers to manually convert data from one type to another. It is done by specifying the desired type in parentheses before the value or variable to be converted.

For example:

```cpp
double num1 = 3.14;
int num2 = static_cast<int>(num1); // Explicitly converts double to int
```

In this example, the double value `3.14` is explicitly cast to an integer using `static_cast`.

### Narrowing and Loss of Data

One significant consideration when using type casting is the possibility of narrowing conversions, where data may be lost when converting from a larger data type to a smaller one. This can result in truncated values, leading to unexpected behavior in the program.

For example:

```cpp
int num1 = 1000;
short num2 = static_cast<short>(num1); // Narrowing conversion (may lose data)
```

In this case, the value `1000` is within the range of `short`, but if the value were larger, data loss would occur.

### Review Question

1. Multiple Choice: In C++, what is the purpose of type conversion?
   a) To convert text into binary code
   b) To convert one data type into another
   c) To create new data types
   d) To automatically detect data types during runtime

2. Completion: Complete the following C++ statement to explicitly cast the variable "value" from a double to an integer:
```cpp
int result = _____(value);
```

3. True/False: Implicit type conversion in C++ is also known as "casting."
    
*Answers: 1. b 2. `static_cast<int>` 3. false* 

## Input Statements

Input statements in C++ are essential for interacting with users and obtaining data from external sources, such as files or other programs. They allow programmers to prompt users for input and store that input into variables, enabling dynamic and interactive behavior in their programs.

This section explores input from the standard input stream (keyboard).

### Input from the Standard Input Stream

In C++, the standard input stream (`std::cin`) is used to read data from the user via the keyboard. To read input from the user, the `>>` extraction operator is used, followed by the variable where the input should be stored.

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Enter your age: ";
    cin >> age;
    cout << "You entered: " << age << endl;
    return 0;
}
```

In this example, the user is prompted to enter their age, and the input is read into the variable `age` using `std::cin`.

### Review Questions
1. Complete the C++ code to read a string input entered by the user:
```cpp
string name;
______ >> name;
```


2. In C++, which library should be included to enable keyboard input using "cin" and "getline" for reading strings?
   a) `<stdio.h>`
   b) `<fstream>`
   c) `<string>`
   d) `<iostream>`


3. True/False: In C++, when reading input using "cin," if the user enters a space or a newline character, the input will be ignored, and the program will wait for valid input to be entered.

*Answers: 1. cin 2. d 3. true*    

## Output Statements

Output statements in C++ are used to display data and results to the user, write data to files, or communicate with other programs. They allow programmers to present information generated during program execution in a human-readable format.

This section explores the output to the standard output stream (console). 

### Output to the Standard Output Stream

In C++, the standard output stream (`std::cout`) is used to display data on the console. To output data, the `<<` insertion operator is used, followed by the data to be displayed.

```cpp
#include <iostream>
using namespace std;

int main() {
    int age = 30;
    cout << "Your age is: " << age << endl;
    return 0;
}
```

In this example, the program uses `std::cout` to display the message "Your age is: " followed by the value stored in the variable `age`.

### Review Questions

1. Complete the C++ code to display the message "Hello, World!" on the screen :
```cpp
______ << "Hello, World!";
```

2. In C++, which of the following manipulators is used to insert a newline character into the output stream?
   a) \n
   b) endl
   c) \t
   d) \r


3. In C++, when using "cout" to display multiple values on the same line, you can separate the values with commas to automatically add spaces between them.

*Answers: 1. cout 2. b 3. false*

## Creating a C++ Program

Creating a simple C++ program involves a series of steps to define, write, compile, and execute the code. This section provides a step-by-step guide to create a basic C++ program, from setting up the development environment to running the program.

### Step 1 - Install a C++ Compiler

The first step is to install a C++ compiler on your system. Several popular C++ compilers are available, such as GCC (GNU Compiler Collection), Clang, and Microsoft Visual C++. Choose the one that best suits your platform and requirements.

### Step 2 - Choose an Integrated Development Environment (IDE) (Optional)

While not mandatory, using an Integrated Development Environment (IDE) can significantly simplify the development process. IDEs provide a user-friendly interface for code writing, debugging, and managing projects. Some popular C++ IDEs include Visual Studio Code, Code::Blocks, and JetBrains CLion.

### Step 3 - Create a New C++ Source File

Once the compiler and IDE (if chosen) are set up, create a new C++ source file with the ".cpp" extension. This file will contain the C++ code for your program. You can use a text editor or the built-in code editor in your chosen IDE.

### Step 4 - Write the C++ Code

In the C++ source file, start writing your code. A simple C++ program typically consists of the `main` function, which is the entry point of the program. The `main` function contains the code that will be executed when the program runs.

Here's an example of a simple C++ program that prints "Hello, World!" to the console:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

### Step 5 - Save the Source File

After writing the C++ code, save the source file with a descriptive name and the ".cpp" extension. This will allow the compiler to recognize it as a C++ source file.

### Step 6 - Compile the Program

To convert the human-readable C++ code into machine-executable instructions, you need to compile the program. Open a terminal or the command prompt, navigate to the directory where the source file is saved, and use the appropriate compiler command to compile the program.

For example, using GCC:

```
g++ -o my_program my_program.cpp
```

This will produce an executable file named "my_program" (or whatever name you choose) in the same directory.

### Step 7 - Run the Program

Once the program is successfully compiled, you can run it by executing the generated executable file.

For example, on Windows:

```
my_program.exe
```

On Linux/macOS:

```
./my_program
```

After running the program, you should see the output "Hello, World!" displayed on the console.

### Step 8 - Debug and Test (Optional)

If your program doesn't produce the expected output or behaves unexpectedly, you may need to debug and test it. Debuggers available in some IDEs can help identify and fix errors in the code. Additionally, thorough testing ensures that your program works correctly under various scenarios.

## Chapter Summary

- Functions are essential elements of C++ that facilitate modular programming, where code is organized into smaller, reusable components, enhancing code readability and maintainability.
- Comments are non-executable lines of text intended for human readers and are ignored by the compiler during code compilation and play a crucial role in any programming language, providing a means for programmers to annotate their code.
- There are two types of comments inline (//) and multiple line (/* */)
- Reserved words, also known as keywords, are specific words with predefined meanings in the C++ language.
- An identifier is a name given to a program element, such as variables, functions, classes, objects, labels, and user-defined types, and acts as labels, allowing programmers to reference and manipulate these entities within their code.
- Data types are fundamental building blocks that define the type of data a variable can hold
- There are four main categories of built-in data types: integer, floating point, character, and boolean. The most common data types are int, long, float, double, char, and bool. 
- Strings are a fundamental data type used to store sequences of characters, such as words, sentences, or even entire paragraphs.
- Strings require the inclusion of the `<string>` header
- Initializing variables is important for preventing undefined behavior, avoiding bugs, increasing code readability, and creating predictable behavior
- The assignment operator (=) is used to assign a value to a variable 
- C++ supports chained assignment, which allows multiple variables to be assigned the same value in a single statement
- The main operators in C++ are +, -, *, /, and %
- Type casting allows programmers to explicitly change the data type of a variable, while type conversions automatically occur when data of one type is assigned to another type. 
- The standard input stream (std::cin) is used to read data from the user via the keyboard. 
- To read input from the user, the >> extraction operator

## Key Terms

assignment operator
    : =; assigns whatever is on the right side to the variable on the left side
    
data types
    : a set of values together with a set of operations

function
    : a collection of statements; when activated, or executed, it accomplishes something
    
identifiers
    : a C++ identifier consists of letters, digits, and the underscore character (`_`); it must begin with a letter or underscore
    
initialized
    : the first time a value is placed in the variable
    
keywords
    : reserved words that have predefined meanings and functionalities within the programming language

output statement
    : an output on the standard output device via cout and <<

variable
    : A memory location whose content may change during program execution.

## Programming Exercises

**Fruit Basket**
Lucas went to the market to buy fruits for a fruit basket for a party. He wants to create a balanced mix of three types of fruits: apples, oranges, and bananas. However, he's not sure how many of each fruit to buy. Each of his friends prefers a different type of fruit. The program should input the number of friends attending the gathering who prefer apples, oranges, and bananas, respectively. Your program should output three integers, representing the total number of each type of fruit Lucas should buy for the fruit basket.

To calculate the number of fruits for each type, Lucas needs to ensure that the ratio of apples, oranges, and bananas matches the ratio of his friends' preferences. Since he wants a balanced mix, he will divide the number of each fruit preference by the smallest value among them and use that as the ratio.

**Example**
```
Preferences (apples, oranges, bananas): 5 3 2
Number of apples, oranges, and bananas: 10 6 4
```

## References

C++ strings. Programiz. (n.d.-a). https://www.programiz.com/cpp-programming/strings 

C++ type conversion. Programiz. (n.d.-b). https://www.programiz.com/cpp-programming/type-conversion 

Deitel, P. J., &amp; Deitel, H. M. (2020). C++ how to program. Pearson. 

GeeksforGeeks. (2023, March 16). C++ variables. GeeksforGeeks. https://www.geeksforgeeks.org/cpp-variables/ 

Malik, D. S. (2018). C++ programming: From problem analysis to program design. Cengage Learning. 

**Editor:** Vanessa Coote (vacoot89)
