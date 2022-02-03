Entities in Dabric stream have an id and the stream describes their state as statements. See [[values represent the state of an entity]]

Entity value does not have an id. It describes a single entity state as attribute value pairs. The attributes are entities and are referred with entity ids like normal entity attributes. Entity values are stored in indexes like other values such as strings and numbers. For ordering in the index they are compared as ordered sequences of attribute value pairs.

An example of an entity value is internationalized string that has two attributes: the language and the string. It could be efficiently stored as struct in dabric files. See [[struct vs record]].

Entity values may contain other entity values and thus form a hierarchical document just like a JSON file. The biggest difference to a JSON file is that attributes are encoded as entity ids rather than strings.

An entity value may be transformed into entities by giving unique entity ids for each entity value in the hierarchy.

Representing hierarchical documents as entity values rather than entities has the advantage that all entities stay in one place in the EAV index. The downside is that any change in the value results to entirely new value in the index. Although compression can be applied easily because the different versions of the document follow each other in the index file. See [[how to keep related entities close to each other in indexes?]]