# Sources of complexity in programming
- there are many programming languages
- many calling conventions
- everything is based on c/c++ code
- dependency management for c/c++ code is not solved
- many CPU instruction sets
- many operating systems
# Solutions
- shared runtime such as .NET and JVM let different languages interoperate seamlessly
	- WASM:s shared garbage collector does this for languages that compile to wasm?
- shared package management system such as Maven or NPM can serve multiple programming languages
- there is need for roughly two types of languages: static for high performance and dynamic for high abstraction level. Embedding [[systems programming language embedded in a higher level language | static language to dynamic language]] would serve both needs while minimising the friction between the two programming paradigms.