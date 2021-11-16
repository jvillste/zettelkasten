Could garbage collection be made controllable enough that thtere would not have to be separate programming languages for use cases where memory allocation is done manually and where garbage collector manges the memory?

One could allocate a memory area from the garbage collector and then run sub program that expects that memory to be stationary. After the sub program has finnished one could allow the gc to move the memory again as needed.

In Java such stationary meory is called "direct byte buffer". See [ByteBuffer](https://docs.oracle.com/javase/7/docs/api/java/nio/ByteBuffer.html).