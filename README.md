# Day4Task

Solve problems using Anonymous function and IIFE function
1. Print odd numbers in an array
   //Using Anonymous function
   const odds = function(array, arr) {
  for (let i=0; i <= array.length; i++){
    if ( i %2 !== 0){
      arr.push(i);
      
    }
  }
  return(arr) 
  
}
console.log(odds([1,2,3,4,5,6,],[]))

//Using IIFE function 
(function odds(array, arr) {
  for (let i=0; i <= array.length; i++){
        if ( i %2 !== 0){
           arr.push(i);
           
         }
       }
       console.log(arr)

})([1,2,3,4,5,6,],[])

2. Convert all the strings to Title cap in a string
   // Using 
