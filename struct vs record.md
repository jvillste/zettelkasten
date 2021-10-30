Encoding an entity consisting of fields can be done so that the schema is in band or out of band. See [Out-of-band data - Wikipedia](https://en.wikipedia.org/wiki/Out-of-band_data)

We use the terms struct and record to refer to these two encodings.

A struct has the attributes as type parameters, i.e. out of band. Record has attributes in the values i.e. in band.

A json object is a record because it can have arbtrary number of properties. A C -programming lanugage struct is a struct because the number and type of it's members is fixed in the type declaration i.e. out of band.