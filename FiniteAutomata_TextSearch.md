# Applications of Finite Automata in Text Search and Pattern Matching

**Author:** Jass Sangale  
**Department:** Cyber Security, Shah & Anchor Kutchhi Engineering College  

---

## Introduction

In the world of computer science, efficiently processing and analyzing text is a fundamental requirement. One of the core tools that makes this possible is the **Finite Automaton (FA)**. Finite Automata are abstract mathematical models used to represent and recognize patterns in strings. They play a vital role in areas such as text search, compiler design, lexical analysis, and even network security.

Finite Automata can be broadly classified into two types:

1. **Deterministic Finite Automata (DFA):** Each state has exactly one transition for each possible input symbol.  
2. **Non-Deterministic Finite Automata (NFA):** States can have zero, one, or multiple transitions for the same input symbol.  

Despite their theoretical nature, these models have real-life applications that directly impact the efficiency of modern computing systems.

---

## Core Concepts

### Deterministic Finite Automata (DFA)

A **DFA** is defined by a 5-tuple `(Q, Σ, δ, q0, F)` where:  

- `Q` = finite set of states  
- `Σ` = finite set of input symbols (alphabet)  
- `δ` = transition function (`Q × Σ → Q`)  
- `q0` = start state  
- `F` = set of accept (final) states  

The DFA reads a string symbol by symbol and moves between states according to the transition function. If it ends in an accept state, the string is **accepted**; otherwise, it is **rejected**.

### Non-Deterministic Finite Automata (NFA)

An **NFA** is similar to a DFA but allows multiple transitions for the same input symbol or even transitions without any input (ε-transitions). NFAs are often easier to design for complex patterns, but every NFA can be converted into an equivalent DFA for implementation.

### Example DFA Diagram

Below is a simple **DFA** that recognizes the binary string `"101"`:

```mermaid
stateDiagram-v2
    [*] --> q0
    q0 --> q1: 1
    q1 --> q2: 0
    q2 --> q3: 1
    q3 --> [*]
