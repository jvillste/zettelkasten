Reasons for implementing wasm backend for clojure compiler:
- To be able to run the exact same language on the server and on the browser. In theory the same could be achieved by a cljc library that implements javascript and java API:s that are now in common use in clojurescript and clojure code.
- It might be that clojure programs compiled to wasm would start up faster because there would be no JVM class loading.

To make a WASM backend to the clojurescript compiler we need to replace emit functions in the [compiler](https://github.com/clojure/clojurescript/blob/master/src/main/clojure/cljs/compiler.cljc) for example using [wasm.cljc](https://github.com/helins/wasm.cljc).

To make the compiler development interactive in the clojure repl we could run the resulting wasm modules with [wasmer-java](https://github.com/wasmerio/wasmer-java) or [wasmtime-java](https://github.com/kawamuray/wasmtime-java). Wasmer and Wasmtime are still lacking GC though. V8 has wasm GC, but it's not clear wether it's Java bindings [Javet](https://github.com/caoccao/Javet) or [J2V8](https://github.com/eclipsesource/J2V8)support running wasm. Calling J8 directly using the Java's new [Foreign Function & Memory API](https://openjdk.org/jeps/442) could work also.

We need to implement low level functionalities such as the big integers and string manipulation which are inherited from java and javascript in clojure and clurescript. We could use c or rust libraries for those.

Developing a [[systems programming language embedded in a higher level language|lower level language]] with the Clojure syntax interactively in Clojure repl could be a nice experience also.