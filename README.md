# java-strings

Strings are immutable, which means they cannot be changed. 

String name = "Larry";
name = "John";

We create this name variable ans assign it the value Larry.
What java does is create that string variable called 'name' but the name variable isn't the String object itself, it is a reference to a String object in memory that it creates with the value of "Larry".  
But when you take this 'name' variable and assign it a new value, java doesn't actually modify the String object in memory. What it does is create a brand new String object in memory with the value "John" and changes this 'name' variable to point to that String object, and it no longer points to that "Larry" string. 

So when we say that Strings are immutable we are talking about the String object in memory. The String variables themselves can be changed to point to whatever String we want.

Reasons why Strings are immutable/not changable:
1. It enables java to save a ton of memory space. 

String name = "John";
String anotherName = "John";
.
.
.

When we create a multiple String variables and set them to the same literal string values, java creates another variables which points to the exact same string object that it already created before. It spares a lot of memory. 

When java creates a String object from a literal, it actually puts that string object in a String pool. And then every time another String literal is created, java will check that string pool to see if that value is already anywhere in there. 

If the string objects weren't immutable this wouldn't work at all. 
If you had both of these string variables ('name' and 'anotherName') pointing to the exact same object in memory, and if the variable was able to change the string object in memory ("John" --> "Larry") that would also change the value of the String being referenced 


