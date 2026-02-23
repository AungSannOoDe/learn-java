# Introduction to Programming

## What is Programming?

Programming is the process of writing instructions that tell a computer how to perform specific tasks. These instructions are written in programming languages and translated into a format that the computer's hardware can understand.

In simple terms:

> Programming is the way humans communicate with computers to solve problems.

Programming is used in:
- Web development
- Mobile applications
- Game development
- Artificial Intelligence
- Operating systems
- Business and banking systems

---

## How Computers Understand Programs

Computers do not understand human language.  
They only understand **binary numbers (0 and 1)**.

All programming languages are eventually converted into binary instructions before the computer executes them.

Programming languages are generally divided into:

1. High-Level Languages
2. Low-Level Languages

This document focuses on **Low-Level Programming**.

---

# Low-Level Programming

Low-level programming languages are closer to computer hardware.  
They provide direct control over memory, CPU registers, and system resources.

There are two main types of low-level programming languages:

- Machine Code
- Assembly Language

---

## 1. Machine Code

Machine code is the lowest-level programming language.

It consists entirely of binary numbers (0s and 1s) and is directly executed by the CPU.

### Example:
10101010 00001111 10101010


Each processor architecture (such as x86 or ARM) has its own machine code format.

### Advantages
- Very fast execution
- Direct hardware control
- No translation needed (executed directly)

### Disadvantages
- Extremely difficult for humans to read
- Hard to debug
- Not portable between different CPU architectures

---

## 2. Assembly Language

Assembly language is a human-readable representation of machine code.

Instead of binary numbers, it uses short keywords called **mnemonics**.

### Example:
MOV AX, 5
ADD AX, 3

Assembly code must be converted into machine code using a program called an **assembler**.

### Features
- Very close to hardware
- Uses CPU registers
- Architecture-specific

### Advantages
- Faster and more efficient than high-level languages
- Precise control over memory and hardware

### Disadvantages
- Harder to learn than high-level languages
- Not portable
- Takes more time to develop large programs

---

# Comparison

| Feature | Machine Code | Assembly | High-Level Language |
|----------|--------------|----------|---------------------|
| Readability | Very Hard | Hard | Easy |
| Speed | Very Fast | Fast | Moderate |
| Hardware Control | Full | High | Limited |
| Portability | No | No | Yes |

---

# Conclusion

Programming allows humans to instruct computers to perform tasks.

Low-level programming (Machine Code and Assembly) gives deep control over hardware but requires strong technical knowledge.

Understanding low-level programming helps build a strong foundation in computer science and improves problem-solving skills.
