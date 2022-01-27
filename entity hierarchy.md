Entities could have "children" -attribute and there could be separate hierarchical EAV -index where the datoms would start with a sequence of entity ids in the hierarchy. The EAV index could leave out entities that have a parent to save space.

The hierarchical EAV index file could compress the id paths because consequent datoms in the index have similar paths.