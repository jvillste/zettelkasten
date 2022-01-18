When inspecting entities that are closely related to each other, such as entities comprising a hierarchical document, it would be inefficient to have the entities spread out in multiple files in the  entity, attribute, value (EAV) -index. We should find a way to keep related entities close to each other in the index so that when the document is viewed, hopefully only one file has to be downloaded.

# Hierarchical entity ids
Entity ids could be sequencies. Related entities could share a common prefix. This is like Datomic partitions. The last value in the sequence would be from the local entity id sequence to ensure uniquenes. This would make entity ids larger in indexes that are not ordered primarily by entity. When the entity is first introduced, the parent must be fixed. Entities could not move in the hierarcy later on.

# Parent attribute and EAV index ordered by parent hierarchy
Entities could have "parent" -attribute and there could be separate EAV -index where the datoms would start with a sequence of entity ids in the parent hierarchy.

The index file could compress the id paths because consequent datoms in the index have similar paths.