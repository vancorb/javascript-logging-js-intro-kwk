JavaScript Logging
---

In this lesson, we're going to focus on the methods on the `console` object. We've already made use of perhaps the most popular of these methods, `console.log()`; but there are a few more tricks up `console`'s sleeve. Let's
dive in!

![dive in](http://i.giphy.com/LlPGmmhr0GcKs.gif)

## Objectives

- Explore the `console` object
- Use different logging methods

## `console`

Open the console in your browser of choice.

Now enter `console` in the console (that's a little funky to say, huh?) and press "enter". In Chrome, you'll see something like

![console](https://curriculum-content.s3.amazonaws.com/skills-based-js/console.png)


To start, just explore that `console` object (you can click on the arrow to expand it). What methods does `console` expose? Can you guess what some of them might do?

When you've finished checking things out on your own, read on and code along to see what you might have missed. Be sure to try the examples below in your console!


### `log()`

The venerable `console.log()` is an all-purpose logging method. In programming, _logging_ refers to the process of printing information about the program as it runs. Try it out!

``` javascript
console.log("I'm logging! I'm a regular lumberjack!")
```

You can pass any number of messages to `console.log()` by separating them with commas; when printed, they'll be separated by a space:

``` javascript
console.log('one', 'two', 'three')
```

When you enter the above in your console, you'll see "one two three".

And you don't just have to pass strings to `console.log()` — try this:

``` javascript
console.log("I must have logged", 1000, "times today.")
```

You should see "I must have logged 1000 times today."

Note that when you use strings, the comma must come _after_ the end quotation mark — this is because it's not punctuation like in English writing, but a way of telling JavaScript, "Hey, I'm going to give you something else!"

### `error()`

`console.error()` prints an error and usually includes a _stack trace_. "Stack traces" is a report of code that was executed at a certain time (in this case, starting from when the error occurred and working backwards). Enter the following in your console:

``` javascript
console.error('Danger, Will Robinson!')
```

You should see something like

![console.error](https://curriculum-content.s3.amazonaws.com/skills-based-js/console_error.png)

If you click on the arrow, you can see the stack trace. When you're debugging, you can click on the linked line numbers in the stack trace to jump to the relevant line in the source code. That won't be particularly useful here, since it will just take you to some of Chrome's internal JavaScript — but it can be incredibly useful when you're writing your own code!

You can pass several messages at once, separated by a comma:

``` javascript
console.error("Danger!", "Something bad happened!", "Time to debug!")
```

When printed, there will be a space after each message: `"Danger! Something bad happened! Time to debug!"`.

``` javascript
console.trace()
```

### `warn()`

`console.warn()` does as its name suggests: it prints a warning. Libraries use this function to warn developers that an action they've taken _might_ not be wise — one common use-case is giving developers a heads-up about deprecations.

``` javascript
console.warn('Hm, you might not want to do that.')
```

## Wrap-up

`console` has _tons_ (or _tonnes_ for some folks) of useful functionality — be sure to explore! Logging info, errors, warnings, and stack traces is essential to staying on top of your application's functionality.

## Resources

- [MDN: Console](https://developer.mozilla.org/en-US/docs/Web/API/Console)
