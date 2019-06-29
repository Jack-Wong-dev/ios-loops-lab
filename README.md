# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

```
swift
// Solution using a For-in loop
let rangeNum = 1...150

for i in rangeNum{  print(i); }


// Solution using a  Repeat-While loop
let rangeNum = 150
var num = 1

repeat {
    print(num)
    num+=1
}
while(num <= rangeNum)

```


***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

```
swift
let rangeNum = 1..<150

for i in rangeNum{  print(i); }
```


***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

```
swift
let someRange = 15...80

for i in someRange where i % 2 == 0{
print(i)
}
```



***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

```
swift
let someRange = 19...51

for i in someRange where i % 2 != 0{
    print(i)
}
```


***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**


```
swift 

let someRange = 1...<100
for i in someRange where i % 10 == 5{
    print(i)
}

```


***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

let someRange = 1..40

```
let someRange = 1...40

for i in someRange where i % 10 == 7{
    print(i)
}
```



***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

```
let someRange = 20...150

for i in someRange where i % 3 == 0{
        print(i)
    }
```

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`
```
let someRange = 20...150

for i in someRange where i % 3 == 0 && i % 2 == 0{
print(i)
}
```

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

```
let someRange = 20...150

for i in someRange where i % 10 == 4{
    print(i)
}
```

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

```
let someRange = 20...150

for i in someRange{
    if(i == 31 || i == 35 || (i >= 40 && i <= 60 )){
        print(i)
    }
}
```


***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
// Variable 'i' will always be greater than 3
// This is an infinite loop.  
// It'll keep going until the computer runs out of memory.

```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
```swift
//Solution
var i = 5

while (i <= 9) {
i += 1
}
```


***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
```swift
var i = 5
var counter = 0

while (i > 3 && counter < 1000) {
    counter += 1
    i += 1
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
```
//Solution
var i = 5
var counter = 0

while (i > 3 && counter < 1000) {
    
    if(i % 2 == 0){print(i)}
    
    counter += 1
    i += 1
}

```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```
In a while loop, the body is executed after the condition is true.
However, in a repeat-while loop the body if executed before checking the condition.

In this situation, the output will be the same.

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

The `break` statement stops the execution of a loop (or a switch) statement. It then jumps to the next statement following the loop or switch statement.

The `continue` statement stops the execution of statements inside a loop (or a switch) statement. It then jumps back to evaluate the loop's expression again.

// Example using break.

var x = 0

while(x < 10){
    if(x == 2){
        break       //program stops running once x==2
}
    print(x)
    x+=1
    }  // output should be '0' followed by '1' 



// Example using continue
while(x < 10){
if(x == 2){
x+=1
continue;   // 2 never gets printed
}
print(x)
x+=1
}  // Output should be '1', '3', '4', '5', '6', '7', '8', '9'



***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue     //goes to the beginning of the loop when i is 4 to 7
    }
    print(i)
}
```

[]1
[]2
[]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

This prints:
1
2
3
8
9
10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break       //Program terminates once i is 3
    }
    print(i)
}
```

[]1
[]2
[]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

This prints:
1
2
3
***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.



```
var N = 10
for x in 1...N {
for y in 1...N{
print("\(x),\(y)", separator: "", terminator: " ")
}
print("")
}
```


***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

```
var N = 10
for x in 1...N{
    for y in 1...N where x-y >= 5{
        print("\(x),\(y)", separator: "", terminator: " ")
    }
}
```


***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```
```
var N = 5

for i in 1...N{
    print(i*i)
}
```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```
```
swift
var N = 2

for _ in 1...N {
    for _ in 1...N{
        print("*", separator: "", terminator: " ")
    }
    print("")
}
```




Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```
```
swift
var N = 3

for _ in 1...N {
for _ in 1...N{
print("*", separator: "", terminator: " ")
}
print("")
}
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
