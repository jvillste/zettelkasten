Dabric file has a header that consists of
- UTF-8 string "DABRIC" as a file signature
- file format version as a VLQ
- length prefixed sequence of 128 bit stream ids. Their position in the sequence are used in the entity ids later in the file. The length is expressed as VLQ and denotes the number of stream ids, not the combined byte count.
- value types as a sequence like stream ids above. Each value type consists of byte size / entity id pair. Byte size is expressed as a VLQ. Zero means the value will be length prefixed wih a VLQ. Entity id:s are encoded as byte size prefixed array of VLQ:s. The first vlq referes to a position in the preceding stream id sequence.

After the header comes the body as a type value pair.