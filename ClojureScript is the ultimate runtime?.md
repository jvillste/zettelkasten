Software should be able to run on Desktop, in the cloud and in the browser with minimal modifications. This can be achieved with:

- Cloud: ClojureScript in Node.js based AWS Lambda
- Browser: ClojureScript as is
- Desktop: ClojureScript with Electron

[[compiling Clojure to WASM|Compiling Clojure to WASM]] would get rid of the JavaScript compiler, but we would have to generate bindings to JavaScript libraries or switch to using libraries from other languages that compile to WASM. That would make sense if ClojureScript would be evolving rapidly, but now as the language is already stable and the compiler works, there is not much advantage in switching from JavaScript to WASM.

Even if [[systems programming language embedded in a higher level language|Clojure(Script) would evolve to include systems programming characteristics]] that could be achieved simply by implementing those by generating WASM modules and calling then from the JavaScript emitted by the ClojureScript compiler. It may be though possible that such calls would be more efficient if also the current dynamic ClojureScript language would be compiled to WASM.