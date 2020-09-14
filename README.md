# Class Notes - Fall 2020 - Intro to Programming
Contact: Mark Sherman <shermanm@emmanuel.edu>

# August 26,2020

Library: p5.js

JavaScript - language
	"interpreted" - a program reads the code, and does it
	
Calling a function

	functionName ( any parameter separated by commas )
	
	createCanvas(200, 100)
	background(210)
	
	madeUpFunction();
	
the parenthesis are what make it a function CALL

; semicolon ends an expression
	technically, in javascript, they SEPARATE expressions
	
Coordinate system:
	0,0 is in the upper-right corner
	x moves left
	y moves down
	x,y


# August 31, 2020

functions
	collections of code that can be called (run)
	a function must be DEFINED
	to call a function, name()
	pass parameters to the function in the parens goFunction(2, true)
	
IF if/else "conditional"

	if (condition) {
		body if true
	}
	
	if (condition) {
		body if true
	} else {
		body if false
	}
	
	a condition statement is an expression that resolves to true or false

VARIABLE

	name, contain (refer to) a value, declared before they can be used
	
	let x = 5;
	var y = 5;
	
	"let" declares a new variable
		"var" also declares a new varible
		"const" declares a new variable, but doesn't let you change the value
		
	= is the assignment operator
	
	if (x === 7){
		...;
	}
	
	Comparator Operators
		compare values
		return true or false - perfect for an if!
		
		> greater than
		< less than
		>= greater than or equal to
		<= less than or equal to
		=== is equal to
		== is equal to (but less good)
		!= not equal to
		
https://p5js.org/reference/

www.w3schools.com

Expression
	a piece of code
	let x = 5;
	expressions can be built out of other expressions
	
	I [want to] [go to] [somewhere]
	
	if (something that must resolve to true or false)
	
	can resolve to a value

[the p5 loop, setup and draw](Whiteboard[2]-01.png)

[flow for IF and IF/ELSE](Whiteboard[3]-01.png)
	
# September 2
<https://integrity.mit.edu/handbook/writing-code>

Comparators to compare values
"is the value of the variable x equal to 2?"  
	x === 2
"is temperature lower than 60?"
	temperature < 60
	
"is temperature lower than 60 or is it raining?"

	let temperature = 76;
	let raining = true;
	
	if (temperature < 60 ||	raining === true) {
		wearJacket();
	}

Logical Operators: 
	&& 	and		[thingA] && [thingB] ===> t/f
	|| 	or 		[thingA] || [thingB] ===> t/f
	
	!	not		![thing] ===> t/f (opposite of thing)
	
[Truth Tables for OR and AND](Whiteboard[4]-01.png)

Logical Primitives:
	true
	false

Expressions: 
	variable name: returns the value in that variable
	assignment operator: returns nothing (undefined)
	
	if ("red") {
		wearJacket();
	}

Truthiness
	any value can be interpreted as true or false
	'if' will always TRY to interpret what you give it as t/f
	
	undefined is falsy
	0 is falsy
	1 is truthy
	strings are truthy

Activity
Context:

	let x = 33;
	let y = 22;
	let z = 11;

	1.	true && false				false	
		
	2.	x === 33			true
		33 === 33
	
	3.	z != z		false
	
	4.	x === y + z			true
		33 === 22 + 11
		33 === 33
	
	5. 	x === y || x === y + z		true
		false   || true 
	
	6. 	x || y			true
		true || true
		
	
	7.	x != y || x != x	true
		true   || false
		
		x != y ---> true
		x != x ---> false
		
# September 7, 2020

Uncaught SyntaxError: missing ) after argument list	sketch.js:17:16

JavasScript treats single quotes and double quotes the same:
	
	let mySingleQuotedString = 'hello';
	let myDoubleQuotedString = "hello";
	
	both are valid!

	
# September 9, 2020

JavaScript Style Conventions: https://www.w3schools.com/js/js_conventions.asp
These are rules we'll follow for our style.

We spent the majority of class doing exercises in compound conditional statements. Whitboard shots are below.

JavaScript uses this same process to parse ALL of the language, not just conditionals!

Operator Precedence: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence
	
Examples (whiteboard, click to see image):

[`temp < 65 || raining === true`](Whiteboard-2020-09-03-1.png)

[`true && false || true && true`](Whiteboard-2020-09-03-2.png)

[`dogs <= 2 === false || bikes > 1`](Whiteboard-2020-09-03-3.png)

[`mouseX > width / 2 && mouseY < height / 2`](Whiteboard-2020-09-03-4.png)

# Monday 14 September 2020

* Starting Ch. 5 in the MAKE book

	* basics of p5
	* variables 
	* logic and conditionals 

* "Responsive"
* Falling Rock Parts 1 & 2
	* "Abstraction"

* What is abstraction? 
	* "concrete" as an opposite for "abstract"
	* abstract has no physical form
	* about conveying ideas and feelings more so than an actual image
	* ⬆️ mostly about art
	
* Abstraction in Computer Science
	* way to deal detail 
	* "abstract" as a verb - details can be "abstracted away"
	* "abstraction barrier" - a definitive junction between layers of abstraction
	* one abstraction barrier is p5 library. 
	* the Falling Rock assignment set uses an abstraction of the rock's altitude.
	
Made a ball bounce on the screen by talking about *state variables*

and how to use conditionals to manipulate them. 

```javascript
// State Variables
let ballX = 0;
let ballY = 0;
let moveRight = true;
let ballSize;

function setup() {
  createCanvas(400, 400);
  fill("purple");
  stroke("gold");
  strokeWeight(4);
  ballY = height / 2;
  ballSize = width / 4;
}

function draw() {
  print(ballX, ballY);
  background(150);
  ellipse(ballX, ballY, ballSize, ballSize);
  
  if(moveRight === true) {
    ballX = ballX + 1;
  } else {
    ballX = ballX - 1;
  }
  
  if(ballX >= width - ballSize / 2) {
    moveRight = false;
    print("FLIPPING THE SWITCH!");
  }
  
  if(ballX <= 0 + ballSize / 2) {
    moveRight = true;
    print("FLIPPING THE SWITCH!");
  }
}
```
