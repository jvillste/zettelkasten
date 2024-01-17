# Sources of complexity in programming
- there are many programming languages
- many calling conventions
- everything is based on c/c++ code
	- package management for c/c++ code is still not solved, although [Conan](https://conan.io/) seems promising.
- many CPU instruction set architectures
- many operating systems
# Solutions
- shared runtime such as .NET, JVM and WASM let different languages interoperate seamlessly and can provide virtual machine that can execute the same binary in all instruction set architectures and operating systems
- shared package management system such as Maven or NPM can serve multiple programming languages
- there is need for roughly two types of languages: static for high performance and dynamic for high abstraction level. Embedding [[systems programming language embedded in a higher level language | static language to dynamic language]] would serve both needs while minimising the friction between the two programming paradigms.