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
