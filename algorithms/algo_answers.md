* Exercise I:
a) O(n) - because the program takes steps of n^2 to reach of n^3
b) O(logn) - beacuse program decrements in the size of i/2
c) O(sqrt(n)) - because O(sqrt(n)*8*8) = O(Sqrt(n))
d) O(nlogn) - bcz outer loop steps in multiple of 2 and inner loop is linear
e) O(n^3) - bcz there are 3 nested linear loops and the inner most is constant. 
Hence, O(10n^3) = O(n^3)
f) O(n) - because the recursion take place in steps of 1
g) O(n) - because the recursion take place in steps of 1


* Exercise II:
a) Algorithm:
1. find min value in the array
2. find max value in the array
3. find highest number on the right of minValue
4. find smallest value on the left of maxValue
5. now you have 2 pairs of numbers from 3 and 4
6. pick the pair with greater diff
example array: 4, 3, 9, 7, 8, 15, 6, 2, 4

 let maxValue1 = a[0], maxIndex = 0;
 let minValue1 = a[0], minIndex = 0;
 for(let i = 0; i < a.length; ++i) {
	if(a[i] > maxValue) {
		maxValue1 = a[i];
		maxIndex = i;
	} 
		
	if(a[i] < minValue) 
		minValue1 = a[i];
		minIndex = i;
 }
 let maxValue2 = a[minIndex], minValue2 = a[maxIndex];
 for(let i = minIndex+1; i < a.length; ++i) {
 	if(a[i] > maxValue2)
 		maxValue2 = a[i];
 }
 for(let i = maxIndex-1; i >= 0; --i) {
 	if(a[i] < minValue2)
 		minValue2 = a[i];
 }
 return (maxValue2-minValue1 > maxValue1-minValue2) ? maxValue2-minValue1 :  maxValue1-minValue2

 b) Algorithm:
We will have to use binary search like algorithm.
first drop egg from n/2 floor
if it doesn't break, go to higher floors and drop the egg
if egg breaks, go to lower floors and drop the egg
like binary search
eventually, you will find the floor f above which egg breaks and below which egg does not break


 * Exercise III:
 a) Time complexity will be O(n^2) in this case because at every step the left partion array is of size 0 while right partion array is of size (n-1), (n-2), ..., 1.

 b) Time complexity in this case will be O(nlogn) beacuse at every step the array is split into 2 partitions of almost n/2 size arrays. Hence there will be logn steps of quick sort and each step has O(n) time complexity.
