# Intro to JavaScript | Part 2

## short URL to this repo [js2.sage.codes](https://github.com/sagecodes/intro-to-javascript-part2)

### FAQ: 

- WIFI: `Galvanize Guest` | Password is posted on the wall
- Bathrooms: Behind you down the hall to the left
- Kitchen outside back classroom door with Coffee & Tea!
- Snacks + water in back of room



## Setting up your computer


#### Please set up the following:

* A web browser to see what we're working on as others see it (Recommend Google Chrome: [chrome.google.com] (http://chrome.google.com))
* We will be using an online text editor for this workshop. You can sign up here: [https://repl.it/](https://repl.it/)


Well... that was easy! 


## What this workshop is

A super friendly introduction to JavaScript No previous experience expected! 

You can't learn EVERYTHING in ~2 hours. But you can learn enough to get excited and comfortable to keep working and learning on your own! 

- This course is for absolute beginners
- Ask Questions!
- Answer Questions!
- Help others when you can
- Its ok to get stuck, just ask for help!
- Be patient and nice

#### Part 1 we'll cover the basics of:

- Variables
- Strings
- Numbers
- Arrays
- Objects
- Conditionals
- Loops
- Put it all together to solve a classic computer science problem


#### Part 2 (Tonight) we'll cover the basics of:
 - Functions
 - Scopes
 - putting it all together again!


Again this will only be the basics and I hope it will serve as a great starting point for you!

We could probably spend more than 2 hours on each one of these concepts. So you'll absolutely want to dive deeper in each topic! 


## About me:

Hello I'm [Sage Elliott](https://www.linkedin.com/in/sageelliott/). I'm a Technology Evangelist here at Galvanize! For the past decade I've worked as a software and hardware engineer with Startups and Agencies in Seattle, WA and Melbourne, FL. I love making things with technology! I'm Currently learning more about computer vision and deep learning deep learning!

- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)

Reach out to me if interested in:

- breaking into the tech industry 
- learning resources
- meetup recommendations 
- learning more about Galvanize
- giving me suggestions for events!
- being friends


## About you!

Give a quick Intro!

- Whats your name?
- Whats your background?
- Why are you interested in JavaScript?


### FAQ Again for anyone who just walked in: 

- WIFI: `Galvanize Guest` | Password is posted on the wall
- Bathrooms: Behind you down the hall to the left
- Kitchen outside back classroom door with Coffee & Tea!
- Snacks + water in back of room
- Get to this repo by typing in URL: **js1.sage.codes**
## What is javaScript?



## JavaScript part1 Recap:

