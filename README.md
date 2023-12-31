# Day4Task

# 1st Part of Task

## Solve problems using Anonymous function and IIFE function
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
## 2. Convert all the strings to Title cap in a string
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

## 5. Return all the palindromes in an array

### Using Anonymous function

```
const words = ["level", "hello", "racecar", "world", "madam"];

const isPalindrome = function (word) {
  const reversed = word.split("").reverse().join("");
  return word === reversed;
};

const palindromes = words.filter(isPalindrome);

console.log(palindromes);

```
### Using IIFE function 

```
const words = ["level", "hello", "racecar", "world", "madam"];

const isPalindrome = (function (word) {
  const reversed = word.split("").reverse().join("");
  return word === reversed;
});

const palindromes = words.filter(isPalindrome);

console.log(palindromes);

```

## 6. Return median of two sorted arrays of the same size.

### Using Anonymous function

```
let median = function (a, b) {
let c = [...a, ...b].sort((a, b) => a - b);

  const half = (c.length / 2) | 0;

  if (c.length % 2) {
    return c[half];
  } else {
    return (c[half] + c[half - 1]) / 2;
  }
};
let arr1 = [1, 12, 15, 26, 38, 24];
let arr2 = [2, 13, 17, 30, 45, 47];
console.log(median(arr1, arr2));

```
### Using IIFE function

```
let median = (function (a, b) {
  let c = [...a, ...b].sort((a, b) => a - b);

  const half = (c.length / 2) | 0;

  if (c.length % 2) {
    return c[half];
  } else {
    return (c[half] + c[half - 1]) / 2;
  }
});
let arr1 = [1, 12, 15, 26, 38, 24];
let arr2 = [2, 13, 17, 30, 45, 47];
console.log(median(arr1, arr2));

```
## 7. Remove duplicates

### Using Anonymous function

```
const removeDuplicates = function (arr) {
  let result = [];
  for (let ind in arr) {
    if (ind == arr.indexOf(arr[ind])){
      result.push(arr[ind]);
    }
  }
  return result;
};

let arr = [
  1, 2, 4, 4, 5, 6, 7, 7, 8, 9, 9, 2, 3, 3, 6, 5
];
let ans = removeDuplicates(arr);
console.log(ans)

```

### Using IIFE function

```
const removeDuplicates = (function (arr) {
  let result = [];
  for (let ind in arr) {
    if (ind == arr.indexOf(arr[ind])){
      result.push(arr[ind]);
    }
  }
  return result;
});

let arr = [
  1, 2, 4, 4, 5, 6, 7, 7, 8, 9, 9, 2, 3, 3, 6, 5
];
let ans = removeDuplicates(arr);
console.log(ans)

```
## 8. Rotate an array by k times

## Using Anonymous function

```
const rotateArray = function (arr, k) {
  const n = arr.length;
  k = k % n; 
  const rotatedArray = arr.slice(k).concat(arr.slice(0, k));

  return rotatedArray;
};


const originalArray = [1, 2, 3, 4, 5];
const k = 3;

const rotatedArray = rotateArray(originalArray, k);
console.log("Original Array:", originalArray);
console.log("Rotated Array:", rotatedArray);

```

## Using IIFE function

```const rotateArray = (function (arr, k) {
  const n = arr.length;
  k = k % n; 
  const rotatedArray = arr.slice(k).concat(arr.slice(0, k));

  return rotatedArray;
});


const originalArray = [1, 2, 3, 4, 5];
const k = 3;

const rotatedArray = rotateArray(originalArray, k);
console.log("Original Array:", originalArray);
console.log("Rotated Array:", rotatedArray);

```

# 2nd Part of Task

## Using Arrow function solve the problems

## 1. Print odd numbers in an array

```
const odds = (array, arr) => {
  for (let i=0; i <= array.length; i++){
    if ( i %2 !== 0){
      arr.push(i);

    }
  }
  return(arr)

}
console.log(odds([1,2,3,4,5,6,],[]))

```
## 2. Convert all the strings to Title cap in a string

```
let string = (str) => {
  str = str.toLowerCase().split(' ');
  for (var i = 0; i < str.length; i++) {
    str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1);
  }
  return str.join(' ');
}
console.log(string("IT WAS A NICE DAY"))

```
## 3. Sum of all numbers in an array
  
  ```
  let array = (arr) => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum = sum + arr[i];
  }
  return sum;
  };
  console.log(array([1, 2, 3, 4]));

  ```
## 4. Return all the prime numbers in an array

```
const primeArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let isPrime = (num) => {
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
};
const numArr = primeArray.filter(function (num) {
  return isPrime(num);
});
console.log(numArr);

```
## 5. Return all the palindromes in an array 

```
const isPalindrome = (word) => {
  const reversed = word.split("").reverse().join("");
  return word === reversed;
};

const palindromes = words.filter(isPalindrome);

console.log(palindromes);

```


   






























