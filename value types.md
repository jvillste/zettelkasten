Data in Dabric streams consists of values. In order to process the data, a program needs to know how to map the values into the programming language's native types and types defined in code libraries.

The values in a stream are encoded in a way that their byte count is always known. Thus if a program does not know how to map a value to a known type, it can always threat the value as a byte array.

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
- array

# value type parameters
Value types may have parameters. Value type along it's parameters is called value type instance.

Byte size is the only value type paramter that is given for all value types. Value types may support only certain byte sizes. For example Dabric arrays are always variable size. i.e. the values are prefixed with their byte count. Unsigned integers defined in the Dabric prelude support only byte sizes 1,2,4 and 8.

Examples:
- array has one value type as a parameter. All values in the array are of that type.
- integers do take only the byte size parameter and only support certain byte sizes.