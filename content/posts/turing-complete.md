---
title: "The Art of Turing Completeness."
date: 2022-11-08T21:45:11-06:00
draft: false
tags: [programming]
---

Us programmers, we like to show off our stuff. Doing hard or downright unrealistic things. For example: porting doom to every system imaginable, [making full fledged 3D games in 96 kb of memory](https://en.wikipedia.org/wiki/.kkrieger), or what we are going to be talking about today: making everything Turing complete.


## What is Turing completeness?
To fully comprehend Turing completeness, we need to understand what a Turing machine is. A Turing machine is a theoretical machine that can compute *anything* that is computable. In technical terms, it is an array of memory with a single pointer to an element of that array. We can increment and decrement both the pointer and the element that the pointer is pointing to.

The key thing to understand about Turing machines is that they can compute ***anything***. Sure, not effectively, but if we can implement a Turing machine into a programming language (or as you'll soon find out, many more things than programming languages), then we can compute anything that is computable.

## How do we make something Turing complete?
To make something Turing complete, we need to implement a Turing machine. This can be done in so many ways, that I can't even begin to list them all. But we are just going to go over one of the most popular ways to do it: Brainf*ck. 

Brainf*ck is the worlds worst programming language, no contest. But, it is also the closest thing to a Turing machine that we can get to in a programming language. It has a 30000 cell array, and a single cell pointer. You can move the pointer left and right, increment or decrement the cell pointed to, or loop a section of code until a cell is 0, and print and read from the console. Thats it. No if statements, No OOP, Not even any built in multiplication. The language (as the name implies) makes your brain hurt.

A simple hello world program looks like this:

```
>++++++++[<+++++++++>-]<.>++++[<+++++++>-]<+.+++++++..+++.>>++++++[<+++++++>-]<+
```

YIKES! But, it works. And it works because it is Turing complete. It can compute anything that is computable. So, theoretically we could create cures for cancer, or make a fully fledged operating system. That's the fun in creating stuff that's Turing complete. You can do anything with it.

## What have we made that is Turing complete?

We have many programming languages that are Turing complete. Javascript, C++, Python, and many more. If you name a prominent programming language, I'd bet my liver that it is Turing complete. However, we have made so many more things that are Turing complete.

Minecraft is theoretically, Turing complete. People have made computers on Minecraft, and given enough memory, we could theoretically run Minecraft on Minecraft. Heck, [somone's done it already!](https://youtu.be/-BP7DhHTU-I) Granted, it's not the actual Minecraft game, just a faithful recreation of it. But it's still mindblowing.

What about not using computers? What if we just used water? [Steve Mould created a video in which he made logic gates out of water](https://youtu.be/IxXaizglscw), and then used those logic gates to make a computer. While it's not a turing machine, and is a 4 bit adder, we can use these water gates to create a Turing complete computer

## Conclusion

The idea of Turing completeness is what attracts programmers to making stuff Turing complete, not the actual output. I didn't make a [Brainf*ck interpreter](https://github.com/tatewilhelm/brainfrick) because I loved watching fibbonacci numbers print to the console. I made it because I wanted to make something that was able to something dumb, like a crappy language mostly used as a joke, and make it able to calculate *literally anything.* It's not the destination, it's the journey. And the journey is what makes Turing completeness so fun.

