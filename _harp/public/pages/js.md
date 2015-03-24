##Table of Contents

* General Principles
* Syntax
    * Indenting
    * White space
        * Line Breaks
        * Parentheses
    * 
* Variables
    * Naming
        * Booleans
        * Single-letter variables
    * Declarations
* Functions
* For Loops
* jQuery

***

##General Principles

The goal of this style guide to promote clean, efficient, and perhaps most importantly, readable code. To achieve this goal, we seek to have consistently and logically formatted code.

##Syntax

###Indenting

Our preferred indent style for JavaScript is one tab set to two space.

###White space

Our preferred use of white space


####Line breaks

Discrete functions should be seperated by two line breaks, but code inside functions should be seperated by only one line break. This is right:

    function function1(){
        ...
        ...
        ...
    }

    function function2(){
        ...
        ...
        ...
    }

This is wrong:

    function function1(){
        ...

        ...

        ...
        ...
    }
    function function2(){
        ...
    }

####Parentheses

Our preferred style of spacing for statements inside of parentheses is to have a space between the parentheses and the statement inside.

This is correct:

    function( param1, param2 ){
        if( boolean ){
            ...
        }
    }

This is wrong: 

    function(param1){
        if(boolean){
            ...
        }
    }


###Logical operators

Our preferred style of handling logical statements with one boolean is to not include a

    if( isCorrect ){
        ...
    }

    if( !isCorrect ){
        ...
    }

This is wrong:

    if( isCorrect == true ){
        ...
    }

    if( isCorrect != true ){

    }


##Variables

###Naming

Variables should be camel-cased and descriptively named.   

###Declarations

When possible, variables should be instantiated with one use of the "var" keyword. Declare all variables required for a given scope level at once. Removing unnecessary uses of the word "var" is better for performance.

This is fine:

    var red,
        orange,
        green,
        blue;

This isnt:

    var red;
    var orange;
    var green;
    var blue;


###Booleans

Booleans should be written as "isCondition" or "hasProperty" so that they can be immediately recognized as booleans. These are fine:

    hasCorrectName = true;
    isCorrectlyNamed = true;

but this isn't:

    correctName = false;

###Single-letter variables

Single-letter variables should be avoided in any case except for instantiating a for loop.

##Loops

###For Loops

A for loop should be written such that its conditional statement is a variable, not the property of a variable. This is done to increase processing speed. This variable should be declared in the for loops initialization, to cut down on use of the "var" keyword and thereby saving processing power. This is correct:

    for( var i=0, x=array.length; i<x; i++ ){
      {...}
    }

while these are not:

    for( i=0; i<array.length; i++ ){
      {...}
    }

    var x = array.length;
    for( i=0; i<x; i++ ){
      {...}
    }

##jQuery

jQuery is a powerful library that makes performing DOM manipulation much easier. But like all powerful things, it must be checked.

###Objects

If a jQuery object is to be used multiple times, it should be declared as a variable, to cut down on both redundant objects and use of the $() function. Example:

    var header = $( '.header' ),
        headerHeight = header.height();

Some people like to preface variables that are jQuery objects with a $ (e.g. $header) and this is fine but not required.

###Selectors

Selectors should be as concise as possible
jQuery selectors should be as concise as possible. Each additional sele