Entity ids are sequencies. Related entities could share a common prefix. The last value in the sequence would be from the local entity id sequence to ensure uniquenes.

Entities could have "parent" -attribute and there could be entity, attribute, value (EAV) -index where the entity ids comprise of the parent id and entity id. EAV index is the only index where this proximity really matters.

Parent attribute values could contain all entity ids in the path to the root in the hierarcy. This way all entities in a hierrachical document would be next to each other in the EAV index.