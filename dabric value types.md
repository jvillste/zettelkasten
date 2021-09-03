# value types in the Dabric prelude
- type tagged value: a VQL refering to the value type sequence in the header followed by the actual value
- value array: byte size prefixed sequence of type tagged values. The type tags are VLQ:s that refer to positions in the value type sequencei in the file header.
- entity id: a byte size prefixed value sequence in which the first value is a VLQ that referes to the stream id sequence in the file header and the following values are local entity ids encoded as VLQ:s.
- attribute dictionary: a byte size prefixed sequence of entity id and type tagged value pairs.

# how to specify atomic and record value types in the dabric file header?
A value type definition in the dabric file header starts with a byte that tells wether an atomic value type definition or a record type definition follows. Atomic value type definition consists of byte size as VLQ and an entity id. Record definition consists of a byte size prefixed sequence if attribute entity id / atomic value type definition pairs.

# Could record be just a parameterized value type?