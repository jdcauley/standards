####Indenting and spacing

The preferred spacing style for Javascript is one tab set to two spaces.

Some members like have spaces on the inside of parantheses, some don't. This practice (or lack thereof) should be neither frowned upon nor smiled at; but rather, looked at with a stern and stoic countenance befitting a team of adults who are capable of reading other people's code without splitting hairs.

This is fine:

    if(boolean)

and this is also fine:

    if( boolean )


The important thing is that your code is readable, and if a space (or lack thereof) is stopping your code from being readable, you probably have larger problems.

We're serious about the tab/spacing thing, though.

####Variable declarations

When possible, variables should be instantiated with one use of the "var" keyword. Declare all variables required for a given scope level at once. Removing unnecessary uses of the word "var" is better for performance.

We'll define "scope" later, but just remember that not everything should be globally-accessible.
####For Loops

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
