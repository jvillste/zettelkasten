Functions in different programming languages could be compiled so that they can call each other like if they were written in the same language. The return value and parameter types must be mapped to the native types of each language.

There could also be common garbage collection runtime so that different languages could operate on the same values in managed memory. If the languages use separate GC implementations the values must be copied.

There could also be common unamanged memory area so that data could be passed by reference between separate language runtimes and runtimeless languages.

Interoperable types could be described and serialized with [[value types|dabric value types]].

See also [[universal sandbox]].