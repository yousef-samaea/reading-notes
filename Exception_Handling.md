# ** How to debug for absolute beginners **

it’s much easier and efficient to use a debugging tool when the code faile,Debugging means to run your code step by step in a debugging tool like Visual Studio, to find the exact point where you made a programming mistake,then i can  understand what corrections i need to make in to my code, so i can continue running the program.

## steps to start debugging:

1. Clarify the problem by asking yourself the right questions

2.Examine your assumptions :
***Here are a few questions to ask yourself to challenge your assumptions.***

Are you using the right API (that is, the right object, function, method, or property)? An API that you're using might not do what you think it does. (After you examine the API call in the debugger, fixing it may require a trip to the documentation to help identify the correct API.)

Are you using an API correctly? Maybe you used the right API but didn't use it in the right way.

Does your code contain any typos? Some typos, like a simple misspelling of a variable name, can be difficult to see, especially when working with languages that don’t require variables to be declared before they’re used.

Did you make a change to your code and assume it is unrelated to the problem that you're seeing?

Did you expect an object or variable to contain a certain value (or a certain type of value) that's different from what really happened?

Do you know the intent of the code? It is often more difficult to debug someone else's code. If it's not your code, it's possible you might need to spend time learning exactly what the code does before you can debug it effectively.

3.Step through your code in debugging mode to find where the problem occurred

4.Create a sample app (with some bugs)

5.Run the app

6.Debug the app

## Summary:
When you find the region of code with the problem, use the debugger to investigate. To find the cause of a problem, inspect the problem code while running your app in the debugger:

Inspect variables and check whether they contain the type of values that they should contain. If you find a bad value, find out where the bad value was set (to find where the value was set, you might need to either restart the debugger, look at the call stack, or both).

Check whether your application is executing the code that you expect. (For example, in the sample application, we expected the code for the switch statement to set the galaxy type to Irregular, but the app skipped the code due to the typo.).

# How to use the try/catch block to catch exceptions;

Place any code statements that might raise or throw an exception in a try block, and place statements used to handle the exception or exceptions in one or more catch blocks below the try block. Each catch block includes the exception type and can contain additional statements needed to handle that exception type.

# Statement keywords (C# Reference):

Category :	C# keywords
Selection statements  :	if, switch
Iteration statements  :	do, for, foreach, while
Jump statements       :	break, continue, goto, return
Exception handling    : statements	throw, try-catch, try-finally, try-catch-finally
Checked and unchecked :	checked, unchecked
fixed statement       : fixed 
lock statement        : lock  
yield statement       : yield

# Therac-25

The Therac-25 was a computer-controlled radiation therapy machine produced by Atomic Energy of Canada Limited (AECL) in 1982 after the Therac-6 and Therac-20 units (the earlier units had been produced in partnership with Compagnie Générale Radiographique (CGR) of France).

It was involved in at least six accidents between 1985 and 1987, in which patients were given massive overdoses of radiation.[1]: 425  Because of concurrent programming errors (also known as race conditions), it sometimes gave its patients radiation doses that were hundreds of times greater than normal, resulting in death or serious injury.These accidents highlighted the dangers of software control of safety-critical systems, and they have become a standard case study in health informatics, software engineering, and computer ethics. Additionally, the overconfidence of the engineers: 428  and lack of proper due diligence to resolve reported software bugs are highlighted as an extreme case where the engineers' overconfidence in their initial work and failure to believe the end users' claims caused drastic repercussions.











