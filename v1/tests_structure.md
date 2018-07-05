Tests Structure
===============

When adding assignments, you must provide a zip file containing test cases. This zip file should contain a folder for each problem (Upload-Only problems don't need any folder). Folder names should be `p1`, `p2`, `p3`, …

There are two methods of checking output for each problem: “Input/Output Comparison” method and “Tester” method:

Input/Output Comparison method
------------------------------

In this method, you must put some input and output files in the problem's folder. Online Judge gives each test's input file to user's code and compares user's output with the test's output. Input files must be in folder in with names input1.txt, input2.txt, … and output files must be in folder out with names output1.txt, output2.txt, …

Tester method
-------------

In this method, you must provide some input test files and a C++ file (tester.cpp) and (optionally) some output test files. Online Judge gives the input test file to user's code and gets the user's output. Then tester.cpp gets test's input, test's output and user's output. If the user's output is correct, returns 0, otherwise returns 1.

You can use this code template for writing tester.cpp:

```cpp
/*
 * tester.cpp
 */
 
#include <iostream>
#include <fstream>
#include <string>
using namespace std;
int main(int argc, char const *argv[])
{
 
	ifstream test_in(argv[1]);    /* This stream reads from test's input file   */
	ifstream test_out(argv[2]);   /* This stream reads from test's output file  */
	ifstream user_out(argv[3]);   /* This stream reads from user's output file  */
 
	/* Your code here */
	/* If user's output is correct, return 0, otherwise return 1       */
 
	...
 
}
```

Sample File
-----------

You can find a sample tests file in Assignments folder of Online Judge.

The tree of this file is:

```
.
└── p2
    ├── in
    │   ├── input1.txt
    │   ├── input2.txt
    │   ├── input3.txt
    │   ├── input4.txt
    │   ├── input5.txt
    │   ├── input6.txt
    │   ├── input7.txt
    │   ├── input8.txt
    │   ├── input9.txt
    │   └── input10.txt
    └── out
        ├── output1.txt
        ├── output2.txt
        ├── output3.txt
        ├── output4.txt
        ├── output5.txt
        ├── output6.txt
        ├── output7.txt
        ├── output8.txt
        ├── output9.txt
        └── output10.txt
```


Problem 1 uses “Input/Output Comparison” method for checking output. So it has two folders `in` and `out` containing test cases.