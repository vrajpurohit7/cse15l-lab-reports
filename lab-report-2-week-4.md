# *Changes made in the code to fix a bug*

## 1) Including print statement:
Faliure inducing input: [Test file 1](https://github.com/vrajpurohit7/markdown-parser/blob/main/test-file.md)

The above test file causes an infinite loop to run:
![Image](2-infinite-loop.png)

We solved the issue by adding a print statement:
![Image](labreport1.png)

Adding this print statement helped check how the current index was changing and thus help figure out what caused the infinity loop.

## 2) Adding an if-statement:
Faliure inducing input: [Test file 2](https://github.com/vrajpurohit7/markdown-parser/blob/main/testfile2.md)

The above test case causes an Index out of Bound error:
![Image](2-if-statement-error.png)

We solve this issue by including an if-statement:
![Image](labreport2.png) 

This monitors the indexs and doesn't let the code give an out of bound error.

## 3) Addresing invalid links:
Faliure inducing input: [Test file 3]()

The above test file caused wrong printing of the links:
![Image](2-invalid-link.png)

We solved this issue by implimenting a for loop and if statements:
![Image]()

These lines made sure that any invalid links are not being added and printed out as the results.