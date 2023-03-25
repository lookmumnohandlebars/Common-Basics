# Variables

## ❓What is a variable?
- **Symbolic representation of an object**: A variable is simply a representation of an object. In computer programming, an object is just an item of data. 
    - For example you can assign somebody's name to a variable called `name` as a sequence of characters, or somebody's age to a variable called `age`.

```python
# python
name = 'Alexander Jaye'
age = 26
```

- **How data is stored and represented within the memory of a program**: Any type of data (or reference to that data) can generally be assigned to a variable.

## 🟰 Value Assignment
- **Variable Declaration**: The first time a variable is created, or created and assigned to, it usually called a variable declaration - a variable has been declared and exists in memory.

```Typescript
// Typescript
let x; // declaration with no initialisation
let y = 4; // declaration with initialisation
```

- **`=` for assignment**: In most contexts, the mathematical equality symbol (`=`) in programming actually performs an assignment, assigning a value to a variable. (e.g. many languages use `==` to mean equality)
- **Valueless assignment**: It is possible, in most languages, for a variable to represent a lack of value, by being assigned a value that represents nothing.

```python
# python
age = None
```

## 🗝️ Types of variables
- **Standard**: Variables, by their name, are subject to change. So the value of a variable is not (necessarily) continuous and can change.
```python
# python
age = 23
age = 24
```
- **Constants**: Constants are a type of variable that cannot change after initial assignment. 

```typescript
// TypeScript
const PI = 3.14;
// PI = 42 will cause an error
```

## 💪 Strong vs. Weak Typing
In programming languages there is a concept of strong and weak typing, which refers to whether you can change the type of a variable between assignments
> In essence, this is whether or not a variable has (or must have) a defined data type that it must always represent.

- **Strong**: A stronly typed variable (or language if enforced) or has a fixed, defined data type. Any subsequent assignment
```TypeScript
// TypeScript
let age: number = 24;
age = 'Alexander Jaye' // would cause an error as age must be a number
```
- **Weak**: A weakly typed variable (or language if enforced) does not require a fixed data type
```Typescript
// Typescript
let ageOrName: any = 24;
ageOrName = 'Alexander Jaye' // This works 👍
```


---

## Quick Exercises
<sub>*In your programming language of choice...*</sub>
1. Assign and print to the console the value of 42 to a variable named `meaningOfLife`
2. Now assign the value of 180 to the `meaningOfLife` and print it to the console
