---
layout: post
title:      "JS Hoisting and Scope"
date:       2019-11-21 22:04:24 +0000
permalink:  js_hoisting_and_scope
---


Hoisting and scope in JS are both something I've had to wrestle around with. Talking about it is easier than predicting what a function will return. 
In javascript, hoisting is when and how we access variables in our program. Functions create new execution contexts which have two phases: the compile phase(first) and the execution phase(second). During the compile phase, declarations, *not assignments*, are being raised to the top of the current scope. Declarations are evaluated before the rest of our code gets run. A variable assignment without a declaration creates that variable in the global scope.
Try to guess the output: 
```
console.log(a)

// Some other code

var a = 5;
```
5? Wrong. Think we will get an error? Wrong. Undefined. Yes! During the complie phase, it reserves memory block for the variable. The variable isn't assigned any value so the value is 'undefined' by default. After this hoisting is done, the execution phase begins, on the first line it sees the variable 'a', which is undefined right now, then 'a' is reassigned the value of 5. This is just a small example but if you're struggling with this, heres a short video for review: [hoisting video](http://https://www.youtube.com/watch?v=AplVrrwY1TI&t=337s) or a some documentation outside of Learn if you're new to the concept of hoisting: [hoisting documentation](http://https://www.w3schools.com/js/js_hoisting.asp)

# Scope
Scope makes a little more sense to me than hoisting and here are a couple of things to remember. 
1.) *let* and *const* are block scoped, meaning those variables exist only within the corresponding block.
2.) *var* is function scoped, meaning whenever you declare a variable in a function with *var*, the variable is visible only within the function; you can't access it outside the function.
```
function foo(){
    var fruit ='apple';
    console.log('inside function: ',fruit);
}

foo();                    //inside function: apple
console.log(fruit);       //error: fruit is not defined 
```
3.) Inner scopes can access outer scopes' variables.
4.) You can go up the scope chain but not down.
Here is a helpful artictle to look over if you're struggling with scope: [scope article](http://https://medium.com/datadriveninvestor/still-confused-in-js-scopes-f7dae62c16ee)

