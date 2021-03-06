Functions in different programming languages could be compiled so that they can call each other like if they were written in the same language. The return value and parameter types must be mapped to the native types of each language.

The PHP str_rot13 function that takes utf-8 string and returns utf-8 string could be called from a C program.

There could also be common garbage collection runtime so that different languages could operate on the same values in managed memory. If the languages use separate GC implementations the values must be copied.

There could also be common unamanged memory area so that data could be passed by reference between separate language runtimes and runtimeless languages.

Interoperable types could be described and serialized with [[value types|dabric value types]].

See also [[universal sandbox]].

For practical existing approach to language interoperability see [Simplified Wrapper and Interface Generator](http://www.swig.org/)