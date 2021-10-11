When a compiler is compiled to wasm and has a wasm backend, any program can be run in a wasm sandbox by first compiling it there.

Applications can thus be packaged in a way that they can be run anywhere as long as they are implemented in a language that has compiler or interpretter that is compiled to wasm and can output wasm.

Web assembly system interface (WASI) still needs to be defined before wasm programs can access operating system services like files and sockets. Also a secure GPU interface like WebGPU is needed for graphical user interfaces.