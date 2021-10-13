Dabric file has a header that consists of
- UTF-8 string "DABRIC" as a file signature
- file format version as a VLQ
- byte size prefixed sequence of 128 bit (16 byte) stream ids. Their position in the sequence are used in the entity ids later in the file. See [[byte size prefixed values]]
- byte size prefixed sequence of value type definitions.
	- Each value type definition consists of
		-  byte size as VLQ. Zero means the value will be byte size prefixed rather than of fixed length.
		-  Value type reference as entity id. See also [[value types in the Dabric prelude]]
		-  byte size prefixed sequence of type tagged parameters for the type. see [[type tag]]