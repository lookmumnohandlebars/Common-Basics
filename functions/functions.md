# Functions

## ❓ What is a Function?

- **Self-contained repeatable task**: A function, in code terms, is a self-contained module of code that can be (re-)used many times throughout a program.
- **Abstraction**: Functions provide an abstraction (1 line of code to represent many more operations) that makes programs more readable and, in general, of better quality.

### Function Definition & Execution

- **Function Definition**: The definition defines the code that is executed on each function call
- **Function Execution/Call**: Also known as function invocation, this is when the code defined in the definition actually executes in the program.

### Basic examples

_Let's imagine a function that adds 5 to an input number._

#### Mathematical

In mathematical notation that function would be:

```LaTex
f(x) = x + 5
```

This can be read as "Given an input of `x`, the function should produce a result equivalent to `x + 5`".
When that function is used (called) then the output should reflect that (the mathematical equivalent of a function call):

```LaTex
f(10) = 15
```

#### TypeScript

In Javascript / TypeScript notation, that function would look similar but with a more bespoke syntax:

```TypeScript
function AddFive(x: number) : number {
    return x + 5;
}
```

This can then be read as "Given a number input `x` into the function of `Add5`, the function should output, or return, `x + 5`, which is always number".
The function execution, or call, then would look like this:

```TypeScript
let value = AddFive(5);
```

The return value of `10` is assigned to the variable `value`

#### Python

In Python notation (which uses indentation to define the scope) the same function would looke like

```python
def AddFive(x):
    return x + 5;
```

This can then be read as "Given an input `x` into the <u>def</u>ined function of `Add5`, the function should output, or return, `x + 5`".

> As Python is a dynamically, or weak, typed programming language, `x` here does not have to be a number, and therefore the output of the function is also dynamic and may not return a number

---

## 🤔 Function Concepts

Programming languages share the concept of a function, and while the syntax may vary, the underlying concepts are most often shared.

### 🖊 Function Signatures

When a function is declared, a function signature is defined, which declares the inputs and oututs for the function. The signature defines how the function should be called, or invoked.

#### Parameters

Function parameters are the definition of variables that are allowed to be input into a function.

- **Required Parameters**: By default most languages require all parameters to be input as arguments
- **Optional & Default Parameters**: Most languages allow paramaters to be defaulted in the event they are not passed in to functions
  > In the AddFive examples earlier, `x` would be the only parameter in all examples.

```TypeScript
function AddFive(x: number = 5) : number {
  return x + 5;
}
AddFive(); // x is defaulted to 5, the output is 10
```

#### Arguments

Function arguments are the values given at call-time to the parameters.

- **Copied into scope**: Arguments are copied into the function scope to be used for the code execution.

```TypeScript
let name = "Malcolm Reynolds"
let age = 34
let catchphrase = "I swear by my pretty floral bonnet I will end you"
CreateCharacter(name, age, catchphrase) // variables passed in as arguments
```

#### Return Type & Value

In the function definition, the return type (& value) is the expected return value (or output) of the function.

Example in Typescript:

```TypeScript
function Add5(val: number) : number {
  return val + 5;
}
```

The return type above, given as `number`, tells the compiler that the output will always be of type `number`. This indicates a contract, meaning any assigned

### 🔭 Function Scope

Functions have their own scope - i.e. boundary of operation. The code that is executed happens within the boundary of the function itself.

- Arguments are usually copied as parameters: The arguments

> If the argument is a reference type.

- Closure: Functions have access to variables in the containing scope, but the containing scope does not have access to function (mostly)

```Typescript
function Add5NTimes(val: number, nTimes: number) : number {
  for (let i = 0; i < nTimes; i++) {
    Add5(); // call Add5 nTimes
  }

  function Add5() { // exists only within the scope of Add5NTimes
    let message = "adding 5"; // message is only accessible within Add5
    val += 5; // val is accessible from the upper scope.
  }
  
  return val;
}

```

#### Functions within functions

Again, most languages offer a way of

### 💾 Function Overloads

### 📦 Functions as Data Types

---

### A brief introduction to functional languages
