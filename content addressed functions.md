When a function is compiled to machine code, machine the code could be stored in a [[delta compressed blob storage|blob storage]] where the blob would be referenced by the hash value of it's contents. If the compiled code is [[programming language agnostic functions|language agnostic]] it could then be called from any programming language. A machine independent intermediate language like WASM could be used to make the function even more universally applicable. See [[universal sandbox]].

In theory the same function could be implemented in different programming languages and result in the same intermediate language code and thus have the same hash value. In practice the optimization would propably result in different implementations in different languages.

[The Unison language](https://www.unisonweb.org/) is based on this concept.