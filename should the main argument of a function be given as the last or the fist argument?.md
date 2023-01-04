If the main argument of a function comes last, we can use partial application to provide the other arguments to produce a function that only takes the main argument.

If the main argument comes first, we can provide optional arguments after the required arguments.

If we would have partial aplication that provided the other arguments except the first one, we could have optional arguments and still be able to use partial application to form a function that only takes the main argument. In clojure this could be called "partial-last".