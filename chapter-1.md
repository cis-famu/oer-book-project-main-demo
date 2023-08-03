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
