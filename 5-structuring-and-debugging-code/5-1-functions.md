# 5.1: Functions

{% embed url="https://youtu.be/M0yXZtZSg-A" %}

We now have a basis to begin formally defining the code structures we're working with and using them to write slightly more realistic programs.

Let's first talk a little about how functions work:

## What does a function do?

A function is just a collection of lines of code. We can run those lines of code when we write the appropriate code statement.

A function is a type of **control flow**, which means we can write code that **does not** just execute line by line downwards through the code file. We can control the order and flow of the execution of our lines of code.

### Define a function

First we'll define a function that isolates the kilometers to miles conversion we were making before, then we'll use it in our program.

Start at the bottom of our `script.js` file.

Create a variable `var kilometersToMiles`

We assign a function to that variable: `var kilometersToMiles = function`

We note the beggining and end of the function `block` with **curly braces**:

```javascript
var kilometersToMiles = function(){

};
```

We define what actions happen when the function will be executed:

```javascript
var distanceInMiles = distanceInKilometers * 0.62;
```

Using `return` keyword we define the output value of the function:

```javascript
return distanceInMiles;
```

We define the function input called a `parameter` as `distanceInKilometers`.

```javascript
var kilometersToMiles = function(distanceInKilometers){
```

All together it looks like this:

```javascript
var kilometersToMiles = function(distanceInKilometers){

  var distanceInMiles = distanceInKilometers * 0.62;

  return distanceInMiles;
};
```

### Execute a function

Let's run this function without the rest of our starter code first.

The syntax for running our function is to mention the name of the function and add **parentheses** to the end of it:

```javascript
kilometersToMiles();
```

Our function takes an argument - an actual value representing kilometers:

```javascript
var someNumber = 4;
kilometersToMiles(someNumber);
```

Let's test this without having to worry about the rest of the starter code.

Open your developer tools by going to the top level menu and selecting view -&gt; developer -&gt; javascript console.

Paste the above code into the console.

You should see the calculated result.

Type the name of the function into the console. You should see the code `block` you defined.

You can run this code again from the console with a different value:

```javascript
kilometersToMiles(7676);
```

Type in your own values.

### Capture the result

We can see the result of the calculation in the console.

We can also capture that value to use it later.

```javascript
var result = kilometersToMiles(7676);
```

Type in the name of the variable: `result` and press enter to see the given value.

### Putting it all together

Inside main call the functions and give the input value as an argument.

```javascript
var main = function(input) {

  var myOutputValue = kilometersToMiles(input);

  return myOutputValue;
};

var kilometersToMiles = function(distanceInKilometers){

  var distanceInMiles = distanceInKilometers * 0.62;

  return distanceInMiles;
};
```

## Other Examples

### Doubling a number

```javascript
var double = function(number){
  return number * 2;
};
```

### Kilos to pounds

```javascript
var kilosToPounds = function(kilos){
  return kilos * 2.2;
};
```

### Area of a circle

```javascript
var circleArea = function(radius){
  var pi = 3.1415;
  return pi * radius * radius;
};
```

## Main function

We can now define `main` as a function. However, we are not in charge of running it. Our starter code is running it for us whenever we click the submit button.

The `input` parameter of `main` is whatever gets typed in the input box.

The `return` value is what gets displayed in the grey box.

With this in mind, assign the value of `input` to myOutputValue to see this connection.

Then change the code again to assign the string value "wow hello" to `myOutputValue`.

## What is a function for?

We already defined a function as a collection of lines of code we can run.

Sometimes we just want to run a set number of lines of code collected together in our programs.

We are doing this in `main` - it is everything that we want to happen when the submit button is clicked.

Given the above function examples we can also say that a function can be a data calculation given some inputs. We can define an action as the kind of data it takes in and the kinds of outputs it gives.

## Exercises

{% hint style="info" %}
### **1\) Duplicate and run the code above.**

### **2\) Errors: take out `return` and `input` from the examples. What happens? Why?**

### **3\) Apps**

For the following apps try to encapsulate each distinct operation inside a function that returns a value. e.g.,`daysToMinutes(3)`.

#### **Juice Wedding**

It takes 4 oranges to make a 90ml glass of orange juice.

When planning your wedding, you need to know how many oranges to buy so all your guests have juice.

The user will enter a number of guests and the app will say how many oranges are needed and how many litres of orange juice you would get.

#### **SG Hugs**

Everyone has a different gauge for how long they like to hug.  
  
The user can enter a number of seconds they like to hug on average, and the app will calculate how many years it will take to hug everyone in Singapore.  
  
You are of course allowed 9 hours a day to sleep and eat.

#### **House Paint**

You want to be able to estimate the price of painting your home.

Your designer home only has windows and doors that are the same size- 90cm x 150cm. 8 windows and 3 doors.

Each room in your 6 room house is the same size: 3m x 3m.

Paint will cover about 300 square meters a litre. You want to use 2 coats.

The user can enter a dollar amount of paint per litre and the app will calculate how much it will cost.

**Train Speed**

Two trains are going to leave for the trip north to Tokyo.

Train 1 is traveling 200kph. It will reach Tokyo in 2 hours.

Train 2 is newer and can travel faster.

A bird lands on the track and delays the 2nd train.  
  
The app will help the conductor by allowing him to enter the current amount of minutes they are delayed and then calculating how fast they need to travel to arrive at Tokyo at the same time as train 1. Output the speed in kph in the grey box.

### More Comfortable

#### **Clock**

A user can enter the number of minutes past 1pm and the app will calculate the angle between the hour and minute hand.
{% endhint %}
