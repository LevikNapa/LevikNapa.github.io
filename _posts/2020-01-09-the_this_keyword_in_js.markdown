---
layout: post
title:      "The `this` keyword in JS"
date:       2020-01-10 04:16:27 +0000
permalink:  the_this_keyword_in_js
---


So the `this` keyword in javascript is a tricky one and what `this` is referring to changes based on where its being invoked. When being used inside a regular function, `this` will refer to the global object, which is not what you would usually want. However when invoked inside a method (a function that is a property of an object) `this ` will refer to the object that it is being invoked in, this is good. You will still run into a issue when defining an inner function (a callback function or simply a function inside a function) because the use of `this` inside the inner function won't be bound to the scope of the outer function. Oh shoot, so what do we do now? One fix would be to use the .bind method which will return a new function with the `this` value set to the context of the outer function. Or, another option would be to use arrow functions, the `this` keyword of an arrow function always belongs to the original context, even when its defined in an inner function.