We'll do a quick refresher on some javaScript Basics that we need to know for this workshop. If you'd like to refresh more you can check out this [repo](https://github.com/sagecodes/Learn-to-code-javascript) or the resource section of near the bottom. 


<details>
  <summary>How do we make a variable</summary>
		use the keywod  var, let, or const

`let name = "Sage Elliott"`
</details>

<details>
  <summary>how do we print out something to the console?</summary>
        console.log() and we put what we want to print out in the ()
		
`console.log("I'm printed")`
</details>

<details>
  <summary>How do we make a string?</summary>
		Strings use quotation marks single or double

`"string"`

`'string2'`

`'string ${num3} with variable'` < - Uses back ticks not single quotes
</details>

<details>
  <summary>How do we make a number?</summary>
		just type a number with no quotation marks

`5`

`5+5`

`6 % 6`

`7 / 4`

</details>

<details>
  <summary>How do we make an array</summary>
		Square brackets []

`fave_food = ["taco", "Sushi", "fried chicken"]`
</details>

<details>
  <summary>How do we make an object</summary>
		curly brackets {}

`person = {"name":"Sage", "city":"Seattle"}`
</details>

<details>
  <summary>What is a comparison?</summary>
		when we compare two pieces of data. >,<, !=, ==, ===, 

`8 > 5`
</details>

<details>
  <summary>What is a conditional?</summary>
		How we often make actions based on a result of a comparision

```
var guess = 5;
var answer = 4;

if (guess == answer) {
    message = "You Win!";
} else if (guess < answer) {
    message = "Your guess is too low!";
} else if (guess > answer){
    message = "your guess is too high!";
} else {
	message = "I think you entered something wrong...";
};
```
</details>



<details>
  <summary>What is a for loop?</summary>
		We can loop thru a specific amount of times

```
for (var i=1; i <= 5; i++) {
    console.log(i);
}
```
</details>

<details>
  <summary>What is a while loop?</summary>
  we can loop until a condition is met

```
var i = 0;
while (i < 8) {
    console.log("I will crash your browser if you don't increment i")
    i++
}
```
</details>



## Functions

Reduce, Reuse, Recycle

Functions make it easy to reuse code. If you find yourself repeating code you may want to turn it into a function!

Example: these functions take in two arguments(a, b) and returns the value of them added together.



You'll see two common ways of creating a function called `Declaration` and `Expression`. We'll go into the differences with these types later when we get into scoping. Just remember there are two types!


Declaration:

```
function add(a, b) {  
  return a + b
}
add(2, 3)

```


Expression:

```
var sum = function(a, b) {  
  return a + b
}
sum(2, 3)

```


## Hoisting

We're going to just cover the basic of *hoisting* in javascript. This can help with understanding scopes. 



#### JavaScript Runtime

When you run javaScript there are essentially two steps that happen:

1. Variables are declared in memory 
2. Then the code is actually executed

below we will see an example of what we just talked about:

Due to the way javaScript runs(see above), it can cause some interesting things to happen! 

Hoisting basically happens at step one. When variables are declared in memory it will "hoist" them up to the top of their scopes. The effects variables declared with `var` and declarative functions. We'll see what this all means soon!

### Variable hoisting in action

`var`

What do you think will happen when we run this code? Lets run it in [repl](https://repl.it).


```
console.log(greeting)

var greeting = "hello"

console.log(greeting)

```
 
 It didn't throw an error! This is because of *hoisting*. The variable `greeting` gets declared in computer memory before we run the code. So the first `console.log()` will run just fine even though greeting does not have an assigned value to it.  
 
Visualizing it how it looks to the computer is something like this:
 
```
var greeting;

console.log(greeting);

greeting = "hello";

console.log(greeting);
```

Does it work with `let` and `const`?


`let`

```
console.log(greeting)

let greeting = "hello"

console.log(greeting)

```

`const`

```
console.log(greeting)

const greeting = "hello"

console.log(greeting)

```

`let` and `const` get treated differently.

To keep it simple you can remember that `let` and `const` cannot be accessed before they are declared. 

Technically they do get hoisted, but are caught is something called the *temporal dead zone*(a period between entering scope and being declared where they cannot be accessed). Read more about that [here](
https://stackoverflow.com/questions/31219420/are-variables-declared-with-let-or-const-not-hoisted-in-es6).


### Function Hoisting in action!

Similar to variables, functions also have get hoisted.

Lets see how it behaves with a Declaration function:

```
add(2, 3)
function add(a, b) {  
  return a + b
}
add(2, 3)

```
Declaration functions DO get hoisted.


Lets see how it behaves with a Expression functions:

We'll try with both `var` and `let`

```
sum(2, 3)
var sum = function(a, b) {  
  return a + b
}
sum(2, 3)

```

```
sum(2, 3)
let sum = function(a, b) {  
  return a + b
}
sum(2, 3)

```

Expression functions do NOT get hoisted. 

Because of hoisting can get confusing in a larger codebase [here is a long article suggesting to us Function Expression over declaration](https://javascriptweblog.wordpress.com/2010/07/06/function-declarations-vs-function-expressions/). 

<!--### using return 
console log vs return-->


<!--### Function Challenges
-->

## Scopes

### Scope

What is a Scope?

Put simply a scope in JavaScript defines what variables you have access to.

Two types of scopes exists:

1. Global Scope
2. Local Scopes

### Global Scope

What is global Scope?

Something with Global scope means you can access it anywhere in your code. Usually it will not be defined inside any function or curly brackets `{}`

##### Global Variables


```
var globalVariableOne = 'hello 1'
let globalVariableTwo = 'hello 2'
const globalVariableThree = 'hello 3'

function greeting() {
  console.log(globalVariableOne)
  console.log(globalVariableTwo)
  console.log(globalVariableThree)
}

greeting()

```

Above are examples of global variables. You will be able to access these variables anywhere in your code. including functions. *Note that we did not have to even pass these into our functions.*


Often best practice to not use global variables when possible. This will decreases the chance of developers changing variables by accident in other parts of the code or variable name collision. When you're working as a developer chances are your code base may be massive and you will not exactly know all the variables names.

##### name collision example:

Lets try these out in repl to see what happens

```
let globalvar = 'hello'
let globalvar = 'by'
```

```
var globalvar = 'hello'
var globalvar = 'by'
```

This is a good example why `let` is safer to use. It at least lets you know when you're re-declaring it. 


### Local Scope

Anything with a local scope can only be used in that part of the code. CANNOT be accessed everywhere in your code. There are two types of local scopes

1. Function scope
2. block scopes



### Function Scope

Functions scopes occur when you declare a variable inside of a function

this example created a local variable and calls it inside the function and outside of the function. What do you think will happen?

```
function greeting () {
  const say = 'hello'
  console.log(say)
}

greeting()
console.log(say)
```

Here is the same thing except the variable is global. What do you think will happen this time if we run this?

```
const say = 'hello'
function greeting () {
  console.log(say)
}

greeting()
console.log(say)
```


### Block Scope

Introduced in  ES6 (newer version of JavaScript)

We can use block level declaration with `let` and `cost`

```
{
  const say = 'hello'
  console.log(say)
}

console.log(say)
```

Again if we move the variable outside of the brackets this will make it global.

```
  const say = 'hello'
{
  console.log(say)
}
console.log(say)
```


### Scopes with functions 

We talked about hoisting in functions. When the function is declared it gets hoisted to the top of the scope its in. Which can be confusing when debugging / developing. Hence why most people say using the function expression is safer. Note that this is probably debatable and may depend on your team. They should probably all at least be consistent. 

##### Functions cannot access local variables from other functions

```
function one () {
  const oneVar = `Hello, this is oneVar`
}

function two () {
  one()
  console.log(oneVar)
}

two()
```

If you're new to programming this and wondering, well how would I get that value into another function to actually do something with it???

```
function one () {
  const oneVar = `Hello, this is oneVar`
  return oneVar
}

function two () {
  console.log(one()) 
}

two()
```



### Lexical scoping

Lexical scopes are nested scopes. Example a function inside of a function. the inner function has access to the outer functions variables, but the outer function cannot access the inner function variables.

Think of this as only having one way street from the inner function. It can move out and look at whats in the outer function. But the outer function cannot move into the inner function


Here we will try to print the inner variable from the outer function. Can you guess what will happen?

```
function outer () {
  const outerVar = `Hello, this is outerVar`

  function inner() {
    const innerVar = `Hello, this is innerVar`
    console.log(outerVar) 
  }

console.log(innerVar)
}

outer()

```

Here we will print the outer variable from the inner function. Based on what we talked about what do you think will happen?

```
function outer () {
  const outerVar = `Hello, this is outerVar`

  function inner() {
    const innerVar = `Hello, this is innerVar`
    console.log(outerVar) 
  }

inner()
}

outer()

```



## JavaScript Closures

What is a closure?

A closure a inner function with access to the outer (enclosing) function’s variables(aka scope chain).

Reiterating: When a function is created inside of another function thats called a closure. Often the inner function(closure) is used to return values. It has access to its outer scope variables and to global variables. 


```
let globalVar ="Hello, this is globalVar";
function outer () {
  const outerVar = `Hello, this is outerVar`;

  function inner() {
    const innerVar = `Hello, this is innerVar`;
    console.log(outerVar) 
    console.log(innerVar)
    console.log(globalVar)
  }

return inner()
}

outer()
```


##### Private variables

the variables inside the scope of a function that cannot be accessed outside of it are often called private variables. 

Returning the function with private variables similar to above allows you get access to the variables in parts of your code that you want. 


there is a lot more to learn about closures, this is just the basics. checkout these resources:

more about closure interview questions:
https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36

## Wrap up


### Lets Review:

<details>
  <summary>What is a Scope?</summary>
	a scope in JavaScript defines what variables you have access to
</details>

<details>
  <summary>What is a global scope?</summary>
	Something with global scope means you can access it anywhere in your code. 
</details>


<details>
  <summary>What is a local scope?</summary>
	a local scope can only be used in that part of the code. CANNOT be accessed everywhere in your code.
</details>


<details>
  <summary>What is hoisting?</summary>
  Hoisting basically happens at step one. When variables are declared in memory it will "hoist" them up to the top of their scopes. The effects variables declared with `var` and declarative functions.
</details>


<details>
  <summary>What type of function does not get hoisted?</summary>
	Expression functions
</details>


<details>
  <summary>What is the temporal dead zone?</summary>
	a period between entering scope and being declared where they cannot be accessed
</details>


<details>
  <summary>let and const are different from let because..?</summary>
	They do not get hoisted the same way as `var` they also throw name collision error. 
</details>


<details>
  <summary>What is special about const </summary>
		`const` value cannot be changed later in the code. It will throw an error if you try.
</details>

<details>
  <summary>What is a closure? </summary>
  A closure is inner function that access to the outer (enclosing) function’s variables(scope chain).
	
</details>

<details>
  <summary>What is lexical scoping?</summary>
  Lexical scopes are nested scopes. Example a function inside of a function. the inner function has access to the outer functions variables, but the outer function cannot access the inner function variables.
	
</details>

What type of function declaration is usually considered less confusing/safer?

Expression functions

<details>
  <summary>What are the two things that happen when JavaScript runs </summary>
  1. Variables are declared in memory 
	2. Then the code is actually executed
</details>



## Keep Learning!!!

### Resources:

- [Hack reactor Premium Prep](https://www.galvanize.com/gift-of-code?utm_medium=Seattle&utm_source=Meetup&utm_campaign=LearnToCode) FREE until 2/15 (usually $250)

- [Free Data Science Prep](https://www.galvanize.com/data-science-prep) - Galvanize

- [Free Software Engineering Prep](https://www.galvanize.com/web-development/prep) - Galvanize

- [https://github.com/getify/You-Dont-Know-JS](You-Dont-Know-JS)

- [You-Dont-Know-JS Scopes and Closures](https://github.com/getify/You-Dont-Know-JS/tree/master/scope%20%26%20closures)

- [hoisting interview questions](https://medium.freecodecamp.org/function-hoisting-hoisting-interview-questions-b6f91dbc2be8)

- [Work through problems here](https://repl.it/@SageElliott/scopesProblems)



## Upcoming Events!

We host so many events! check out our [calendar](https://www.galvanize.com/events)

Visit the [Learn to code Seattle](https://www.meetup.com/Learn-Code-Seattle/) meetup for all upcoming events.

[Python 101](https://www.eventbrite.com/e/javascript-mini-bootcamp-fundamentals-i-tickets-54952026992) - 2/21/19 6:30 - 8:30pm

[JavaScript Mini Bootcamp: Fundamentals I](https://www.eventbrite.com/e/javascript-mini-bootcamp-fundamentals-i-tickets-54952026992) - 2/23/19 10am - 4:30pm

[JavaScript 101](https://www.eventbrite.com/e/javascript-101-tickets-54952136319) - 2/27/19 6:30 - 8:30pm

## What is Galvanize?

#### Immersive Bootcamp


- [Software Engineer](https://www.galvanize.com/web-development) - 4/8/19 - 7/5/19
- [Data Science](https://www.galvanize.com/data-science) - 5/6/19 - 8/6/19


#### Part-Time Courses

- [Intro to Data Science](https://www.galvanize.com/part-time/intro-to-data-science) - 3/4/19 - 4/24/19

- [Digital Marketing](https://www.galvanize.com/part-time/digital-marketing) - 4/15/19 - 6/7/19

#### Co-working Space

[work in our building!](https://www.galvanize.com/entrepreneur)

#### We are a community

## Questions

Please feel free to reach out to me with any questions! Let me know what you're planning to do next and how I can help!


- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)

Questions about education at Galvanize SF email [learn@galvanize.com](mailto:learn@galvanize.com)


