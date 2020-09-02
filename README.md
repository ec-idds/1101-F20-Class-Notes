# Class Notes - Fall 2020 - Intro to Programming
Contact: Mark Sherman <shermanm@emmanuel.edu>

## August 26,2020

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


## August 31, 2020

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

[whiteboard 2](Whiteboard[2]-01.png)

[whiteboard 3](Whiteboard[3]-01.png)
	
## September 2
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
	
[whiteboard 4](Whiteboard[4]-01.png)

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
		

	
	
	
	
	
	
	
	 
