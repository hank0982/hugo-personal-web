---
title: "Code With Human - Programming"
date: 2020-12-01T21:53:31+08:00
draft: true
---
### **The evolution of programming language fits the need of human**
What is programming? At the beginning of computing, humans wrote the code to communicate with a machine. We have 101010101010000, then assembly code, then C, and now we got plenty of programming languages for us to chose from. The trend is that these modern languages are more like natural language and designed for programmers to write, read and communicate with each other. Some languages exchange performance for readability. Some languages constrain certain operations, such as directly controlling memory space, to prevent developers from writing harmful code, thus enhancing security.

Let us dive into a specific programming syntax used commonly in every single program: Loop.

I recall my first assignment written in FORTRAN. Professor asked us to write a program without modern loop operators like *while* / *for* / *do while* and function (procedure). We can only use *goto* to experience the difficulty of writing code in the old time. 

### **What is goto**

Imagine you are reading the article, and you see the keyword GOTO 111. No matter where you are looking now, you should turn to line 111 and read from that line.

Now, imaging you are the compiler (reader of programming languages), when you see "goto 111", you should find line 111, and execute the code from that line. 

Below is the example,

![GOTO](/images/goto.png)

>console.log is to print something on the screen.

The code is not precisely the syntax in JavaScript. However, I hope you can understand the meaning of that. When the computer reads the code, it reads from top to bottom. When it sees line 5, it will GOTO line 2 and continue. The final result of this program is
```
test
test
nice to meet you
```

Therefore, we could use this sort of mechanism to mimic modern loop operators. Now let's write a program to add from 1 to 100.
Below, the code snippet is written in FORTRAN-like syntax. You can see if the N is less than 100, the executor will run the code from line 3 to line 6 repeatedly, just like how modern loop operators perform.
![GOTO_MIMIC_LOOP](/images/fortran_goto.png)

"Oh~ that is easy." you might think. Good, let us see another example. Below is the code snippet from https://craftofcoding.wordpress.com/tag/spaghetti-code/, and the purpose of this program is to generate the formatted date. Enjoy the read and try your best to understand the code.

![GOTO_MIMIC_LOOP_UNSTRUCTURED](/images/doy_unstructured.jpg)

I bet you give up. Now, let us see a more user-friendly (developer-friendly) program that utilizes modern loop operators.

![GOTO_MIMIC_LOOP_STRUCTURED](/images/doy_structured.jpg)
I believe you will agree that the purpose and the structure of the program are much easier to be understood. Any junior developers could understand and modify the code easily.

### **GOTO is harmful **

Some computer scientists argue the usage of GOTO is bad. For instance, famous computer scientist Edsger Dijkstra criticized GOTO and published a letter: Go To Statement Considered Harmful. 
https://homepages.cwi.nl/~storm/teaching/reader/Dijkstra68.pdf

GOTO is easy to use and easy to write. However, when there are too many GOTO statements in the code, you have to frequently change your focus and quickly produce an unmaintainable spaghetti code. 

Understanding the negative impacts of GOTO, computer scientists came up with several structural statements like selection (if/else/then) or repetition (while/for) to improve code clarity.

