# Chapter 3 Types, Values, and Variables #

* Javascript has two types
  1. *Primitive* types
    * Numbers
    * Strings
    * Booleans
    * *null* and *undefined*
  2. *Object* types
    * Basically everything else you see is an object.

* Javascript objects are unordered collection of named values.

* Arrays and functions are considered special objects.

* Javascript preforms automatic garbage collection for memory management. This way programmers don't have to go back and delete objects later on to improve performance.

* Javascript is object oriented because instead of passing everything into defined functions we call on to methods for example.  
For array a, instead of `sort(a)` we call `a.sort`

* Everything is basically an object except for undefined and null since they have built in methods.

* Javascript will convert one type to another if it expects a certain type (Can be avoided with === ).

* Variables are untyped.

* Javascript uses lexical scoping, which means variables are scoped in functions or to the window.

## Numbers ##
* All numbers in Javascript are floating point values.

* Javascript supports base-10 integer literals and hexadecimals. Stray away from octal literals since not all implementations support them.

* When doing operations, anything that overflows will just have a value of infinity and -infinity.

* Underflow happens when the result is closer to 0 than the smallest digit supported. Javascript will just yield 0 in the case of underflow.
