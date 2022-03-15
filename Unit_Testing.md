# Unit Testing and Documentation

### What Unit Testing Isn’t

First, let’s clear up any misconceptions by talking about what doesn’t count.  Not every test you could conceivably write qualifies as a unit test.

If it we have written something that can fail when run on a machine without the “proper setup,” you haven’t written a unit test,Unit tests also don’t count as other sorts of tests,And, finally, unit tests don’t exercise multiple components of your system and how they act

### What Unit Testing Is

In C#, you can think of a unit as a method.  You thus write a unit test by writing something that tests a method.
That’s really it — all there is to it.  You’ll notice that I haven’t mentioned a few things that might pop into your head, such as test-driven development (TDD), unit test frameworks

### Unit Testing Tutorial

First off, we have a class called “CalculatorTests,” indicating that it will contain tests for the calculator class.
It gets an attribute called “TestClass” to tell Visual Studio’s default test runner and framework, MSTest, that this class contains unit tests.

## Unit Testing Best Practices:

1. Arrange, Act, Assert : To pull off this experiment, first, we arrange everything we need to run the experiment,you may need to seed an object with some variable values or call a particular constructor.

2. One Assert Per Test Method : Unit testing newbies commonly make a mistake of testing all of the things in one test method
 
3. Avoid Test Interdependence : Each test should handle its own setup and tear down. 

4. Keep It Short, Sweet, and Visible : Resist the impulse to abstract test setup (the “arrange”) to other classes, and especially resist the impulse to abstract it into a base class

5. Recognize Test Setup Pain as a Smell : When you create setup heavy tests, you create brittle tests.

6. Add Them to the Build : If your team has a continuous integration build, add your new unit test suite’s execution to the build.  If any tests fail, then the build fails.


