# Debugging

Every statment in a script lives in one of three execution contexts:

- global context. If variable is declared outside a function, it can be used anywhere because it has global scope. 
- function context. If variable is declared inside a function, it can only be used within that function.
- eval context

Each time a script enters a new execution context, there are two phases of activity:

1. Prepare

- the new scope is created
- variables, functions and arguments are created
- the value of the **this** keyword is determined
 
2. Execute

- now it can assign values to variables
- referance function and run their code
- execute statement

## Error objects

Error objects can help you find where your mistakes are and browsers have tools to help you read them.
Whenan Error object is created, it will contain the following properties:

- name
- message
- fileNumber
- lineNumber

There are seven types of built-in error objects in JS

- Error - Generic error
- SyntaxError - Syntax has not been followed
- ReferenceError - Tried to reference a variable that is not declared within scope
- TypeError - An unexpected date type that cannot be coerced
- RangeError - Numbers not in acceptable range
- URIError - enodeURI(), decodeURI, and similar methods used incorrectly
- EvalError - eval() functin used incorrectly

### How to deal with errors?

1. Debug to script to fix errors
2. Handle errors gracefully

Browser dev tools
For opening the console you need to:

- Chrome/Opera/IE - Press **F12**
- FireFox - Press **CTRL + Shift + K**
- Safari - **Alt +Cmd + C**

