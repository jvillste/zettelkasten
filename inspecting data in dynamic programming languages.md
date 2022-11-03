When reading programs written in dynamically typed programming languages one does not have a type system that tells what properties a given variable has. There are several approaches for inspecting the values stored in a given variable while running the code for example by executing a unit test.
- pringing the values
- using a debugger
- saving the values as global variables. This is called "inline deffing" in Clojure. Down side of this is that you need to find names that do not collide with other variables or functions.
-  [vvvvalvalval/scope-capture: Project your Clojure(Script) REPL into the same context as your code when it ran](https://github.com/vvvvalvalval/scope-capture) saves all variables in a given scope and then defines them in the namespace with the local names so that one can evaluate expressions inside a function while having the local scope available. 
-  one could use tracer such as:
	-  [Cyrik/omni-trace: Omnipotent/omniscient tracing and debugging for clojure(script)](https://github.com/Cyrik/omni-trace)
	-  [clojure/tools.trace: 1.3 update of clojure.contrib.trace](https://github.com/clojure/tools.trace)
-  A tracer could save function parameters during a test run and then the IDE could provide tooling for inspecting values that a function parameter under the cursor contained.

Here is a list of relevant tools for Clojure: [Clojure observability and debugging tools](http://www.futurile.net/2020/05/16/clojure-observability-and-debugging-tools/)