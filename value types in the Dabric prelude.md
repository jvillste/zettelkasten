## first order types
- unsigned integer: little endian integer of a fixed byte count. Supported byte sizes are 1,2,4,8. Note that the byte size is not a type parameter but the regular type size value given for every type.
- signed integer: twos complement liitle endian integer. Supported byte sizes are 1,2,4,8 
- unsigned leb128: a leb128 encoded unsigned integer
- string: utf-8 encoded byte size prefixed string
- type tagged value: a type tag / value -pair where the type tag is a VQL refering to the value type sequence in the file header

## higher order types
- array: a byte size prefixed sequence of values of a single type
- type tagged array: a byte size prefixed sequence of type tagged values
- tuple: fixed length sequence of fixed type values. Tuple type is parameterized with an array of types.
- struct: fixed length sequence of attribute values. Structs type parameters are a sequence  of attribute id / type -pairs. See [[length vs size]].
- record: a byte size prefixed sequence of attribute entity id, type tag, value triplets. See [[struct vs record]].
- type alias: a type definition along with an entity id that defines the meaning of the values. For example entity id (array of unsigned leb128:s), date (struct of year, month and day).

## named value type instances
Named value type instance is a value type that is parameterized with a type name as entity id and a value type reference and it's parameters.

Examples:

- entity id: a type alias for an array of VLQ:s where the first VLQ refers to a stream id in the file header
- epoch: a unix epoch as an unsigned leb128

## value attributes
Dabric prelude defines the following attributes to be used in structs and records:
- date time
	- year
	- month
	- day
	- hour
	- minute
	- second
	- millisecond