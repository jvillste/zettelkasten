When a program is compiled and linked, the dependencies between compilation modules need to be met. There can be conflicts between the dependencies of the modules.

Possible solutions to dependency conflicts are:
- pick one version and hope that it works with the modules that depend on a different version
- raise the granulairity of dependencies to function level to avoid conflicts
- allow linking to multiple versions of the same function at the same time

The function signature may be incompatible between different versions of the same function. Even with static typing different versions of the function may behave differently in an incompatible manner. Only tests can tell if the specific version of the called function works as expected.

If the function has side effects, they may be incompatible between function versions even if the function signature remains the same.

Modules could have automatic tests that are run after the linking. This should be done any time a new combination of dependencies is linked. This would make security patching more stable.

One could specify the exact code that is run on a function call by giving the hashes of the compiled versions of all the functions that the called function depends. Those compiled functions could be stored in a key value store so that one could load only the exact bytes that are needed for running the function. The compiled functions should be [Position-independent code](https://en.wikipedia.org/wiki/Position-independent_code). Jumps between functions need more resolving at link time if the code is loaded one function at a time instead of larger units at a time.

One can refer to a function implementation in different stages of compilation:
- source code
- intermediate machine indpendent language
- machine code

If one is serious about testing, the testing should be done with the exact machine code that will be run in production.

Joe Armstrong elaborates on this here: [Why do we need modules at all?](http://lambda-the-ultimate.org/node/5079)
