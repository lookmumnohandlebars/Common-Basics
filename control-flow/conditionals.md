# Conditionals

Conditionals are how to 'choose' which operations in code are executed (actually done).

The 'condition' of a conditional is a `boolean` that acts as a trigger 

Or, in a more behavioural language
> Given a condition is true, Then execute the following code.

## ⁉️ IF & ELSE Statements

### `IF`
The `if` statement takes a condition and executes the code in its scope (following the use of `if`) if the condition evaluates to the boolean value of `true`

<u>Python</u>:
```Python
if age >= 18:
    print('You are an adult! It's all downhill from here!')
```

<u>TypeScript</u>:
```TypeScript
if (age >= 18) {
    console.log("You are an adult! It's all downhill from here!");
}
```
### `IF` `ELSE`
The `else` statement, dependant on an `if` statement, defines a branch of code to execute if the condition given to an `if` statement is false.


<u>Python</u>:
```Python
# Given age is a number variable
if age >= 18:
    print('You are an adult! Everyhing is downhill from here!')
else:
    print('You are a kid! Make the most of your time!')
    
```

<u>TypeScript</u>:
```TypeScript
// given age is a number variable
if (age >= 18) {
    console.log("You are an adult! It's all downhill from here!");
} else {
    console.log("You are a kid! Make the most of your time!");
}
```

### (IF) ELSE IF (elif)
An informal operation, this involves chaining `if..else` statements to create multiple branches.

<u>Python</u>:
```Python
# Given age is a number variable
if age >= 18:
    print('You are an adult! Everyhing is downhill from here!')
elif age >= 13:
    print('You are a teenager! Enjoy your most awkward years!')
else:
    print('You are a child!')
    
```

<u>TypeScript</u>:
```TypeScript
// given age is a number variable
if (age >= 18) {
    console.log("You are an adult! It's all downhill from here!");
} else if (age >= 13) {
    console.log("You are a teenager! Enjoy your most awkward years!");
} else {
    console.log("You are a kid! Make the most of your time!");
}
```