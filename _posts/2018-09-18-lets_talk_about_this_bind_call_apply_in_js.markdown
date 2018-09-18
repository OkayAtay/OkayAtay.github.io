---
layout: post
title:      "Let's Talk about 'This' : bind(), call(), apply() in JS"
date:       2018-09-18 11:48:38 +0000
permalink:  lets_talk_about_this_bind_call_apply_in_js
---


The concept of 'this' may be something that you gloss over as you navigate the Learn.co curriculum. You may be coming off a rails a hotshot, more than comfortable with 'self' and positive that it's pretty much the same thing. And that is where I come in, to set you right. 

'This' in JS is all about context and allows us to refer to the object your function is bound to:

For example

```
var puppy = {
 firstName: "Fluffy",
 lastName: "McCuteFace",
 function bark(){
     console.log(this.firstName + " " + this.lastName + "says Ruff");
}
```

In the above, super realistic example Fluffy McCuteFace is easily referred to as 'this' and our code knows exactly to whom I'm referring. 

So what happens when we want to set the value of this -- that's when we use bind(), call(), and apply(). 

## When to call()/apply()
### The easier way to think about is that call()/apply() methods are for now and ...

The best way to conceptualize this is an example where there could be multiple objects that 'this' could refer to -- if you're a grammar buff, it's almost like thinking of using a pronoun when you can not directly reference the noun. 

e.g. Jerry and Sam meandered together along the path and arrived at his house.

Whose house is it?!?! Unclear.

Call/Apply allows us to explicitly refer to the object that we'd like to act on: 

```

var puppy = {
 firstName: "Fluffy",
 lastName: "McCuteFace",
}

 function bark(){
     console.log(this.firstName + " " + this.lastName + "says Ruff");
}

var dog = {
    firstName: "Scooby",
		lastName: "Doo",
}

```

How do we make this mystery solving dog bark? Like this:

```
bark.apply(dog) OR bark.call(dog) // both return "Scooby Doo says Ruff"
```

Either of the above does the trick.
## When to bind()
### ...bind() methods are for later. 

Using the same examples from above, say I have multiple variables within a function and want to retain the value of a specific variable. Then I use bind, so that I can use that variable for later. 

```

var dog = {
    firstName: "Scooby",
		lastName: "Doo",
}


 function mysterysolve(partner){ 
     console.log(${partner} + "solved a mystery with" + ${this.firstName})
}

let newMystery = mysterysolve.bind(dog)

newMystery("Fluffy")

```

The resulting code is "**Fluffy** solved a mystery with **Scooby**" 

*What a dynamic duo.*


