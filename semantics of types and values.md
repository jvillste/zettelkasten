A value type may have a structure of 32 bit unsigned integer and semantics of unix epoch. A single value of that type may have the semantics of being a birth time of a specific person.

Semantics of types are described in the file headers and semantics of values are described in the file body.

An example:
- **type**:  tupple
- **type instance**: two 16 bit floating point numbers
- **type instance semantics**: a coordinate pair
- **value semantics**: position of a specific car

In a struct or record (see [[struct vs record]]) the attributes specify the type level semantics of their values. A coordinate pair may be expressed as a struct with x and y attributes.