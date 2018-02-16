* Exercise I:
a) O(n)
b) O(logn)
c) O(3logn)
d) O(nlogn)
e) O(n^4)
f) O(n)
g) O(n)


* Exercise II:
a) 
let max = 0;
for(let i = 0, j = 1; i < a.length-1; ++i) {
	if(a[j] - a[i]) > max {
		max = a[j] - a[i];
	}
	++j;
}

 b) 