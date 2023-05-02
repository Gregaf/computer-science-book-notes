# 1.2 The Structure of a Compiler

A compiler at a high level maps a source program into a semantically equivalent target program. The idea of this mapping is broken into two parts, `analysis` and `synthesis`.

## Analysis
A source program is broken up into constituent pieces while imposing a grammatical structure on it and is then used to create an intermediate representation. It is responsible for detecting what is considered invalid or semantically unsound, then providing feedback for corrective measure to be taken.

This analysis is responsible for collecting information about the source program storing it into a `symbol table`. The `intermediate representation` and the `symbol table` are then handed off to the `synthesis` phase to be constructed. 

## Synthesis
