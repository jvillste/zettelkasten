`{:tags [:programming-languages] :draft true}`

# Homoiconic runtimeless programming language

## The problem

C is a small language that does not need a runtime. It is thus easy to use C programs from programs written in other programming languages. C's syntax is not as malleable as Lisp's syntax. Lisp needs a runtime because it has garbage collection. A runtimeless language that would have a Lisp like homoiconic syntax would be useful.

Homoiconicity makes it possible to have a macro system that let's the language to be extended by macros written in the language itself. 

## Links
* [Extempore](https://extemporelang.github.io/) is a statically typed language without garbage collection that has macros written in Scheme
