# JS-Notes

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
4. The '=' and '*' characters are operators -- they perform actions with the values and variables such as assignment and mathematic multiplication.
5. Most statements in JavaScript conclude with a semicolon (;) at the end.
6. The statement 'a = b * 2'; tells the computer, roughly, to get the current value stored in the variable b, multiply that value by 2, then store the result back into another variable we call a.

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

1. Go to browser click `<ctrl> + <shift> + <c>` or you can right click and select inspect, it will open the console.
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
  * Assignment: `=` as in a = 2.
  * Math: `+ (addition)`, `- (subtraction)`, `* (multiplication)`, and `/ (division)`.
  * Compound Assignment: `+=`, `-=`, `*=`, and `/=` are compound operators that combine a math operation with assignment, as in a += 2 (same as a = a + 2).
  * Increment/Decrement: `++ (increment)`, `-- (decrement)`, as in a++ (similar to a = a + 1).
  * Object Property Access: `.` as in console.log().
  * Equality: `== (loose-equals)`, `=== (strict-equals)`, `!= (loose not-equals)`, `!== (strict not-equals)`, as in a == b.
  * Comparison: `< (less than)`, `> (greater than)`, `<= (less than or loose-equals)`, `>= (greater than or loose-equals)`, as in a <= b.
  * Logical: `&& (and)`, `|| (or)`, as in a || b that selects either a or b.
<!--   4. For much more detail, and coverage of operators see the Mozilla Developer Network (MDN)'s "Expressions and Operators" 
    (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators). -->
 
  ## Values & Types

There are different representations for values are called *types* in programming terminology. JavaScript has built-in types for each of these so called *primitive* values:

* When you need to do math, you want a `number`.
* When you need to print a value on the screen, you need a `string` (one or more characters, words, sentences).
* When you need to make a decision in your program, you need a `boolean` (`true` or `false`).

Values that are included directly in the source code are called *literals*. `string` literals are surrounded by double quotes `"..."` or single quotes (`'...'`) -- the only difference is stylistic preference. `number` and `boolean` literals are just presented as is (i.e., `42`, `true`, etc.).

  Consider: 
```
  "I am a string";
  'I am also a string';

  42;

  true;
  false;
 ```
## Converting Between Types
  
  1. If you have a number but need to print it on the screen, you need to convert the value to a string, and in JavaScript this conversion is called "coercion." 
  2. Similarly, if someone enters a series of numeric characters into a form on an ecommerce page, that's a string, but if you need to then use that value to do math     operations, you need to coerce it to a number.

  JavaScript provides several different facilities for forcibly coercing between types. For example:
  ```
  var a = "42";
  var b = Number( a );

  console.log( a );	// "42"
  console.log( b );	// 42
  ```
  3. When comparing the string `"99.99"` to the number `99.99`, most people would agree they are equivalent. But they're not exactly the same. It's the same value in    two different representations, two different types.
  4. To help you out in these common situations, JavaScript will sometimes kick in and implicitly coerce values to the matching types.
  5. If you use the == loose equals operator to make the comparison `"99.99" == 99.99`, JavaScript will convert the left-hand side `"99.99"` to its number equivalent `99.99`. The comparison then becomes `99.99 == 99.99`, which is of course `true`.
  6. The common feeling is that implicit coercion is confusing and harms programs with unexpected bugs, and should thus be avoided. It's even sometimes called a flaw in the design of the language.
  
 ## Code Comments
  
  1.  These are bits of text in your program that are inserted purely to explain things to a human.
  2. The interpreter/compiler will always ignore these comments.
  3. Comments should explain why, not what. They can optionally explain how if that's particularly confusing.
  4. In JavaScript, there are two types of comments possible: a single-line comment and a multiline comment.
  ```
  // This is a single-line comment

  /* But this is
       a multiline
             comment.
                      */
  ```
  ## Variables
  
  1. Consider variable as a container in which you store a value.
  2. `Static typing` - In some programming languages, you declare a variable (container) to hold a specific type of value, such as `number` or `string`. `Static typing`, otherwise known as `type enforcement`.
  3. Dynamic typing - Other languages emphasize types for values instead of variables. `Weak typing`, otherwise known as `dynamic typing`.
  4. We declare a variable using the var statement
  ```
  var amount = 99.99;

  amount = amount * 2;

  console.log( amount );		// 199.98

  // convert `amount` to a string, and
  // add "$" on the beginning
  amount = "$" + String( amount );

  console.log( amount );		// "$199.98"
  ```
  The amount variable starts out holding the `number 99.99`, and then holds the number result of `amount * 2`, which is `199.98`.
  
  The first console.log(..) command has to implicitly `coerce` that `number` value to a `string`to print it out.
  
  Then the statement `amount = "$" + String(amount)` explicitly coerces the `199.98` value to a string and adds a `"$"` character to the beginning.
  
  At this point, `amount` now holds the `string` value `"$199.98"`, so the second `console.log(..)` statement doesn't need to do any coercion to print it out.
  
  5.Note that `amount` holds a running value that changes over the course of the program, illustrating the primary purpose of variables: managing program *state*.
  6. State - state is tracking the changes to values as your program runs.
  7. Another common usage of variables is for centralizing value setting. This is more typically called constants, when you declare a variable with a value and intend    for that value to not change throughout the program.
  8. You declare these constants, often at the top of a program, so that it's convenient for you to have one place to go to alter a value if you need to. 
  ```
  var TAX_RATE = 0.08;	// 8% sales tax

  var amount = 99.99;

  amount = amount * 2;

  amount = amount + (amount * TAX_RATE);

  console.log( amount );				// 215.9784
  console.log( amount.toFixed( 2 ) );	// "215.98"
  ```
  
 `toFixed(..)`lets us specify how many decimal places we'd like the number rounded to, and it produces the string as necessary.
  
  The`TAX_RATE`variable is only constant by convention -- there's nothing special in this program that prevents it from being changed. But if the city raises the sales tax rate to 9%, we can still easily update our program by setting the`TAX_RATE`assigned value to 0.09 in one place, instead of finding many occurrences of the value 0.08 strewn throughout the program and updating all of them.
  
  9. The newest version of JavaScript at the time of this writing (commonly called "ES6") includes a new way to declare constants, by using const instead of var:
  ```
  // as of ES6:
  const TAX_RATE = 0.08;

  var amount = 99.99;

  ```
   constants also prevent accidentally changing value somewhere else after the initial setting. 
  
  ## Blocks
  

