# Ruby: Unexpected Read-Only Behavior of Instance Variables

This example demonstrates a subtle issue in Ruby related to the seeming read-only nature of instance variables when accessed outside the class definition.  While instance variables are not inherently read-only,  directly assigning a new value to them outside their class's methods may not produce the expected effect.

## The Problem
The `bug.rb` file contains code that initializes a `MyClass` object and attempts to modify its instance variable `@value` directly. This does not change the object's state.  The issue is that instance variables are intended to be managed within the class's methods.  Direct external manipulation is not the intended way of updating the values.

## The Solution
The `bugSolution.rb` file provides the solution by implementing a `setValue` method. This gives controlled access and modification to the instance variable.