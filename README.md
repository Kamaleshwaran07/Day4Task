# Day4Task

Solve problems using Anonymous function and IIFE function
## 1. Print odd numbers in an array
### Using Anonymous function
```
const odds = function(array, arr) {
  for (let i=0; i <= array.length; i++){
    if ( i %2 !== 0){
      arr.push(i);    
    }
  }
  return(arr)   
}
console.log(odds([1,2,3,4,5,6,],[]))
```
### Using IIFE function
```
(function odds(array, arr) {
  for (let i=0; i <= array.length; i++){
        if ( i %2 !== 0){
           arr.push(i);
         }
       }
       console.log(arr)
})([1,2,3,4,5,6,],[])
```
2. Convert all the strings to Title cap in a string
   ### Using Anonymous function

```
  var string = function (str) {
  str = str.toLowerCase().split(' ');
  for (var i = 0; i < str.length; i++) {
    str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1);
  }
  return str.join(' ');
}
console.log(string("IT WAS A NICE DAY"))

```

### Using IIFE function

```
  let string = (function (str) {
  str = str.toLowerCase().split(' ');
  for (var i = 0; i < str.length; i++) {
    str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1);
  }
  return str.join(' ');
})
console.log(string("IT WAS A NICE DAY"))
```

## 3. Sum of all numbers in an array

### Using Anonymous function

```
let array = function (arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum = sum + arr[i];
  }
  return sum;
};
console.log(array([1, 2, 3, 4]));
```
### Using IIFE function

```
let array = (function (arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum = sum + arr[i];
  }
  return sum;
});
console.log(array([1, 2, 3, 4]));
```
## 4. Return all the prime numbers in an array
### Using Anonymous function

```
const primeArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let isPrime = function (num) {
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
};

const numArr = primeArray.filter(function(num) {
  return isPrime(num);
});
console.log(numArr);

```
### Using IIFE function

```
const primeArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let isPrime = (function (num) {
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
});
const numArr = primeArray.filter(function(num) {
  return isPrime(num);
});
console.log(numArr);

```

## 5. 































