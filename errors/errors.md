# Errors

When something goes wrong in a program, errors, or exceptions, are used to signal that the program has failed in an unrecoverable way.

Generally speaking, if unhandled, an error will cause a program to exit at the point it is raised.

## Compile-Time Errors

Depending when the program (in the language or framework you are using) compiles into an executable (machine code), compile-time errors should be catch

## Runtime Errors

A runtime

## 🔔 Raising / Throwing Errors

There are cases where you may want to raise, or throw, an error yourself - in the event that something would break the logic or operation of your code. Languages have slightly different ways of raising or throwing an error.

Python:

```python
raise Exception("I screwed up!")
```

Typescript:

```TypeScript
throw new Error("I screwed up!")
```

C#:

```C#
throw new Exception("I screwed up!")
```

Ruby:

```Ruby
raise RuntimeError.new("I screwed up!")
```

## 🧤 Handling Errors

In the event of an error being thrown, by the code in the program or a dependency, it is possible to handle the error and execute code in the event an error is thrown.

### "Trying" Code

To be able to handle errors, the code needs to signal that it expects an error may happen within the current scope (because otherwise errors should not happen and the program will exit).

Most languages do this with a "try" block that quite literally tries to execute the code in it's scope. This allows errors/exceptions to be handled.

### "Catching" Code

Within the context of a try, normally a try block is followed by a catch block, which catches the error enables further code to be executed.

Two important notes here:

-

### "Finally" Code

### Examples

Python:

```python
try:
    raise Exception("I screwed up!")
except Exception, e:
    print(str(e))
else:
    print("I didn't screw up")
finally:
    print("Thats why they call me Archimedes")
```

Typescript:

```TypeScript
try {
    throw new Error('I Screwed Up!') // Custom error always gets thrown
} catch (error) {
    // handle error not being an Error, weird Typescript behaviour
    if (!(error instanceof Error)) {
        console.error('unknown error')
        throw new Error("Unknown error occured")
    }
    console.log(error.message); // print the error message
} finally {
    console.log('Thats why they call me Archimedes'); // This will always print, regardless of error
}
```

C#:

```C#
try {
    throw new Exception("I Screwed Up!")
} catch (Exception e) {
    Console.WriteLine(e.Message);
} finally {
    Console.WriteLine("Thats why they call me Archimedes");
}
```

Ruby:

```Ruby
begin
    raise RuntimeError.new("I screwed up!")
rescue RuntimeError => e
  puts e.message
else
    puts "I didn't screw up!"
ensure
    puts "Thats why they call me Archimedes"
```

## 🐛 Debugging / Resolving Errors

- **Using A Debugger**: Most compiled languages allow you to attach a debugger, which means you can target code statements to pause on and observe the
- Logging: Logging is a tried and tested way to figure out what is going wrong.

## 🎁 Common Errors

- Null / None / Undefined Reference: This happens when
- Arithmetic Errors:
-
