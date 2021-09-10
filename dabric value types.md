# value types in the Dabric prelude
## first order types
- unsigned integer: little endian integer of a fixed byte count. Supported byte sizes are 1,2,4,8. Note that the byte size is not a type parameter but the regular type size value given for every type.
- signed integer: twos complement liitle endian integer of a fixed byte count. Supported byte sizes are 1,2,4,8 
- unsigned leb128: a leb128 encoded unsigned integer
- string: utf-8 encoded byte size prefixed string
- type tagged value: a type tag / value -pair where the type tag is a VQL refering to the value type sequence in the file header

## higher order types
- array: a byte size prefixed sequence of values of a single type
- tuple: fixed length sequence of fixed type values. Tuple type is parameterized with an array of types.
- struct: fixed length sequence of attribute values. Struct type parameters are a sequence  of attribute entity id / type -pairs. See [[length vs size]].
- record: a byte size prefixed sequence of attribute entity id, type tag, value triplets.
- type alias: a type definition along with an entity id that defines the meaning of the values. For example entity id.

## type aliases
- entity id: a type alias for an array of VLQ:s where the first VLQ refers to a stream id in the file header
- epoch: a unix epoch as an unsigned integer

## value attributes
Some values are encoded as structs or records and use attributes defined in the Dabric prelude.
- date time
	- year
	- month
	- day
	- hour
	- minute
	- second
	- millisecond

# how to specify atomic and record value types in the dabric file header?
A value type definition in the dabric file header starts with a byte that tells wether an atomic value type definition or a record type definition follows. Atomic value type definition consists of byte size as VLQ and an entity id. Record definition consists of a byte size prefixed sequence if attribute entity id / atomic value type definition pairs.

# Could record be just a parameterized value type?