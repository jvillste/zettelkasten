Data in Dabric streams consists of values. In order to process the data, a program needs to know how to map the values into the programming language's native types and types defined in code libraries.

The values in a stream are encoded in a way that their byte count is always known. Thus if a program does not know how to map a value to a known type, it can always threat the value as a byte array.

See [[value types in the Dabric prelude]]

# value type parameters
Value types may have parameters. Value type along it's parameters is called value type instance.

Byte size is the only value type paramter that is given for all value types. Value types may support only certain byte sizes. For example Dabric arrays are always variable size. i.e. the values are prefixed with their byte count. Unsigned integers defined in the Dabric prelude support only byte sizes 1,2,4 and 8.

Examples:
- array has one value type as a parameter. All values in the array are of that type.
- integers do take only the byte size parameter and only support certain byte sizes.

# kinds of value types

## first order value types
These types define values that are atomic in the sense that they do not consist of multiple values.

Examples:
- unsigned integer
- utf-8 encoded string
- jpeg image

## higher order value types
These types define values that consist of multiple values.

Examples:
- array: variable length sequence of values of certain type
- struct: fixed length sequence of attribute values

# named value type instances
Some value type instances may need further specification on how the values should be interpreted. Such type instances may be given an entity id by with they are refered to. This entity id is called the name of the type instance.

A 32 bit integer is just a number, but it may be typed with a named type instance that declares that it represents a unix epoch.

A struct instance with the fields year, month and day may be parsed into a hashmap, but if it has a name that declares that it represents a date, it could be parsed into a date object defined in a time management code library.
