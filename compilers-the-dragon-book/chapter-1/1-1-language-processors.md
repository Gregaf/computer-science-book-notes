# 1.1 Language Processors

### Language Processor Types

- A compiler converts a _source language_ to a _target language_.
- An _executable machine-language program_ is run via supplied _input_ with corresponding _output_.
- An _interpreter_ is another language processor. Rather than producing a target program, the operations specified as _inputs_ are executed directly.

### Java Language Processors

Java language processors combine compilation and interpretation. The Java source program is first compiled into *bytecodes*, which is interpreted by a virtual machine. In some cases, Java *just-in-time* (JIT) compilers will translate the bytecodes into machine language (binary) prior to running the intermediate program.

### Large Program Compilation

Since source programs may be distributed among multiple files in modules; a separate program called a `preprocessor` may expand shorthands called macros, into source language statements.

> Relocatable machine code refers to object files, e.g. `<file_name>.o`  

The compiler may produce an assembly-language program as output. The generated assembly language is then processed by a program called an `assembler` that produces relocatable machine code as output. Large programs tend to be compiled into large pieces, thus the relocatable machine code must be linked together with other relocatable object files and library files into code that can be executed on the machine.

The `linker` resolves the external memory addresses where code in **file b** may refer to the location in **file b**. After the `linker`, the `loader` is responsible for placing all executable object files into memory for execution.

### Excercises
1. **What is the difference between a compiler and an interpreter?**
	A compiler will take in a source language and output to another language. An example of this is how `C` outputs `Assembly` that can them be processed by an `Assembler`. While an interpreter will take a source program (Python code) and any inputs provided to the source program and execute the source program along with the provided inputs generating output, *NOT* another language.

 2. **What are the advantages of:**
	 - **a: A compiler over an interpreter.**
	 - **b: An interpreter over a compiler.**

	a: Compilers have the following advantages over interpretters:
	- Faster program execution time since there is less overhead of executing and interpretting at the same time.
	b: Interpetters have the following advantages over compilers:
	- Improved debugging capabilities, as the source program is being executed directly.

3. **What advantages are there to a language-processing system in which the compiler produces assembly language rather than machine language?**
	A compiler that produces assembly is easier to generate and debug.

4. **A compiler that translates high-level language into another high-level language is called a source-to-source translator. What advantages are there to using C as a target language for a compiler.**
	An advantage of compiling to `C` as the target language would allow for the generated `C` code to be again compiled into `assembly` which would result in faster program execution times, also `C` is widely available, and thus can be compiled on most platforms (portability).

5. **Describe some of the tasks that an assembler needs to perform.**
	The assembler is responsible for translating `assembly` into relocatable machine code, this can be multiple relocatable machine outputs.


Online solutions found [here](https://dragon-book.jcf94.com/book/ch01/1.1/1.1.html)