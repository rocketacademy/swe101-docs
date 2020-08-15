# 6.1: Intro to Logic

So far what we have coded are basically calculators or, if the program deals with words, programs that fill in the blanks.

The next level of complexity is to create progams that, given some possible inputs, give output based on some logical decision.

## Simple Condition Example: Secret Word

Let's write a program that changes the output value of "hello world" if you type in a particular phrase.

### if statement

An if statement is a control flow `block` that runs if a condition is `true`. We'll talk more about what specifically `true` means later, but you can see that what's happening is very intuitive.

```javascript
var main = function (input) {
  var myOutputValue = 'hello world';

  if (input == 'palatable papaya') {
    myOutputValue = 'you wrote the secret phrase!';
  }

  return myOutputValue;
};
```

On line 5 we put our `if` statement. This is testing to see if `input` parameter is **equal** to the string value phrase we want to look for.

If it is equal the code we wrote between the curly braces runs.

If it is **not equal** it doesn't run.

This is the 2nd main way we use curly braces to denote `blocks` - specific sections of code that run or not given some **control flow**. We'll cover one other control flow syntax later using curly braces, **loops**.

Try your program both ways. Enter the secret phrase and click the button to see the different output. Enter anything else and click the button to see the base case.

#### equality

We're using the **boolean operator** `==` to test to see if `input` is **equal** to "palatable papaya".

## comments

Now that things are getting more complicated, we might want to leave notes to ourselves and others that say what our code does.

Comments let you write things in the code file that are just notes.

```javascript
// this won't actually run
```

## dice game

Let's build a game of dice program. We will begin with very simple rules to this game: guess the number we will roll.

### randomness / dice

Let's build the random number generation before we talk about the dice game logic.

Javascript language can produce random numbers using a build-in set of functions called `Math` \(case-sensetive\).

```javascript
var myRandomValue = Math.random();
```

Calling `Math.random()` returns a random number value. However we have a dice game, so there is more code we have to write to get the value we want.

#### `Math.random()` returns a decimal number from 0-1.

We have to do some math on this number to get what we want.

We'll also be using another math functionality: `Math.floor()`.

We will use the code refered to on this [page.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)

We can make a function that produces any random integer:

```javascript
var getRandomInteger = function (max) {
  // produces a float between 1 and max + .999999 etc.
  var randomFloat = (Math.random() * max) + 1;

  // take off the decimal
  var resultInteger = Math.floor(randomFloat);

  return resultInteger;
};
```

But what we are creating is a dice rolling game, so we can just make a dice function.

We can make a function that produces any random integer:

```javascript
var diceRoll = function () {
  // produces a float between 0 and 7
  var randomFloat = Math.random() * 7;

  // take off the decimal
  var resultInteger = Math.floor(randomFloat);

  return resultInteger;
};
```

### Game: Dice Roll Guess

Let's implement the logical rules to our game.

If the dice roll the same number as the user entered, they win.

```javascript
var main = function (input) {
  var randomDiceNumber = diceRoll();

  var myOutputValue = 'you lose';

  if (randomDiceNumber == input) {
    myOutputValue = 'you win';
  }

  return myOutputValue;
};
```
