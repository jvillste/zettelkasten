Stateful components need to have identifiers if they are part of a sequence that may change. Otherwise the GUI framework does not know how to map component states to the scene graph nodes.

React gives a warning if elements in a sequence do not have unique keys.

Reagent puts the keys into the html element properties like this: `[:div {:key :some-unique-key}]` or as a metadata `^{:key :some-unique-key} [some-component]`

In fungl the scenegraph nodes are just maps so ids can be given with assoc: `(assoc (some-visual) :id :some-unique-key)`. Stateful components must be vectors that start with a function. The node id could come before the function: `[:some-unique-key some-component]`