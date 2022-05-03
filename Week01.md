# core-code-from-scratch-readme



## Tuesday 
* Create an explanation about interpreted And Compiled programming Languages 

For starters it's necessary to understand that most languages can have both but they tend to work better with one. Each one have their own ways to manipulate the written code in order to let the computer understand and process the code. To make ourselves clear of what it's the difference between them we'll use two scenarios to see the process. 
In the first scenario we have a code that it's written in a compiled language, first we need to translate every line of code with a compiler and then create a separate code that it's now translated, this new code it's what be call an executable file. 

In the other scenario we have a code that we want to run so we handle to the other person a copy ofthe code, with the help of a interpreter we translate a line and execute it and repeat the procces for each line until we reach the end of the code. 

* Is Java compiled or interpreted, or both? 

We can determine that Java is both a compiled and an interpreted language, it mainly depend on our execution environment. We use Java language to code, then a compiler create a file with bytecode, then that file it's going to be either translated by another compiler or it's going to be  executed by an interpreter.

* Pseudocode exercise 
>For this exercise will be getting the valu of the two variables because bitcoin fluctuates 

 START
amount<--GET

bitcoinReferenceInDollars<--GET

bitcoinConvertion<-- amount/bitcoinReferenceInDollars

PRINT bitcoinConvertion

END

* High and low level languages 


Since our tech devices only understand binary and binary it's very complicated for us to write code, so, we had to find a way to make ourselves able to communicate with the device and then the first language created was an intermediate between us and the PC. That first language was assembly language that was less close to our human way of communicate, it had some reserved words and symbols.
That first language is part of what we call low level languages
Low level languages are called that way because it's a low abstraction of machine language, it means that the language it's pretty close to machine language.
In the other hand we have high level languages that are closer to the way we communicate, by that we mean that it has it's own rules and grammatic.

## Wednesday

* Your date of birth in the matrix? exercise
As we learned, in binary we only use 1's and 0's so we can use different methods to make the convertion od a decimal number into a binary one. First we need to know that every digit of a number has it's own weight and to determine the weight we number each position and we use it as an exponent and  we elevate a base 2 with the current exponent or position, the very last number has a position 0 which means that has a 2^0 weight 

Know to make ourselves clear we can convert 2000 which is the year I was bornt. We can use different methods to convert it.
 1. Method 1:

Here we need to list some of the values that we can get with different exponents when we calculate power of two, we need to stop listing when we reach a number that it's bigger than the one we are going to convert, we only need those that are less than the number.
2^0 =1
2^1 =2
2^2=4
2^3=8
2^4=16
2^5=32
2^6=64
2^7=128
2^8=256
2^9=512
2^10=1024 
2^=11= 2048
> We'll stop here, the las number we'll use is 1024 because is less than 2000

We'll substract from 2000 the power of two that it's close to it, the result will follow the same process repeatedly until we reach 0
2000-1024=976 <-- Here we used 2^10

976-512=464 <--9

464-256=208 <--8

208-128=80<--7

80-64=16<--6

16-16=0<--4

We got the numbers that are going to have the value of 1, the ones we didn't use will remain as 0.

 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 
 -- | -- | - | - | - | - | - | - | - | - | - | -
 0  | 0  | 1 | 1 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 



 2. Method 2:

We can divide the number by two, the result will repeat the process until we reach 0 as the quotient, for each division will take note of the remainder because those are te digits that are our result

Division | Quotient | Remainder
-------- | -------- | --------
2000/2   | 1000     | 0
1000/2   | 500      | 0
500/2    | 250      | 0
250/2    | 125      | 0
125/2    | 62       | 1
62/2     | 31       | 0
31/2     | 15       | 1
15/2     | 7        | 1
7/2      | 3        | 1
3/2      | 1        | 1
1/2      | 0        | 0

now we take the remainders from bottom to top and that it's our convertion

* MIPS
 ``` Javascript
   .data
        name: .asciiz "\nElena Lopez\n"
  .text
        main:
              li $v0, 4
              la $a0, name
              syscall
   ```
   
## Thursday
1. Bad code
The given exercise was to find the error in the code, in order to write the answer the bad code will be commmented and then the solution will be written.
```javascript
var cond = false;

if ((cond = true)) { // it's not making a comparison so, the conditional it's not responding
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```
The solution to fix the bug:
```javascript
var cond = false;

if ((cond == true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```
2. Bad code 2
Solution:
``` Javascript
var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
else if (n < 1000 && n % 10 == 0 ) {
  console.log('');
} else {
  console.log('Just a regular number');
}
```
3. Print special numbers
```javascript
for(let num=0 ; num <100; num++){
  if(num%2!=0){ console.log(num);}
}
```
