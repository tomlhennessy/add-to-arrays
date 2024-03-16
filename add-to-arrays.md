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

## Triple Sequence
Generates a sequence of numbers starting from a given number, where each subsequent number is obtained by multiplying the previous number by 3.

```javascript
function tripleSequence(start, length) {
    // initialise array to store sequence, starting with given number
    let seq = [start];

    // loop starting at index after last element in seq array, in this case: 'i = 1' as there is only ever one element. but 'i = sq.length' is a more generalised approach
    for (let i = seq.length; i < length; i++) {
        // multiply last number by 3 and add to sequence
        seq.push(seq[seq.length - 1] * 3);
    }
    return seq;
}

console.log(tripleSequence(2, 4)); // [2, 6, 18, 54]
console.log(tripleSequence(4, 5)); // [4, 12, 36, 108, 324]
```

## Unique
Function to return an array containing only unique elements from the input array.

```javascript
let unique = function(array) {
    // initialise empty array to store unique elements
    let uniques = [];

    for (let i = 0; i < array.length; i++) {
        // get current element
        let el = array[i];

        // check if element is not already present in uniques array
        if (!uniques.include(el)) {
            // if current element not present, add it to uniques array
            uniques.push(el);
        }
    }
    return uniques;
}

console.log(unique([11, 7, 8, 10, 8, 7, 7])); // [11, 7, 8, 10]
console.log(unique(['a', 'b', 'c', 'b'])); // ['a', 'b', 'c']
```

## Yeller
Converts each word in an array to uppercase and adds an exclamation mark

```javascript
let yeller = function(words) {
    // initialise empty array to store modified words
    let newWords = [];

    for (let i = 0; i < words.length; i++) {
        // get current word
        let word = words[i];

        // convert to 'yelled' word
        let modifiedWord = word.toUpperCase() + '!';

        // add mofified word to newWords array
        newWords.push(modifiedWord);
    }
    return newWords;
}

console.log(yeller(['hello', 'world'])); // [ 'HELLO!', 'WORLD!' ]
console.log(yeller(['kiwi', 'orange', 'mango'])); // [ 'KIWI!', 'ORANGE!', 'MANGO!' ]
```

## Tripler
Returns a new array containing three times every number of the original array.

```javascript
let tripler = function(nums) {
    // initialise array to store tripled nums
    let newNums = [];

    for (let i = 0; i < nums.length; i++) {
        // assess each number, store in variable 'num'
        let num = nums[i];

        newNums.push(num * 3);
    }
    return newNums;
}

console.log(tripler([2, 7, 4])); // [ 6, 21, 12 ]
```

## Long Words
returns an array containing only the words that are longer than 5 characters.

```javascript
let longWords = function(words) {
    let filteredWords = [];

    for (let i = 0; i < words.length; i++) {
        // access current word
        let word = words[i];

        if (word.length > 5) {
            filteredWords.push(word);
        }
    }
    return filteredWords;
}

console.log(longWords(['couscous', 'soup', 'ceviche', 'solyanka' ,'taco'])); // [ 'couscous', 'ceviche', 'solyanka' ]
```

## Choosey Endings
Takes an array of words and a suffix as input. Any words that end the suffix are returned in an array.

```javascript
let chooseyEndings = function(words, suffix) {
    // check if input words is not an array
    if (!Array.isArray(words)) {
        // if not array, return empty array
        return [];
    }

    // define empty array to store filtered words
    let filteredWords = [];

    // iterate through each word in input array
    for (let i = 0; i < words.length; i++) {
        // get current word from array
        let word = words[i];
        // check if current word ends with provided suffix
        if (word.endsWith(suffix)) {
            // add to filteredWords array
            filteredWords.push(word);
        }
    }
    return filteredWords;
}

console.log(chooseyEndings(['family', 'hound', 'catalyst','fly', 'timidly', 'bond'], 'ly'));
// [ 'family', 'fly', 'timidly' ]
```

## Common Factors
Accepts two numbers as arguments. Function should return array containing positive numbers that are able to divide into both arguments.

```javascript
let commonFactors = function(num1, num2) {
    let factors = [];
    for (let i = 1; i <= num1; i++) {
        if (num1 % i === 0 && num2 % i === 0) {
            factors.push(i);
        }
    }
    return factors;
}
```

## Adjacent Sums
Takes an array of numbers as an input. It iterates through calculates the sum of the adjacent elements, adding each new sum to a new array.

```javascript
let adjacentSums = function(array) {
    if (!Array.isArray(array)) {
        // if not an array, throw an error message
        throw 'Not an array!';
    }

    // define empty array to store sums of adjacent elements
    let sums = [];

    // iterate through each element, except last
    for (let i = 0; i < array.length - 1; i++) {
        // calculate sum of current element and next element
        let sum = array[i] + array[i + 1];
        // add sum to sums array
        sums.push(sum);
    }
    // return array containing sums of adjacent elements
    return sums;
}
