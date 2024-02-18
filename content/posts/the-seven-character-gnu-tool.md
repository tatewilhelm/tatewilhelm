---
title: "Making a 7 Character GNU Tool."
date: 2022-07-11T11:37:27-06:00
draft: false
tags: [programming, cli]
---

In most programming languages, there's a trade off between efficiency, and ease of use. It's a spectrum of the two, for example, C would be on the efficiency side, and Javascript would be on the ease of use side. But both are usable for making large programs, there's only a few languages you can think of so effecient that it is barely usable for the average programmer. You may have in mind x86 assembly, Fortran, or another archaic language. But I present to you: BrainF*ck. (I'm gonna call it BrainFlock, just to keep my website PG.)

Like the silly name, BrainFlock, is a silly language. It's the closest to a Turing Machine a language can get. It contains a 30000 cell array, and a single cell pointer. You can move the pointer left and right, increment or decrement the cell pointed to, or loop a section of code until a cell is 0, and print and read from the console. Thats it. No if statements, No OOP, Not even any built in multiplication. The language (as the name implies) makes your brain hurt.

A simple hello world program looks like this:

```
>++++++++[<+++++++++>-]<.>++++[<+++++++>-]<+.+++++++..+++.>>++++++[<+++++++>-]<+
+.------------.>++++++[<+++++++++>-]<+.<.+++.------.--------.>>>++++[<++++++++>-
]<+.
```

Yeah, hurts to read, doesn't it?

As you can probably tell, this language was not created for actual use. You're not gonna program the next unix-like operating system in BrainFlock, obviously. Good luck writing a boot loader in BrainFlock.

Since BrainFlock is a joke, literally. Theres is barely any good interpreters out there, besides those crappy web interpreters that you have to copy to from VSCode, so I created a BrainFlock interpreter, transpiler, and compiler, all in one program, called BrainFrick.

> Just to clarify, because it gets confusing: BrainFlock is my substitute name for the language, BrainFrick is the actual program I made.

BrainFrick is the software equivalent of taking a joke seriously. BrainFrick has a built in interpreter, transpiler to 2 different languages, and a compiler to create actual machine executables. 

So now that we have a compiler, we can create a *GNU tool* with BrainFlock. `cat` is the perfect program to recreate. It's very easy, but still is useful.

So the `cat` tool can be recreated with this:
```
+[>,.<]
```

Now don't run `sudo rm /usr/bin/cat` yet. There are some limitations. It can't read files, due to BrainFlock's limitations, and it doesn't have a help menu or MAN page. But it functions the same as when you type into cat.

That's only a basic program in BrainFlock, there are tons more that are way more complex. For example: [Linus Akesson's implementation of Conways Game of Life](https://www.codegrepper.com/code-examples/whatever/game+of+life+brainfuck). This program is slow when being interpreted, but thanks to BrainFrick's compiler, this work of art runs almost instantly.

Overall, I like BrainFlock. Not because it's a easy language, or has the most up to date features (it hasn't been updated since its creation), but because of how hard and unuseful it is. Because, as a programmer, making things harder and unuseful is what we do.

