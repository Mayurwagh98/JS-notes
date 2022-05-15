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
  
  The`TAX_RATE`variable is only constant by convention -- there's nothing special in this program that prevents it from being changed. But if the city raises the sales   tax rate to 9%, we can still easily update our program by setting the`TAX_RATE`assigned value to 0.09 in one place, instead of finding many occurrences of the value   0.08 strewn throughout the program and updating all of them.
  
 9. The newest version of JavaScript at the time of this writing (commonly called "ES6") includes a new way to declare constants, by using const instead of var:
  ```
  // as of ES6:
  const TAX_RATE = 0.08;

  var amount = 99.99;

  ```
   constants also prevent accidentally changing value somewhere else after the initial setting. 
  
  ## Blocks
  
1. In code we often need to group a series of statements together, which we often call a block. In JavaScript, a block is defined by wrapping one or more statements inside a curly-brace pair { .. }.
  ```
  var amount = 99.99;

// a general block
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
  ```
  2. Typically, blocks are attached to some other control statement, such as an if statement or a loop. 
  For example:
  ```
  var amount = 99.99;

// is amount big enough?
if (amount > 10) {			// <-- block attached to `if`
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```
## Conditionals

```
var bank_balance = 302.13;
var amount = 99.99;

if (amount < bank_balance) {
	console.log( "I want to buy this phone!" );
}
  ```
  The if statement requires an expression in between the parentheses ( ) that can be treated as either true or false.
  
  In this program, we provided the expression `amount < bank_balance`, which indeed will either evaluate to true or false depending on the amount in the bank_balance variable.
                                                                      
Values that aren't already of an expected type are often coerced to that type. The if statement expects a `boolean`, but if you pass it something that's not already boolean, coercion will occur.

JavaScript defines a list of specific values that are considered `"falsy"` because when coerced to a boolean, they become false -- these include values like `0` and `""`. Any other value not on the `"falsy"` list is automatically `"truthy"` -- when coerced to a `boolean` they become `true`. 

`Truthy` values include things like `99.99` and `"free"`. 

## Loops
								      
1. Repeating a set of actions until a certain condition fails -- in other words, repeating only while the condition holds -- is the job of programming loops; loops can take different forms, but they all satisfy this basic behavior.
2. A loop includes the test condition as well as a block (typically as { .. }). Each time the loop block executes, that's called an `iteration`.
```
while (numOfCustomers > 0) {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
}

// versus:

do {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);
```
The only practical difference between these loops is whether the conditional is tested before the first iteration (while) or after the first iteration (do..while).

For a variety of historical reasons, programming languages almost always count things in a zero-based fashion, meaning starting with `0` instead of `1`.

## Functoins
	  
1. A function is generally a named section of code that can be "called" by name, and the code inside it will be run each time.
```
function printAmount() {
	console.log( amount.toFixed( 2 ) );
}

var amount = 99.99;

printAmount(); // "99.99"

amount = amount * 2;

printAmount(); // "199.98"
```
2. Functions can optionally take arguments (aka parameters) -- values you pass in. And they can also optionally return a value back.
```
function printAmount(amt) {
	console.log( amt.toFixed( 2 ) );
}

function formatAmount() {
	return "$" + amount.toFixed( 2 );
}

var amount = 99.99;

printAmount( amount * 2 );		// "199.98"

amount = formatAmount();
console.log( amount );			// "$99.99"
```
The function printAmount(..) takes a parameter that we call amt. The function formatAmount() returns a value. Of course, you can also combine those two techniques in the same function.

3. Functions are often used for code that you plan to call multiple times, but they can also be useful just to organize related bits of code into named collections, even if you only plan to call them once.
```
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}

var amount = 99.99;

amount = calculateFinalPurchaseAmount( amount );

console.log( amount.toFixed( 2 ) );		// "107.99"
```
Although calculateFinalPurchaseAmount(..) is only called once, organizing its behavior into a separate named function makes the code that uses its logic (the amount = calculateFinal... statement) cleaner. 

## Scope

1.  Scope is basically a collection of variables as well as the rules for how those variables are accessed by name.
2. Only code inside that function can access that function's scoped variables.
3. A variable name has to be unique within the same scope -- there can't be two different a variables sitting right next to each other. But the same variable name `a` could appear in different scopes.
```
function one() {
	// this `a` only belongs to the `one()` function
	var a = 1;
	console.log( a );
}

function two() {
	// this `a` only belongs to the `two()` function
	var a = 2;
	console.log( a );
}

one();		// 1
two();		// 2
```
4. Nested scope
```
function outer() {
	var a = 1;

	function inner() {
		var b = 2;

		// we can access both `a` and `b` here
		console.log( a + b );	// 3
	}

	inner();

	// we can only access `a` here
	console.log( a );			// 1
}

outer();
```
Lexical scope rules say that code in one scope can access variables of either that scope or any scope outside of it.

So, code inside the `inner()` function has access to both variables `a` and `b`, but code in `outer()` has access only to `a` -- it cannot access `b` because that variable is only inside `inner()`.
	  
## Practice Problem
	  
* Write a program to calculate the total price of your phone purchase. You will keep purchasing phones (hint: loop!) until you run out of money in your bank account. 
* You'll also buy accessories for each phone as long as your purchase amount is below your mental spending threshold.
* After you've calculated your purchase amount, add in the tax, then print out the calculated purchase amount, properly formatted.
* Finally, check the amount against your bank account balance to see if you can afford it or not.
* You should set up some constants for the "tax rate," "phone price," "accessory price," and "spending threshold," as well as a variable for your "bank account balance.""
* You should define functions for calculating the tax and for formatting the price with a "$" and rounding to two decimal places.
* Bonus Challenge: Try to incorporate input into this program, perhaps with the prompt(..) covered in "Input" earlier. You may prompt the user for their bank account balance, for example. Have fun and be creative!
	  
## Solution 
```
const SPENDING_THRESHOLD = 200;
const TAX_RATE = 0.08;
const PHONE_PRICE = 99.99;
const ACCESSORY_PRICE = 9.99;

var bank_balance = 303.91;
var amount = 0;

function calculateTax(amount) {
	return amount * TAX_RATE;
}

function formatAmount(amount) {
	return "$" + amount.toFixed( 2 );
}

// keep buying phones while you still have money
while (amount < bank_balance) {
	// buy a new phone!
	amount = amount + PHONE_PRICE;

	// can we afford the accessory?
	if (amount < SPENDING_THRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

// don't forget to pay the government, too
amount = amount + calculateTax( amount );

console.log(
	"Your purchase: " + formatAmount( amount )
);
// Your purchase: $334.76

// can you actually afford this purchase?
if (amount > bank_balance) {
	console.log(
		"You can't afford this purchase. :("
	);
}
// You can't afford this purchase. :(
```
	
	
