Could single programming language support two different kinds of programming paradigms: dynamic typing, garbage collector and persistent data structures i.e. Clojure and static typing, manual memory management and mutable data structures i.e. C?

Could C like language be implemented as a macro in Clojure? The syntax would consist of the Clojure data structures but the code would be compiled to C like functions. This would be similar to embedding assembly code in C code.

C like languages are useful for algorithms that need high performance, but most applications require lot's of code for tasks that do not need the performance and would thus benefit from high abstraction level. Python is a good example of how slow, interpreted high level language is powerful when combined with high performance algorithms written in C.

Having a low level language be embedded in a high level language would make them co-operate as seamlessly as possible. Macros for example could be written in the higher level language. An example of this is the [Extempore](https://extemporelang.github.io/) language that uses Scheme for macros in a low level language.

	[jank](https://jank-lang.org/) seems to be an effort to this direction.

For a list of low level programming languages see [[c language alternatives]]. One approach would be to create an EDN based syntax for Zig or Odin and to compile that to Zig or Odin code. That would make sure that the battle proven patterns of static programming would be taken into use in this new programming language. The sole goal of this work would be to combine Clojure with static language with minimal friction between them.

Clojure's interoperability syntax shows one way of embedding statically typed language to dynamically typed language.

C# supports using manual memory management and disable array bounds checking for performance critical code:
[Possible to mix garbage collection and manual memory management?](https://langdev.stackexchange.com/questions/2956/possible-to-mix-garbage-collection-and-manual-memory-management)

# Making it embeddable
It should be possible to drop the runtime all together if the whole code base does not use GC. GC would possibly only be used on compile time for running macros.