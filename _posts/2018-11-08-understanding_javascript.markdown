---
layout: post
title:      "Understanding JavaScript"
date:       2018-11-08 20:27:14 -0500
permalink:  understanding_javascript
---

### Declaring Variables - var, let, const
* `var` - Declares a variable, optionally initializing it to a value.
* `let` - Declares a block-scoped, local variable, optionally initializing it to a value.
* `const` - Declares a block-scoped, read-only named constant.

`let` and `const` provide block scope variables.

### Scope - Local vs Global
A variable's scope is the context in which it exists. The scope specifies from where you can access a variable and whether or not you have access to it in that context. 

### **Global Scope**
Any variable declared outside of a function belongs to the global scope and is accessible from anywhere in your code. 

```const globalVariable = 'a value'```

Once declared, you can use that variable anywhere in your code.

```
const greeting = 'Hiya Harry!'

function sayGreeting() {
        console.log(greeting)
}
			
console.log(greeting) // 'Hiya Harry!'
sayGreeting() // 'Hiya Harry!'
``` 

The reason declaring variables in the global scope is not advised is that it exposes you to a chance of naming collisions. You'll receive errors when a name collision happens if you declared your variables with ```let``` or ```const```.

```
let theChosenOne = 'Harry Potter'
let theChosenOne = 'Neville Longbottom' // Error: 'theChosenOne' has already been declared
```

If you had declared the variables with `var`, the second would overwrite the first.

```
var theChosenOne = 'Harry Potter'
var theChosenOne = 'Neville Longbottom'
console.log(theChosenOne) // 'Neville Longbottom'
```


### **Local Scope**
Variables that are usable only in a specific part of your code are in a local scope. The two kinds of local scope are function and block.

**Function scope**

```
function castSpell() {
     const levitate = 'Wingardium Leviosa!'
		 console.log(levitate)
}

castSpell() // 'Wingardium Leviosa!'
console.log(levitate) // Error: levitate is not defined
```

In the above example, `levitate` is in the castSpell() scope. When you declare a variable in a function, you can only access it within the function.

**Block scope**

When you declare a variable with `const` or `let` within `{ } ` you can access this only within the curly brace.

```
{
const forget = 'Obliviate!'
console.log(forget) // Obliviate!
}
console.log(forget); // Error: forget is not defined
```

#### var vs. let & const

```
if (true) {
   var x = 8;
}
console.log(x); // 8
```

When using `let` this behavior changes

```
if (true) {
   let y = 8;
}
console.log(y); // Error: y is not defined
```

The first example returns 8 because the scope of x is the function within which it was declared and not the block/if statement.


### Hoisting

Hoisting has been defined as variable and function declarations being "moved to the top" of your code. What is actually happening is the variable and function declarations are put into memory during JavaScripts compile phase but stay exactly where you typed them in your code. 

```
function className(name) {
     console.log("I'm taking " + name + " this year.");
}

className("Potions"); // I'm taking Potions this year.
```

When we call the function before we write it the code still works the same. The variables can be initialized and used before they are declared.

```
className("Potions");

function className(name){
     console.log("I'm taking " + name + " this year.");
}
// I'm taking Potions this year.
```

### Context in JavaScript

While scope pertains to the visibility of variables, context in JavaScript refers to the object to which a function belongs. When you use the "this" keyword, it refers to the object to which the function belongs. "This" has different values depending on where it is used.

* In a method, **this** refers to the owner object.
* Alone, **this** refers to the global object.
* In a function, ** this** refers to the global object.
* In a function, in strict mode, **this** is undefined.
* In an event, ** this** refers to the element that received the event.
* Methods like call(), and apply() can refer **this** to any object.

```
let student = {
	firstName: "Ron",
	lastName: "Weasley",
	house: "Gryffindor",
	homeAddress: "The Burrow",
	studentInfo: function() {
		return this.firstName + " " + this.lastName + " in " + this.house + " house is from " + this.homeAddress + "." ;
    }
};

console.log(student.studentInfo()) // Ron Weasley in Gryffindor house is from The Burrow.
```

With the introduction of arrow functions in ES6, the `this` keyword is not used.

### Arrow Functions

Arrow Functions were introduced as a way for writing shorter functions and without defining its own `this` value. Before arrow functions, every new function defined its own `this` value.  the `this` value of an arrow function is the same as the `this` value of its enclosing object.

```
const professor = {
  firstName: 'Remus',
	lastName: 'Lupin',
  greet: function() {
    return () => {
      return 'Hi, I'm professor ${this.firstName} ${this.lastName}.';
    };
  }
};
professor.greet()();
// "Hi, I'm professor Remus Lupin."
```

The inner arrow function retains the context of the outer greet method. The outer greet method's context is professor and the inner function's context is now also professor.



> “Fortunately, JavaScript has some extraordinarily good parts. In JavaScript, there is a beautiful, elegant, highly expressive language that is buried under a steaming pile of good intentions and blunders.” 
― Douglas Crockford, JavaScript: The Good Parts











