###Indenting and spacing

The preferred spacing style for Javascript is one tab set to two spaces.

Some members like have spaces on the inside of parantheses, some don't This is fine:

    if(boolean)

and this is also fine:

    if( boolean )


###Variable Declarations

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

####Variable Naming

Variables should be camel-cased and descriptively named.     

#####Booleans
Booleans should be written as verbCondition--where "verb" is ideally copulative. This is great:

    hasCorrectName = true;

this is even better:

    isCorrectlyNamed = true;

this is wrong:

    correctName = false;


#####Single-letter variable names

Single-letter variables are appropriate for and _only_ for instantiating for loops. Speaking of which...

###For Loops

A for loop should be written such that its conditional statement is a variable, not the property of a variable. This is done to increase processing speed. This variable should be declared in the for loops initialization, to cut down on use of the "var" keyword. This is correct:

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


####Variable Scoping

First, let's remember that JavaScript hoists variables. This means that this:


    x = 4;
    var x;

delivers the same result as:

    var x;
    x = 4;

Now, let's forget that JavaScript hoists variable declarations. Don't write any code that uses this, because it makes everything extremely unreadable.

For maximum clarity, declare all variables in a block at the top of their scope level. For instance:

    function returnNegative100(){
        var number1 = 5,
            number2 = 10,
            number3 = 20;

        return ( number1 - number2 ) * number3;
    }

is better than:

    var number1 = 5,
        number2 = 10,
        number3 = 20;
    function returnNegative100(){
        return( number1 - number2 ) * number3;
    }

Because no other function should have access to those variables (this is assuming of course that no other function should have access to those variables, which is really hard to prove in a short example). This protects you from having unexpectedly rewritten variables, and it keeps everything nice and readable because everything is moved as close to its actual use situation as possible.