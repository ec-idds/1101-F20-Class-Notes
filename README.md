# Class Notes - Fall 2020 - Intro to Programming
Contact: Mark Sherman <shermanm@emmanuel.edu>

<!--ts-->
   * [Class Notes - Fall 2020 - Intro to Programming](#class-notes---fall-2020---intro-to-programming)
   * [August 26,2020](#august-262020)
      * [Coordinate system](#coordinate-system)
   * [August 31, 2020](#august-31-2020)
      * [functions](#functions)
      * [IF if/else "conditional"](#if-ifelse-conditional)
      * [VARIABLE](#variable)
      * [Expression](#expression)
   * [September 2](#september-2)
      * [Comparators to compare values](#comparators-to-compare-values)
      * [Logical Operators](#logical-operators)
   * [September 7, 2020](#september-7-2020)
   * [September 9, 2020](#september-9-2020)
      * [Operator Precedence](#operator-precedence)
      * [Logic Practice](#logic-practice)
   * [Monday 14 September 2020](#monday-14-september-2020)
      * [Starting Ch. 5 in the MAKE book](#starting-ch-5-in-the-make-book)
      * [What is abstraction?](#what-is-abstraction)
   * [Wednesday 16 September 2020](#wednesday-16-september-2020)
      * [Variable "Scope"](#variable-scope)
      * [keyCode](#keycode)
   * [Thursday 21 September 2020](#thursday-21-september-2020)
   * [Wednesday 23 September 2020](#wednesday-23-september-2020)
      * [Starting Chapter 6!](#starting-chapter-6)
   * [Monday 28 September](#monday-28-september)
   * [Wednesday 30 September](#wednesday-30-september)
   * [Monday 05 October](#monday-05-october)
      * [NESTED LOOPS](#nested-loops)
   * [Wednesday 7 October](#wednesday-7-october)
   * [Monday 12 October](#monday-12-october)
      * [Arrays](#arrays)
   * [Wednesday 14 October](#wednesday-14-october)
      * [Looping over Arrays](#looping-over-arrays)
      * [Understanding nested function calls:](#understanding-nested-function-calls)
      * [Odd and Even](#odd-and-even)

<!-- Added by: shermanm, at: Wed Oct 14 16:46:32 EDT 2020 -->

<!--te-->

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
	
## Coordinate system
	0,0 is in the upper-right corner
	x moves left
	y moves down
	x,y


# August 31, 2020

## functions
	collections of code that can be called (run)
	a function must be DEFINED
	to call a function, name()
	pass parameters to the function in the parens goFunction(2, true)
	
## IF if/else "conditional"

	if (condition) {
		body if true
	}
	
	if (condition) {
		body if true
	} else {
		body if false
	}
	
	a condition statement is an expression that resolves to true or false

## VARIABLE

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

## Expression
	a piece of code
	let x = 5;
	expressions can be built out of other expressions
	
	I [want to] [go to] [somewhere]
	
	if (something that must resolve to true or false)
	
	can resolve to a value

[the p5 loop, setup and draw](2020-08-31/Whiteboard02.png)

[flow for IF and IF/ELSE](2020-08-31/Whiteboard03.png)
	
# September 2
<https://integrity.mit.edu/handbook/writing-code>

## Comparators to compare values
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

## Logical Operators
	&& 	and		[thingA] && [thingB] ===> t/f
	|| 	or 		[thingA] || [thingB] ===> t/f
	
	!	not		![thing] ===> t/f (opposite of thing)
	
[Truth Tables for OR and AND](2020-09-02/Whiteboard04.png)

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

We spent the majority of class doing exercises in compound conditional statements. Whiteboard shots are below.

JavaScript uses this same process to parse ALL of the language, not just conditionals!

## Operator Precedence

Operator Precedence: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence
	
## Logic Practice

Examples (whiteboard, click to see image):

[`temp < 65 || raining === true`](2020-09-09/Whiteboard-2020-09-03-1.png)

[`true && false || true && true`](2020-09-09/Whiteboard-2020-09-03-2.png)

[`dogs <= 2 === false || bikes > 1`](2020-09-09/Whiteboard-2020-09-03-3.png)

[`mouseX > width / 2 && mouseY < height / 2`](2020-09-09/Whiteboard-2020-09-03-4.png)

# Monday 14 September 2020

## Starting Ch. 5 in the MAKE book

	* basics of p5
	* variables 
	* logic and conditionals 

* "Responsive"
* Falling Rock Parts 1 & 2
	* "Abstraction"

## What is abstraction? 
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

// is not a state variable, in that we don't use it to maintain the state of the program
// but it is still a variable that's representing a value with a name for more clarity. 
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

# Wednesday 16 September 2020

##  Variable "Scope" 
* Scope is where a variable is visible/usable
* Global - variables are created outside of any functions or other code blocks
* Local - variables are created in, and only accessible in, a particular function
	* only exist in the body they're created in
	* only exist DURING THE CALL they're created in
	* ==> these variables don't remeber anything between function calls

I'm skipping Example 5.7 you can do that on your own

Some shorthand operators:

    x += n
    x = x + n
  
    x++
    x += 1
    x = x + 1
 
    x-- 
    x -= 1
    x = x - 1

We found a fun logic error, where this code had a bug:

    if (keyIsPressed && key == 'c' || key == 'a') {
      fill('red');
    } else {
      fill('blue');
    }
	
the solution was to add grouping parenthesis around the latter two expressions to make sure the OR was evaluated as one unit,  prior to being AND'ed with keyIsPressed. [Here is the whiteboard about that](2020-09-16/Whiteboard-2020-09-16.png)

## keyCode

Then we introduced `keyCode` which is different than `key` but serves the same purpose to report keyboard info. `keyCode` gives you access to keys that don't have face characters, like the arrow keys, shown below. Make sure you look at the [reference page for keyCode](https://p5js.org/reference/#/p5/keyCode) when you go to use it!

Here's the code we ended up with:

```javascript
let x;
let y;

function setup() {
  createCanvas(400, 400);
  x = width / 2;
  y = height / 2;
}

function draw() {
  background(180);
  text('Press Space to Change Color');
  
  if(keyIsPressed && keyCode == LEFT_ARROW) {
    x--;
  }
  
  if(keyIsPressed && keyCode == RIGHT_ARROW) {
    x++;
  }
  
  if (keyIsPressed && (key == 'c' || key == ' ')) {
    fill('red');
  } else {
    fill('blue');
  }

  ellipse (x, y, 200);
  
  if (keyIsPressed) {
    text(key, 300, 300);
  }
}
```
I recommend you play with this, possibly with editor.p5js.org. Try to add the up and down arrows!

# Thursday 21 September 2020

# Wednesday 23 September 2020

## Starting Chapter 6!

THINGS DON'T GET WRITTEN LINEARLY

	/* Example 6-7 */

	var angle = 0.2;
	var angleDirection = 1;
	var speed = 0.005;

	function setup() {
	  createCanvas(120, 120);
	}

	function draw() {
	  background(204);
  
	  stroke('black');
	  translate(20, 25);
	  rotate(angle);
	  drawAxis();
	  strokeWeight(12);
	  line(0, 0, 40, 0);
  
	  translate(40, 0);
	  stroke('red');
	  rotate(angle * 2.0);
	  drawAxis();
	  strokeWeight(6);
	  line(0, 0, 30, 0);
  
	  translate(30, 0);
	  stroke('blue');
	  rotate(angle * 2.5);
	  drawAxis();
	  strokeWeight(3);
	  line(0, 0, 20, 0);
  
	  angle += speed * angleDirection;
	  if ((angle > QUARTER_PI) || (angle < 0)) {
	    angleDirection *= -1;
	  }
	}

	function drawAxis() {
	  strokeWeight(0.5);
	  line(-width, 0, width, 0);
	  line(0, -height, 0, height);
	}

# Monday 28 September
Here's a bunch of whiteboards.

[Whiteboard 1](2020-09-28/Whiteboard1.png)

[Whiteboard 2](2020-09-28/Whiteboard2.png)

[Whiteboard 3](2020-09-28/Whiteboard3.png)

[Whiteboard 4](2020-09-28/Whiteboard4.png)

[Whiteboard 5](2020-09-28/Whiteboard5.png)

[Whiteboard 6](2020-09-28/Whiteboard6.png)

# Wednesday 30 September
We worked in groups on Loop Exercises. Here it is, all cleaned up. 

[C2 Loop Exercises.pdf](C2_Loop_Exercises.pdf)

# Monday 05 October
Reviewed homeworks:

- Falling Rock (pts 1, 2, and bonus)
- Emoji Wars

Whiteboard:

[Falling Rock Jet Pack 1](2020-10-05/Whiteboard1.png)

[Falling Rock Jet Pack 2](2020-10-05/Whiteboard3.png)

[with the offset for Emoji Wars](2020-10-05/Whiteboard4.png)


Started Task 4 from the above Loop Exercises. Here's the new trick (which we'll expand on Wednesday): 

## NESTED LOOPS

```javascript
for(let j = 0; j < 3; j++){
  for(let i = 0; i < 3; i++){
    ellipse(i * 30, j * 30, 20);
  }
}
```

# Wednesday 7 October

More work on NESTED LOOPS. We hand-executed a single loop program to draw a row of circles. Then we created a double-loop, a *nested loop*, and executed that by hand. 

Some tricks to nested loops:

- There is an *inner* and *outer* loop. The Outer loop runs first, and the inner loop is inside the body of the outer loop.

- When the inner loop starts, it runs to completion before we return to the outer loop

- When the inner loop is completely done, meaning it got "false" for its conditional check, we then proceed with the rest of the outer loop's body. If there isn't any more body, we jump back into the outer loop's flow chart at the end of the body. 

- The outer loop increments its counter, checks its conditional, and if the conditional is still true, goes into its body, just like usual. 

- When we enter the body of the outer loop a second (or subsequent) time, the inner loop is like a NEW loop to the computer, and it starts over with the initialization/setup expression, which usually sets its counter back to zero. Then it runs in its entirety again. 

[Tracing the Single loop](2020-10-07/Whiteboard1.png)

[Tracing the Double loop](2020-10-07/Whiteboard2.png)

[Trying to make the middle circle not print (doesn't quite work)](2020-10-07/Whiteboard3.png)

```javascript
function setup() {
  createCanvas(300, 300);
}

function draw() {
  background(220);
  translate(50, 50); // just so we can see it all on the canvas

  for(let j = 0; j < 3; j++) {
    for(let i = 0; i < 3; i++) {
      ellipse(i * 30, j * 30, 20);
    }
  }
}
```

# Monday 12 October 

Reviewed the Falling Rock jetpacks, Emoji Wars, and Pinwheels. 

## Arrays

The most critical pieces are on these two slides:

[Introduction to Arrays](2020-10-12/Whiteboard1.png)

[Cool things about arrays](2020-10-12/Whiteboard2.png)

We started trying these ideas with the following example, that rotates colors whenever the mouse is clicked. (I tweaked it a little bit after class to fix a bug)

```javascript
function setup() {
  createCanvas(400, 400);
}

let colorIndex = 0;
let myColors = ['red', 'green', 'blue', 'yellow', 'pink'];

function draw() {
  background(220);
  
  fill(myColors[colorIndex]);
  ellipse(width / 2, height / 2, width, height);
}

function mouseClicked() {
  colorIndex++;
  if (colorIndex >= myColors.length) {
    colorIndex = 0;
  }
  print(colorIndex)
}
```

# Wednesday 14 October

p5 reference, as you know, is https://p5js.org/reference/

for the language itself, javascript reference is here https://www.w3schools.com/jsref/

## Looping over Arrays

[looping over an array](2020-10-14/Screenshot1.png)

```javascript
let myArray = ['red', 'green', 'blue', 'pink', 'yellow'];

function setup() {
  createCanvas(800, 400);
  noStroke();
  
  for(let i = 0; i < myArray.length; i++) {    
    fill(myArray[i]);
    rect(100 * i, 100, 75, 75);
  }
}
```

[arrays are mutable](2020-10-14/Whiteboard01.png)

[arrays are expandable](2020-10-14/Whiteboard02.png)

```javascript
let myArray = [];

function setup() {
  createCanvas(800, 400);
  noStroke();
  
  for(let i = 0; i < 100; i++){
    myArray.push(i + 1);
  }
  
  for(let i = 0; i < myArray.length; i++){
    if(myArray[i] % 2 !== 0){
      print(myArray[i]);
    }
  }
}
```

## Understanding nested function calls:

* I accidentally had all of your faces in front of the screenshot, so I had to re-do it
* [The first screenshot](2020-10-14/Screenshot2.png)
* [The Re-Do](2020-10-14/Whiteboard03.png)

## Odd and Even

[Introducing Modulus](2020-10-14/Whiteboard04.png)

[Even Detector Expression](2020-10-14/Whiteboard05.png)
