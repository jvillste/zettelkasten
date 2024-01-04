Could single programming language support two different kinds of programming paradigms: dynamic typing, garbage collector and persistent data structures i.e. Clojure and static typing, manual memory management and mutable data structures i.e. C?

Could C like language be implemented as a macro in Clojure? The syntax would consist of the Clojure data structures but the code would be compiled to C like functions. This would be similar to embedding assembly code in C code.

C like languages are useful for algorithms that need high performance, but most applications require lot's of code for tasks that do not need the performance and would thus benefit from high abstraction level. Python is a good example of how slow, interpreted high level language is powerful when combined with high performance algorithms written in C.

Having a low level language be embedded in a high level language would make them co-operate as seamlessly as possible. Macros for example could be written in the higher level language. An example of this is the [Extempore](https://extemporelang.github.io/) language that uses Scheme for macros in a low level language.

	[jank](https://jank-lang.org/) seems to be an effort to this direction.

For a list of low level programming languages see [[c language alternatives]].