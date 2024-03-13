# Arrays

## Array Methods
1. Array Push:
• the 'push' method adds one or more elements to the end of an array

```javascript
let fruits = ['apple', 'orange'];
fruits.push('banana', 'grape');
console.log(fruits); // output: ['apple', 'orange', 'banana', 'grape']
```

2. Array Pop:
* the 'pop' method removes the last element from an array and returns that element

```javascript
let fruits = ['apple', 'orange', 'banana'];
let removedFruit = fruits.pop();
console.log(fruits); // output: ['apple', 'orange', 'banana']
console.log(removedFruit) // output 'banana'
```

3. Array Shift:
* the 'shift' method removes the first element from an array and shifts the remaining elements to a lower index

```javascript
let fruits = ['apple', 'orange', 'banana',];
let removedFruit = fruits.shift();
console.log(fruits); // ['orange', 'banana']
console.log(removedFruit) // output: 'apple'
```

4. Array Unshift:
* the 'unshift' method adds one or more elements to the beginning of an array and shifts the existing elements to higher indexes

```javascript
let fruits = ['orange', 'banana'];
fruits.unshift('apple', 'grape');
console.log(fruits); // output: ['apple', 'grape', 'orange', 'banana']
```

## Add To Array
This function allows you to add an element to thr front or back of an array based on the specified location. If an invalid location is provided, it logs an error message.

```javascript
function addToArray(location, element, arr) {
    // check specified location for adding element
    if (location == "FRONT") {
        // add element to front of array
        arr.unshift(element);
    } else if (location == "BACK") {
        // add element to back of array
        arr.push(element);
    } else {
        // if invalid location is provided, log error message
        console.log("ERROR: Invalid location specified");
    }
}

testArray = [1,2,3]

addToArray("FRONT", 0, testArray)
console.log(testArray) // [0,1,2,3]

addToArray("BACK", 4, testArray)
console.log(testArray) // [0,1,2,3,4]

addToArray("MIDDLE", 4, testArray) // "ERROR"
console.log(testArray) // [0,1,2,3,4]
```

## Range
Creates an array that includes all numbers within a specified range (inclusive).

```javascript
let range = function(min, max) {
    // create an empty array to store the result
    let array = [];

    for (let i = min; i <= max; i++) {
        // push each number to the array
        array.push[i];
    }
    return array;
}
```

## factors Of
Returns an array containing all positive numbers that are able to divide into 'num' with no remainder.

```javascript
let factorsOf = function(num) {
    let factors = [];

    for (let i = 1; i <= num; i++) {
        if (num % i === 0) {
            factors.push(i);
        }
    }

    return factors;
}

console.log(factorsOf(9)); // [ 1, 3, 9 ]
console.log(factorsOf(10)); // [ 1, 2, 5, 10 ]
```

## Fizz Buzz Array
Function returns an array containing all positive numbers less than 'max' that are divisible by either 3 or 5, but not both.

```javascript
let fizzBuzz = function(max) {
    let array = [];
    for (let i = 1; i < max; i++) {
        if ((i % 3 === 0 && i % 5 !== 0) ||
        (i % 3 !== 0 && i % 5 === 0)) {
            array.push(i);
        }
    }
    return array;
}

console.log(fizzBuzz(12)); // [ 3, 5, 6, 9, 10 ]
console.log(fizzBuzz(20)); // [ 3, 5, 6, 9, 10, 12, 18 ]
```

## Double Sequence
Generates a sequence of doubled values starting from a given base value until the specified length is reached.

```javascript
let doubledSequence = function(base, length) {
    // Check if length 0, return empty array
    if (length === 0) {
        return [];
    }

    // create array with initial base value
    let seq = [base];

    // while length of array is less than specified length
    while (seq.length < length) {
        // get last element in array
        let last = seq[seq.length - 1];

        // calculate next value by doubling last element
        let next = last * 2;

        // add next value to array
        seq.push(next);
    }
    // return resulting array
    return seq;
}

console.log(doubleSequence(7, 3));  // [7, 14, 28]
console.log(doubleSequence(3, 5));  // [3, 6, 12, 24, 48]
```
