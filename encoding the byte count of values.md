The byte count of a value type instance may be encoded in these ways:
# primitive values
- **fixed length:** Each value has the same length. For example 32 bit float.
- **length prefixed:** Each value is prefixed with the length of the value. For example a variable length string.
- **terminated:** The value ends with a terminator byte sequence. For example null terminated strings.
- **implicit length:** The length is encoded in the same bytes as the value itself. For example LEB-128 where each byte has one bit that designates wether the value continues on the following byte.
# collection values
- **fixed value count:** For collection values the count of contained values can be fixed. The reader must know how to decode the length of each contained value. For example an entity ID in a file could be an array of two VLQ:s. The first denoting a stream declared in the file header and the second denoting the local entity id.
- **value count prefixed:** A collection value is prefixed with the count of values in the collection. For example a record may have arbitrary number of attribute value pairs and that number may be given as a prefix to the value. See [[struct vs record]].
- **terminated collection:** A collection may be terminated with a specific value.

The number of different length encodings used in Dabric files should be limited for simplicity. Length prefixed values could be the only supported encoding, but that would make it unreasonably inefficient to serialize for example lots of fixed length numbers. Also encoding entity ids as a pair of VLQ:s should be supported because it is so common.

It may seem that using terminator values would save space, but because the size of a langth prefix is logarithmic to the length this is not true unless there are lots of big values. See [[identifier number size does not matter for storage space and readability]]. Using a terminator would be useful if the value must be streamed to a channel and it's size is not known beforehand. Supporting terminated values should be optional.