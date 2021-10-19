When a program is compiled and linked, the dependencies between compilation modules need to be met. There can be conflicts between the dependencies of the modules.

Possible solutions to dependency conflicts are:
- pick one version and hope that it works with the modules that depend on a different version
- raise the granulairity of dependencies to function level to avoid conflicts
- allow linking to multiple versions of the same function at the same time

The function signature may be incompatible between different versions of the same function. Even with static typing different versions of the function may behave differently in an incompatible manner. Only tests can tell if the specific version of the called function works as expected.

If the function has side effects, they may be incompatible between function versions even if the function signature remains the same.

See [Why do we need modules at all?](http://lambda-the-ultimate.org/node/5079)
