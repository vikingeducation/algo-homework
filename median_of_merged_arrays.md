##Median of Merged Arrays

You are given 2 sorted arrays of integers of the same size, *n*. Write a function, `medianOfMergedArrays()`, to find the median of the array obtained after merging the above 2 arrays into an array of length *2n*.

Try to do this with a time complexity of **O(log(n))**, i.e. better than linear time.

Here's a helper function to find the median of a sorted array.

```
var median = function(arr){
  var i = Math.floor(arr.length/2)
  if ( arr.length % 2 === 1 ) {
    return arr[i]
  } else {
    return ((arr[i-1] + arr[i]) / 2); 
  };
}
```
###Test cases

```
var arrA = [1];
var arrB = [2];
medianOfMergedArrays(arrA, arrB);
//=> 1.5

var arrC = [1,5];
var arrD = [2,4];
medianOfMergedArrays(arrC, arrD);
//=> 3

var arrE = [2, 3, 4];
var arrF = [1, 3, 5];
medianOfMergedArrays(arrE, arrF);
//=> 3

var arrG = [1, 2, 10];
var arrH = [2, 8, 9];
medianOfMergedArrays(arrG, arrH);
//=> 5

var arrI = [6, 10, 20, 25];
var arrJ = [1, 2, 3, 4];
medianOfMergedArrays(arrI, arrJ);
//=> 5

var arrK = [1, 5, 7, 10, 13];
var arrL = [11, 15, 23, 30, 45];
medianOfMergedArrays(arrK, arrL);
//=> 12

// It should work the same no matter which
// order the arrays are given.
medianOfMergedArrays(arrL, arrK);
//=> 12

```
