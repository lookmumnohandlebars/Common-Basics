# Objects & Classes

Objects are a common feature in most languages - they are used for structured data (stored within a single variable). Classes are commonly used to define a blueprint when creating Objects that contain the same data.

Objects are also a collection of data (one that is often native to the language), and as such are a reference type.

## 📦 Objects

Objects are a structured collection of data defined by 2 major features:

- State: What data it holds (for its lifetime)
- Behaviour: What functions (known as methods) the object has

Here is an example in Javascript (in which dynamic objects are common-place)

```Typescript
let character = {
    name: "Alex" // state (variable the belongs to the object)
    sayHello: function () { return 'Hello, my name is ' + this.name} // behaviour
}

character.name = "Barry";
character.sayHello(); // Hello, my name is Barry
```

## 🎓 Classes

Classes are blueprints for how an object should be created. Every object created from a class constructor is said to be an instance of that class.

> An object is (or can be) an instantiation, or existence, of a class.

Here is an example of the character object rewritten as a class in TypeScript:
```Typescript
class Character {
    constructor(name: string) { // constructor
        this.name = name
    }
    public name: string;
    public
}
```

## ‼️ An important reminder on reference types

Most of the time, because objects are 'large' (in comparison to numbers), variables that refer to an object reference the memory address, not the value of the object.

Here's a quick example in TypeScript, which treats all objects as reference types

```TypeScript
// Character is a class with a 'Name' state/property
let obj = new Character(); // obj aliases a character object
obj.Name = "Alex"
console.log(obj.Name); // prints character name "Alex"
let copy = obj; // Copies the reference to obj
copy.Name = "Batman"; // sets the object name to "Batman"
console.log(obj.Name); // Prints original object name as "Batman"

/**
 * This is because 'copy' is assigned the reference of the object, not the value, so it actually refers to the same instance of the original Character object.
*/
```

This is common to many languages due to the way that values are stored. If you think about it, if each time we passed in an object to a function, the whole object is copied, then suddenly it takes much more memory (avalaible data space). So this is an often used optimisation (sometimes enforced in a language) to minimise the program memory taken by objects.

Lower-level (more nitty-gritty) programming languages such as C++, Go & Rust.

## 🗯 Examples

###
