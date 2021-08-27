In a Dabric file values are often prefixed with a number that tells how many bytes the following value takes. This way the file can be parsed even if the readers does not know how to interpret some of the values. The byte count is always expressed as a [[Variable length quantity]] (VLQ). This kind of values are called here "byte size prefixed".

Dabric file has a header that consists of
- UTF-8 string "DABRIC" as a file signature
- file format version as a VLQ
- byte size prefixed sequence of 128 bit stream ids. Their position in the sequence are used in the entity ids later in the file.
- byte size prefixed sequence of value type definitions.
	- Each value type definition consists of byte size / entity id pair. Byte size is expressed as a VLQ. Zero means the value will be byte size prefixed rather than of fixed length.
	- Entity id:s are encoded as byte size prefixed array of VLQ:s. The first vlq referes to a position in the preceding stream id sequence.

After the header comes the body as a type value pair.