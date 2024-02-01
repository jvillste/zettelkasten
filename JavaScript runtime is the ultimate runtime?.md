Software should be able to run on Desktop, in the cloud and in the browser with minimal modifications. This can be achieved with:

- Desktop: ClojureScript with Electron
- Cloud: ClojureScript in Node.js based AWS Lambda
- Browser: ClojureScript as is

[[compiling Clojure to WASM|Compiling Clojure to WASM]] would get rid of the JavaScript compiler, but we would have to generate bindings to JavaScript libraries or switch to using libraries from other languages that compile to WASM. Of course the ClojureScript compiler could take care of the bindings generation automatically. It might make sense if ClojureScript would be evolving rapidly, but now as the language is already stable and the compiler works, there is not much advantage in switching from JavaScript to WASM.

Even if [[systems programming language embedded in a higher level language|Clojure(Script) would evolve to include systems programming characteristics]] that could be achieved simply by implementing those by generating WASM modules and calling them from the JavaScript emitted by the ClojureScript compiler. It may though be possible that such calls would be more efficient if also the current dynamic ClojureScript language would be compiled to WASM.

One big missing feature from JavaScript runtimes is multithreading. JVM is still more powerful in that respect. Compiling Clojure to WASM could solve multithreading in the browser although WASM modules have to use web workers just like javascript so maybe also ClojureScript could have some kind of multithreading implemented with web workers too.

Cider does not know how to run ClojureScript tests. This should be fixable.