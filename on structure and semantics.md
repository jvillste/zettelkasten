Reading serialized data involves understanding how the data is broken down to individual pieces and what semantics do those pieces carry.

The reader may know that the data contains a 32 bit unisgned integer and thus knows how many bytes should be read and what primitive type in the used programming language should be used to store the value. This is structural understanding of the data.

The reader may further know that the number represents an instance in time encoded as seconds since the year 1970. Yet another level of understanding would be that the instance represends the birth time of a person.