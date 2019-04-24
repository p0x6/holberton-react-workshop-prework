# Holberton School React Workshop

## Prerequisite work instructions - __Please Read__:

These exercises are to be completed before the first workshop session. It should take around 1 to 1.5 hours to complete.

### Submission details
Please use [JSFiddle](https://jsfiddle.net) complete each exercise.
**So, you should have a total of 8 JSFiddle url’s as there are 8 exercises.**

After completing all the exercises, open an [issue in this repo](https://github.com/p0x6/holberton-react-workshop-prework/issues/new).

You can set the title to anything you want.

In the issue body please use this format.
```text
Name:
Slack Name:
Answers:
1)
...
8)
```
make sure to tag me at the end `@p0x6` so I can review.
***

# Mandatory Holberton School React Workshop Exercises

## 1) Arrow Functions Exercise
- Below we have a factorial function that clearly uses the 'function' keyword.  **Your challenge exercise is to refactor the factorial function below to use ES6 fat arrow syntax.**  Keep in mind that there isn't anything wrong with using the `function` keyword, but it does look better with the fat arrow syntax instead.

### Fat arrow function rules
- Keep in mind the rules for fat arrow functions:

```
- For functions with just one argument, the parentheses around the argument list are not required.
- For functions with just a single expression in the body, we can remove the curly 
  braces and 'return' keyword.
```

**Factorial with "function" keyword:**

```javascript
const fact = function factorial(n) {
  if (n === 0) return 1;
  
  return n * factorial(n - 1);
}
```
***

## 2) Destructuring Exercise

- Below we have some code that references `bio` *twice* inside the `isStudent` function.  

```javascript
const bio = {
  title: 'Student',
  cohort: 2,
};


function isStudent(bio) {
  var title = bio.title;
  var cohort = bio.cohort;
  return title === 'Student' && cohort === 2;
}
```

- **Your challenge exercise is to refactor the code used to reference the `title` and `cohort` properties.  You should use ***destructuring***** Try to get the `isStudent` function down to a single line.

***

## 3) Destructuring and Map() Exercise

- Suppose we have an array of arrays representing a student's assignments.  For example, our array of arrays would look something like this:

```javascript
const assignments = [
  [ '0x00. Vagrant', 1, 100 ]
];
```

- Each array in our assignments array has the structure of `[assignmentName, submitAttempts, score]` - in that exact order. **Now, your challenge exercise is to convert this array of arrays into an array of *objects* instead.**  Each object inside the array should have the keys `assignmentName`, `submitAttempts`, and `score` - along with the associated values for each key.  The resulting array of objects should be assigned to a variable named `assignmentsAsObject`. 

- Your data structure should have a setup like this (in this example we only have one object, but yours would have three):

```javascript
const assignmentsAsObject = [{ assignmentName: '0x00. Vagrant', submitAttempts: 1, score: 100 }]
```

- So, to summarize, take the array of arrays (reproduced below) and convert it into an array of ***objects*** stored in an array called `assignmentsAsObject`.  You must use both ***array destructuring*** and the ***map*** helper.  

```javascript
const assignments = [
  [ '0x00. Vagrant', 1, 100 ],
  [ '0x02. vi', 3, 100],
  [ '0x03. Git', 5, 0 ],
];
```

- Remember that to destructure arrays we must use the square brackets (the `[]`) instead of the curly braces (the `{}`).

***

## 4) ES6 Classes Exercise
- Create an ES6 class called `User`.  **Your challenge exercise is to do some basic initialization for instances of the User class inside the constructor.**  Here is what you need to do specifically:
```
- The constructor will accept a 'profile' object that has 'name' and 'title' properties.
  You need to assign those 'name' and 'title' properties to User as well.
- Initialize the 'cohort' property of the User class to 'Holberton'.
- Create an instance of the class.
```

***

## 5) ES6 Classes Exercise
- Now that we have our User class, your challenge exercise is to create a subclass of the `User` class called `Student`.  
- The requirements for the `Student` class are:
```
- The Student class should have a `setCohort` method.  The only argument to this 
  method is another instance of the `Student` class.
- The instance of `Student` that is passed into `setCohort` should have 
  it's `cohort` changed to.
- Create an instance of the class.
```

***

## 6) Rest Operator Exercise
- Refactor the function below to use the rest operator:

```javascript
function totalScore(v, w, x, y, z) {
  var scores = [v,w,x,y,z];
 
  return scores.reduce(function(accumulator, score) {
    return accumulator + number;
  }, 1)
}
```
***
## 7) Spread Operator Exercise

- Refactor the function below to use spread operator (arr1 and arr2 are arrays):

```javascript
function join(arr1, arr2) {
  return arr1.concat(arr2);
}
```

***
## 8) Rest Operator Exercise #2

- Refactor the function below to use only the rest operator:

```javascript
function unshift(array, x, y, z) {
  return [x, y, z].concat(array);
}
```
