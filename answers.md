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

What actually happened: Exactly what we thought


### Q16
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {
  if(false) {
    return -100
  }

  return num1 * 10
}

const result = myFunction(5)
```

The result of this one would be 50 as the statement is set to false meaning it just skips the if statement and does 5*10 instead.

What actually happened: Exactly what we thought


### Q17
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {
  return -100

  return num1 * 10
}

const result = myFunction(5)
```

The result of this function will be `-100` as `return -100` is the first line in the function.

What actually happened: Exactly what we thought


### Q18
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {

  return num1 * 10

  return -100
}

const result = myFunction(5)
```

The result will be `50` as the first return statement in the function is `return num1 * 10` so it will just do 5*10.

What actually happened: Exactly what we thought


### Q19
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  return num2
}

const result = myFunction(5, 10, 15)
```

The result will be `10` as it is calling back the second value we sent through.

What actually happened: Exactly what we thought


### Q20
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  return num1 + num3
}

const num1 = 20
const num2 = 200
const num3 = 1000

const result = myFunction(5, 10, num3, 15)
```

The result of this should be `1005` as num1 is changed into 5 by the `myFunction(5, 10, num3, 15)` however num3 is not changed into anything else so it calls it from `const num3 = 1000` meaning the function is running `5 + 1000`.

What actually happened: Exactly what we thought


### Q21
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  const result = num1+num2
  return result
}

const result = myFunction(10, 20)
myFunction(100, 2)
```

The result of this should be 30 as the second myFunction is irrelevant, so we just add 10 + 20.

What actually happened: Exactly what we thought


### Q22
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  let result = num1+num2
  return result
}

let result = 0
myFunction(100, 2)
```

The `let result = 0` is outside the scope of the function so it will not be changed and the result will remain as `0`.

What actually happened: Exactly what we thought


### Q23
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  result = num1+num2
}

let result = 0
myFunction(100, 2)
```

Since inside the function we are just declaring that result is `result = num1+num2` instead of creating a new let, this will change the `let result = 0` to `102`.

What actually happened: Exactly what we thought


### Q24
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  const result = num1+num2
  return 100
}

const result = myFunction(5, 2)
```

The result for this one will be `100` as the previous values are irrelevant and it will just `return 100`.

What actually happened: Exactly what we thought


### Q25
What will be the printed out by the console log statements when this code runs? Why?
```javascript
function myFunction(a) {
  let b = 20
  
  console.log("a:", a)
  console.log("b:", b)
  console.log("c:", c)
}

let a = 1
let b = 2
let c = 3

myFunction(100)
```

For this one a will be 100, b will be 20 and c will be 3. The a is 100 because its in the argument when we call the function. The b is 20 because inside of the function we have declared that b = 20. The c will be 3 as the only place that it is declared is outside of the function as c = 3.

What actually happened: Exactly what we thought