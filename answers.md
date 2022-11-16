### Q1
What is the value of `result` after calling this function? Why?

```javascript
function myFunction(num1, num2) {
  return num1+num2
}

const result = myFunction(5,5)
```

The result of this function will be 10 because it adds up the num1 and num2.

What actually happened: Exactly what we thought


### Q2
What is the value of `result` after calling this function? Why?

```javascript
function myFunction(num1, num2) {
  num1+num2
}

const result = myFunction(5,5)
```

It will add the numbers but it will not return a result, so it will be undefined.

What actually happened: Exactly what we thought


### Q3
What is the value of `num` at the end of the program? Why?

```javascript
function myFunction(num) {
  return num-1
}

let num = 10
num = myFunction(num)
num = myFunction(num)
``` 

The function will -1 from 10 making it 9, but then it will run again making it 8.

What actually happened: Exactly what we thought


### Q4
What is the value of `add` and `num` at the end of the program? Why?

```javascript
function myFunction(num) {
  return num-1
}

let num = 10
let add = 3
add = myFunction(add)
add = myFunction(add)
```

The value of `add` will be 1 as it goes through the function twice, but the value of `num` is never used by the function.

What actually happened: Exactly what we thought


### Q5
What value will be logged inside the function call? Why?

```javascript
function myFunction(num, num1) {
  console.log(num1)
}

let num = 10
let num1 = 2

myFunction(num)

```

The result would be undefined as the function is trying to log `num1` but that number is never called into the function.

What actually happened: Exactly what we thought


### Q6
What value will be logged inside the function call? Why?

```javascript
function myFunction(num, num1) {
  console.log(num1)
}

let num = 10
let num1 = 2

myFunction(num1, num)
```

The result of this function would be 10 as the second number that is called is `let num = 10` so the function is basically saying `myFunction(2, 10)`.

What actually happened: Exactly what we thought


### Q7
What will the value of counter be at the end of this program? Why?

```javascript
let counter = 1

function myFunction() {
  counter++
  return counter
}

myFunction()
const num = myFunction()
```

The result of this function should be 3, as the number we start with is 1 which then changes to 2 after the first function runs, but we run the function twice so the final number would be 3.

What actually happened: Exactly what we thought


### Q8
What will the value of `result` be at the end of this program? Why?

```javascript
function myFunction(num1, num2) {
  return num1 + num2
}

const num1 = 10
const num2 = 1
const num3 = 4

const result = myFunction(num3, num1)
```

The result of this function will be 14 as we are calling `num3` which is 4 and `num1` which is 10 and then the function adds those together.

What actually happened: Exactly what we thought


### Q9
What will be logged out on the console when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  console.log(num3)
}

const num1 = 10
const num2 = 1
const num3 = 20

myFunction(num3, num1)
```

The result of this function will be 20 as the function can see see the const `num3` which is outside of the function.

What actually happened: Exactly what we thought


### Q10
What will be logged out on the console when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  console.log(num3)
}

const num1 = 10
const num2 = 1
const num3 = 20

myFunction(num3, num1, 100)
```

The result of this function will be 100, as the scope of the function allows the console.log to call the `num3` that is in the function first before the `const num3 = 20`

What actually happened: Exactly what we thought


### Q11
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  return num1 + num2 + num3
}

const num1 = 10
const num2 = 1
const num3 = 20

const result = myFunction(1, 1, 1)
```

The result of this function will be 3 as we pass `1, 1, 1` into the argument. The constants that are outside it are unused in this function.

What actually happened: Exactly what we thought


### Q12
What will be the value of `result` when this code runs? Why?

```javascript
function getSomeValue() {
  return 2
}

function myFunction(num1) {
  const num2 = getSomeValue()
  return num1 * num2
}

const result = myFunction(5)
```

The result of this function will be 10 as the first functions declares that `getSomeValue()` is 2 and then in the second function we are just doing 5 * 2

What actually happened: Exactly what we thought


### Q13
What will be the value of `result` when this code runs? Why?

```javascript

function getSomeValue() {
  return 2
}

function myFunction(num1) {
  const num2 = getSomeValue()
  return num1 * getSomeValue()
}

const result = myFunction(5)
```

The result of this function will be 10 as the first functions declares that `getSomeValue()` is 2 and then in the second function we are just doing 5 * 2.

What actually happened: Exactly what we thought


### Q14
What will be the value of `result` when this code runs? Why?

```javascript
function getSomeValue() {
  return 2
}

function myFunction(num1) {
  return getSomeValue() * getSomeValue()
}

const result = myFunction(5)
```

The result of this would be 4 as it is just doing 2*2.

What actually happened: Exactly what we thought


### Q15
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {
  if(true) {
    return -10
  }

  return num1 * 10
}

const result = myFunction(5)
```

This function will return `-10` as the if statement is true