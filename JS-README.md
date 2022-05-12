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
```
alert( a );
```
## Excuting a Program

1. Statements like a = b * 2 are helpful for developers when reading and writing, but are not actually in a form the computer can directly understand. So a special utility on the computer (either an interpreter or a compiler) is used to translate the code you write into commands a computer can understand.
2. For some computer languages, this translation of commands is typically done from top to bottom, line by line, every time the program is run, which is usually called interpreting the code.
3. For other languages, the translation is done ahead of time, called compiling the code, so when the program runs later, what's running is actually the already compiled computer instructions ready to go.
4. It's typically asserted that JavaScript is interpreted, because your JavaScript source code is processed each time it's run. But that's not entirely accurate. The JavaScript engine actually compiles the program on the fly and then immediately runs the compiled code.

## Try It Yourself

1. Go to browser click <ctrl> + <shift> + <c> or you can right click and select inspect, it will open the console.
2. To type multiple lines into the console at once, use <shift> + <enter> to move to the next new line. Once you hit <enter> by itself, the console will run everything you've just typed.
3. Let's get familiar with the process of running code in the console. First, I suggest opening up an empty tab in your browser. I prefer to do this by typing about:blank into the address bar. Then, make sure your developer console is open, as we just mentioned.
Now, type this code and see how it runs:
```
  a = 21;

  b = a * 2;

  console.log( b );
```
## Output

1. First, the log( b ) part is referred to as a function call. What's happening is we're handing the b variable to that function, which asks it to take the value of b and print it to the console.
2. Second, the console. part is an object reference where the log(..) function is located.

  ## Input
  
  1. There's an easier way to get input for simple learning and demonstration purposes. Use the prompt(..) function:
  ```
  age = prompt( "Please tell me your age:" );

  console.log( age );
  ```
  2. The message you pass to prompt(..) -- in this case, "Please tell me your age:" -- is printed into the popup.
  
  ## Operators
  
  1. The = equals operator is used for assignment -- we first calculate the value on the right-hand side (source value) of the = and then put it into the variable that we specify on the left-hand side (target variable).
  2. You should always declare the variable by name before you use it. But you only need to declare a variable once for each scope; it can be used as many times after that as needed.
  ```
  var a = 20;

a = a + 1;
a = a * 2;

console.log( a );	// 42
  ```
  3. Here are some of the most common operators in JavaScript:
  
  
