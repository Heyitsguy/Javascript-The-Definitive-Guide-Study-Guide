# Chapter 2 Lexical Structure #
* Lexical structure is basically the rules of a particular language
that you have to follow to write code that can be interpreted.

* Javascript is case sensitive while HTML is not, but since
there is overlap between javascript and XHTML, its important
to make XHTML case sensitive.

* Unicode escapes (`\u....`) can be used to display some Unicode
characters like vowels with tildes.

* `//` are single line comments, while `/* comment here */`
are used for multiline comments.

* A *literal* is a data value that appears directly in
a program. Examples of which are:
  * **String Literal** `"hi, im a string"`.
  * **Array Literals** `[Andy, Bill, 32, 20]` (Array Initializer)
  * **Object Literals** `{car:red, bike:maroon}`(Object initializer)
  * **Numbers**
  * **Booleans**

* Identifiers is a name for anything in Javascript, most commonly variables.
They can begin with:
  1.A letter
  2.an underscore
  3.Dollar sign

* Keep in mind that there are certain reserved words in
Javascript that have special meaning and cannot be used
as an identifier.

* Javascript treats line breaks as a semicolon when it
cannot parse the code.

* In general if a statement begins with `(,[,/,+, or -` there
  is a chance that it could be interpreted as a continuation
  of the statement before.

* Some programmers use a defensive semi colon before the
  statements that start with the characters listed above.

* Do not insert a line break before 'return, break or continue' keywords.

* `++ and --` should also be on the same line when postfixing them.
