---
title: A Gentle Intro to RISC-V
---

RISC-V is an open source hardware project started in 2010 at UC Berkeley USA 。As described by its official site https://riscv.org 

>RISC-V: The Free and Open RISC Instruction Set Architecture

Below is the longer version of this description, Let's find out what a Instruction Set Architecture , ISA for short, really means, how ISA is related to assembly languages, compilers and hardware implementations. We'll too cover RISC, and the differences between RISC-V and all the mainstream ISAs , say x86, ARM and so on.

## What an ISA Is

First thing first, what is a ISA?

Knowing what a Instruction is, is key to understand what ISA is, for short, an instruction is binary code in correspondence with a CPU operation. A computer architecture is largely determined by its ISA ，so there is an A in ISA, which stands for Architecture. The S in ISA stands for set. The character left, I, which means instruction, is not a day-to-day thing and deserves a bit explanation. The software logic we write in high level programming language needs to be translated into a sequence of CPU operations, for example, arithmetic or logical operations or memory I/O. And as we know, the only thing CPU can handle is Machine Language, that is the 0s and 1s. So it is obvious that one certain operation needs to be mapped to a binary code of some length, say 16 bit, 32 bit. Bit, for those who have no CS background, means a binary bit.

ISA is the interface between hardware and software. In order to be useful, ISA demands support from both sides. For the hardware side, a chip with the very ISA must be produced. For the software side, compiler support is a must, because different CPU architecture has different instruction for the same operation. In theory, given a ISA specification, we can program the CPU in machine language, even though nowadays nobody do this any more. What we do today is to code in high level languages, like C or Java, then let compiler translate the source code to binary. So if the ISA has no compiler support, it is out of the question to use the ISA for work.

To conclude so far, a instruction is a binary code mapped to a certain CPU operation, ISA is just a set of these things, ISA largely determines the CPU architecture, and it is the interface between software and hardware.

## What an ISA Is Not

Now that we are done with what an ISA is, let's make things even clearer by considering what an ISA is NOT.

First thing, an ISA is not a assembly language. Assembly language, asm for short, is a programming language, out of which the keywords are human readable English words or characters. While an ISA is a set of binary codes, 0s and 1s, so the distinction is very clear. And yes, asm is a so-called low-level language, most keywords have very direct correspondence with instructions.

Secondly, ISA is not a hardware implementation either. ISA is a abstract model for computers. For example, four wheels one steering wheel will make a abstract model for cars. So we can see, abstract model does not define the implementation. No matter a motor or engine inside, a car is still a car, and this don't change the way how people operate this car. Similarly, an ISA may have different hardware implementations. Intel and AMD both have CPUs with ISA of x86, but each have very different implementation, that's why the performance vary a lot. But, as long as both have the same ISA, the way people operation the CPUs with 0s and 1s remains the same. And for a vendor, if the implementation is upgraded but ISA is not, the corresponding compiler needs no modification.

So, the point is ISA is the interface between hardware or software. It is not an assembly language, because assembly language is within the realm of software, nor it is a hardware implementation specification, since it's don't put any constraint on the inner hardware logic.

## RISC-V vs x86 and ARM

Last thing, let's talk about the differences between RISC-V and other mainstream ISAs.

Let's begin by making the concept of RISC really clear. ISA has different categories, among which the main two are CISC and RISC. CISC stands for Complex Instruction Set Computer, x86, the ISA rules desktop computers, is of this category. RISC stands for Reduced Instruction Set Computer, and as the name implies, it removed the rarely used instructions out of CISC. ARM is a RISC ISA, that is the de facto standard for embedded device CPUs.

RISC-V is special with the virtue of being open and free of charge, that's why people call it the Linux for hardware. Project is maintained by the community, no patent fees is required to use RISC-V , with hardly any other sort of constraints.

RISC-V has built up a nice ecosystem. RISC-V foundation has a lot of big names as it members. Corporations support RISC-V as a mean to fight back the control of ARM and Intel. ARM and x86 are very complex nowadays due to the long history of commercial use, since backward compatibility is a must for them. On the contrary, being a new player, RISC-V has no such burden, that leads to a more concise set and really outstanding performance. Many hardware implementations for RISC-V are also open-sourced, and compilers like GCC and LLVM has good RISC-V support.

## Conclusion

That's all I want to share about RISC-V. The takeaways are, RISC-V is a instruction set, the interface between hardware and software. ISA determines how our code looks in its compiled binary form. Apart from the commercial ISAs like ARM and x86, RISC-V serves a great alternative being free and open.
