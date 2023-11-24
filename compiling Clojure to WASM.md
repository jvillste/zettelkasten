To make a WASM backend to the clojurescript compiler we need to replace emit functions in the [compiler](https://github.com/clojure/clojurescript/blob/master/src/main/clojure/cljs/compiler.cljc) for example using [wasm.cljc](https://github.com/helins/wasm.cljc).

To make the compiler development interactive in the clojure repl we could run the resulting wasm modules with [wasmer-java](https://github.com/wasmerio/wasmer-java). Wasmer [does not seem to have](https://github.com/wasmerio/wasmer/issues/357) GC yet though.

We need to implement low level functionalities such as the big integers and string manipulation which are inherited from java and javascript in clojure and clurescript. We could use c or rust libraries for those.

Developing a [[systems programming language embedded in a higher level language|lower level language]] with the Clojure syntax interactively in Clojure repl could be a nice experience also.