Programming languages are often developed by adding features along the way as seen fit while using the language. Designing the language around low level abstractions such as sequences and sets might result in more consistent and thus easier to understand langauge.

Clojure tries at least at this point in time be more thoughtful in adding new features. For example if some function works for one kind of data structure, it should work for all datastructures for which it makes sense.

We could collect abstractions and algorithms from existing languages and find a core language that has small but coherent set of functions around fundamental abstractions.

Similar approach could be used to define langauges for other domains other than programming. For example we need a language for describing argumentation for [[online_argumentation]]. At first, if there are no good examples of such langauges it may be useful to just start modelling and inventing the language on the way. But the end goal should be to find minimal, coherent and comprehensive set of language constructs. Removing features from a language is as important as removing repetition and dead code from computer programs.