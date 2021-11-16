Functions could operate on dabric types and call functions accross langauge and runtime boundaries in the same process.

Ready made mappings between common dabric types and various programming language types could be implemented so that interoperability could be achieved without any library specific effort.

Single process could run multiple runtimes for different programming languages. A Perl function could call Java function that takes a byte array and returns utf-8 encoded string. The program would have to start the Java runtime before making the call. The same program could call another Java function from a different Java version standard library by loading two Java runtimes into the same process.

The processes could be run in a [[universal sandbox]] that could run various language compilers and runtimes on multilple hardware architectures. A [[low level cloud infrastructure]] could be used to coordinate the processes.

Language specific package management tools could be replaced by a genereic blob storage or content distribution network or p2p network. See [[delta compressed blob storage]].

See [[combining managed and unmanaged memory]].