Type tag is a one based index number that refers to type instances in the file header.

Typetag 0 means that the tag is followed by another type tag and the combination evaluates to a type instance rather than a value.

Example type instance definition header:
- type: *unsigned integer* size: 1 parameters: ()
- type: *array* size: 0 parameters: 0 1