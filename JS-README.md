# JS---notes

## Code
1. A program, often referred to as source code or just code, is a set of special instructions to tell the computer what tasks to perform. 
2. The rules for valid format and combinations of instructions is called a computer language, sometimes referred to as its syntax.

## Statements
1. In a computer language, a group of words, numbers, and operators that performs a specific task is a statement. In JavaScript, a statement might look as follows:
```
  a = b * 2;
```
2. The characters a and b are called variables which are like simple boxes you can store any of your stuff in. In programs, variables hold values (like the number 42) to be used by the program. Think of them as symbolic placeholders for the values themselves.
3. By contrast, the 2 is just a value itself, called a literal value, because it stands alone without being stored in a variable.
4. The = and * characters are operators -- they perform actions with the values and variables such as assignment and mathematic multiplication.
5. Most statements in JavaScript conclude with a semicolon (;) at the end.
6. The statement a = b * 2; tells the computer, roughly, to get the current value stored in the variable b, multiply that value by 2, then store the result back into another variable we call a.

## Expressions

1. Statements are made up of one or more expressions. An expression is any reference to a variable or value, or a set of variable(s) and value(s) combined with operators.
```
a = b * 2;
```
This statement has four expressions in it:

* 2 is a literal value expression
* b is a variable expression, which means to retrieve its current value
* b * 2 is an arithmetic expression, which means to do the multiplication
* a = b * 2 is an assignment expression, which means to assign the result of the b * 2 expression to the variable a.

2. A general expression that stands alone is also called an expression statement, such as the following:
```
b * 2;
```
3. This flavor of expression statement is not very common or useful, as generally it wouldn't have any effect on the running of the program -- it would retrieve the value of b and multiply it by 2, but then wouldn't do anything with that result.
4. A more common expression statement is a call expression statement, as the entire statement is the function call expression itself:
```alert( a );```
