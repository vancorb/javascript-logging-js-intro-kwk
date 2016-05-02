JavaScript Logging
---

In this lesson, we're going to focus on the methods on the `console` object.
We've already made use of perhaps the most popular of these methods,
`console.log()`; but there are a few more tricks up `console`'s sleeve. Let's
dive in!

![dive in](http://i.giphy.com/LlPGmmhr0GcKs.gif)

## `console`

Open the console in your browser of choice. Different browsers have slightly
different implementations of the `console` object, but we'll look at a subset
of its most important functionality.

To start, just type `console` and explore. What methods does `console` expose?
Can you guess what some of them might do?

When you've finished checking things out on your own, read on to see what you
might have missed. Be sure to try the examples below in your console!

### `assert()`

`console.assert()` throws an error unless its first argument evaluates to
`true`.

``` javascript
var alpha = 'a'
var beta = 'b'

console.assert(alpha === alpha) // undefined
console.assert(alpha === beta) // error!
```

### `dir()`

`console.dir()` allows you to explore objects' properties interactively.

``` javascript
var myObject = {
  myProperty: {
    mySubProperty: {
      surprise: "HI!"
    }
  }
}

// now you can explore `myObject` interactively!
console.dir(myObject)
```

### `error()`

`console.error()` prints an error and usually includes a stack trace. "Stack
traces" is a report of code that was executed at a certain time (in this case,
starting from when the error occurred and working backwards).

``` javascript
var error = new Error('Uh-oh!')

console.error(error.message) // 'Uh-oh!' all in red

// What do you think this will do?
console.error('Danger, Will Robinson!')

// String substitution is allowed!
console.error('Something %s happened %d times', 'bad', 10)
```

### `log()`

The venerable `console.log()` is an all-purpose logging method. It takes any
number of arguments and allows for string substitution.

``` javascript
console.log('one', 'two', 'three') // 'one two three'
console.log('%d', 1, 'two', 3) // '1 two 3'
```

### `trace()`

`console.trace()` prints out a stack trace starting at the current execution
frame (usually, the current line of code in the context in which it's running).

``` javascript
console.trace()
```

### `warn()`

`console.warn()` does as its name suggests: it prints a warning. Libraries use
this function to warn developers that an action they've taken _might_ not be
wise — one common use-case is giving developers a heads-up about deprecations.

``` javascript
console.warn('Hm, you might not want to do that.')
```

## Wrap-up

`console` has _tons_ (or _tonnes_ for some folks) of useful functionality — be
sure to explore! Logging info, errors, warnings, and stack traces is essential
to staying on top of your application's functionality.

## Resources

- [MDN: Console](https://developer.mozilla.org/en-US/docs/Web/API/Console)
