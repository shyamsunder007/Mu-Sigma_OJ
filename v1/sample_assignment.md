# Sample Assignment

Here is a sample assignment for testing Online Judge. Add this assignment by clicking on `Add` in `Assignments` page.

## Problems

This assignment has three problems:

### Problem 1 (Max):
  
Read integer n, and then read n integers. Print sum of the two largest numbers between these n numbers.

| Sample Input      | Sample Output |
| ----------------- | ------------- |
| 7<br/>162 173 159 164 181 158 175  | 356           |

## Tests

Tests follow [this structure](tests_structure.md).

You can find the zip file of the tests in Assignments folder.

The tree of this file is:

    .
    ├── p1
    │   ├── in
    │   │   ├── input1.txt
    │   │   ├── input2.txt
    │   │   ├── input3.txt
    │   │   ├── input4.txt
    │   │   ├── input5.txt
    │   │   ├── input6.txt
    │   │   ├── input7.txt
    │   │   ├── input8.txt
    │   │   ├── input9.txt
    │   │   └── input10.txt
    │   ├── out
    │   │   ├── output1.txt
    │   │   ├── output2.txt
    │   │   ├── output3.txt
    │   │   ├── output4.txt
    │   │   ├── output5.txt
    │   │   ├── output6.txt
    │   │   ├── output7.txt
    │   │   ├── output8.txt
    │   │   ├── output9.txt
    │   │   └── output10.txt   
    │   └── Problem1.pdf
    └── SampleAssignment.pdf

## Sample Solutions

### Sample Solution for problem 1:

#### C

```c
#include<stdio.h>
int main(){
	int n , m1=0, m2=0;
	scanf("%d",&n);
	for(;n--;){
		int k;
		scanf("%d",&k);
		if(k>=m1){
			m2=m1;
			m1=k;
		}
		else if(k>m2)
			m2=k;
	}
	printf("%d",m1+m2);
	return 0;
}
```

#### C++

```cpp
#include<iostream>
using namespace std;
int main(){
	int n , m1=0, m2=0;
	cin >> n;
	for(;n--;){
		int k;
		cin >> k;
		if(k>=m1){
			m2=m1;
			m1=k;
		}
		else if(k>m2)
			m2=k;
	}
	cout << (m1+m2) << endl ;
	return 0;
}
```
