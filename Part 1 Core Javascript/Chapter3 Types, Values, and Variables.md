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
* Not a number (`NaN`) does not compared equal to any other value. (even itself). if  x!=x returns true then it is NaN.
* negative zero in JavaScript also acts weird and is equal to positive zero except when in the dividor. 
* be careful when doing financial calculations in JavaScript because binary floating point representation cannot represent .10, .01,.001 and so on. For example `.3 -.2 != .2-.1`
* You can avoid this problem by using whole integers and just taking out the decimal.
### Dates and Time ###
* `Date()` is a constructor for creating objects that represent date and time.
* When a new object of date is created, the object will have methods attached to it that can get the mins secs hours month and year.
## Text ##
* A *string* is an immutable ordered sequence of 16-bit values. 
* You can write a string literal by putting text in between `"" or ''`.
* You are allowed to break up a string literal across multiple lines but you have to include a `\` at the end of each line except for the last one.
* When you combine JavaScript strings and HTML strings in the same file, it is conventional to put text in between double quotes in one and between single quotes in the other. Example : `<button onclick = "alert('Thank you')">Click me </button>`
* The backslash lets you escape the next key you enter inside a string.

### Working With Strings ### 
* There are set number of methods that you can call that are attached to strings.
* Since strings are immutable in JavaScript, methods like replace and toUppercase actually return and create new strings.
* Strings can also be seen as read only arrays and you can access different indexes using square brackets `[]` instead of `charAt()`.
* Regex: Text between pairs of slashes constitutes a regular expression literal. The second slash can be followed by a letter that give different meanings.
* **Strings have methods** that take regular expression as arguments.


`var text = "testing: 123"`

`var pattern = /\d+/g`

`pattern.test(text) // => true`

* Some more examples are 
  * `text.search(pattern) // position of the first match`

  * `text.match(pattern) // array of all matches`

  * `text.replace(pattern, "#") // replaces digits with "#"`

  * `text.split(/\D+/) // split on non digits`

## Boolean values ##
* Boolean values represent truth or falsehood.
* If else statements rely on Booleans because different events happen depending on the Boolean.
* Any JavaScript value can be converted to a Boolean value. 
* The following converts to false
  * Undefined
  * Null
  * 0
  * -0
  * NaN
  * "" //Empty string
#Type Conversions#
## Object to Primitive Conversions ##
* All objects when converted to a boolean results in true.
* There are two methods used in order to convert objects into primitive values.
 1.  The toString() method.
 2. The valueOf() method.
* **Steps that javascript takes when trying to converting an object to a string.**
 1. Look for a toString() method. If one if found it is executed and the result is converted to a string if not already a string. 
 2. If 1 does not work then javascript looks for a valueOf() method and tries to call it. 
 3. If 1 and 2 both dont work then javascript throws a type error.
* **Steps that javascript takes when trying to convert an object into a number.** 
 1. Look for a valueOf() method. If one is found the value is returned and converted into a number.
 2. If 1 does not work then it checks the toString() method, converts and returns value.
 3. if 1 and 2 does not work then javascript will throw a type error.
* Lets look at the conversion of an array (which is considered a special object) converting into a number:
  * Runs valueOf(). Since valueOf() method returns the object instead of a primitive type, it will go to option 2 and run toString() method.
  * toString() method runs and converts the array to a string by joining the array.
  * The string is then converted into a number. 
  * If the array only had one digit in it, the array will be converted to that number. If the array is empty, the array will be converted to 0.
  * If the array has more than one index of numbers, it will convert to NaN.
* When you try to use ==, +, or != operators on objects it will try to use the valueOf() method first except for the date class. For the date class toString() method will try to be used.
* All other relational operators like < will follow the valueOf() method including dates. Only the operators listed in the previous bullet point will have an exception for the date class.
## Variable Declaration ##
* Before you can use a variable you must declare it. This can be done with the var, let, or const keyword.
* Often it is a good idea to initialize your variables when declaring like this: `var city = NYC`
