It must be possible to cryptographically authenticate the data that belongs to a given stream.

Each change in the stream is identified by a hash value of the contents of the change and the hash of the previous change. To authenticate the whole stream, the reader must obtain the hash value of the latest change from a trusted source. This will most likely be done with an API call to a trusted domain over TLS, but the hash value could be read from a hand written note if that's preferred.

This same mechanism is used in the git version management tool. Each commit in git is refered by the hash of the commit object's contents including the hash of the previous commit.

Note that the hash values of the changes identify a specific state of the stream, but each stream also has a stable identifier. See [[dabric stream identity]].

The dabric api should provide the hash value for each transaction number in the stream to make it possible to authenticate only a part of the stream without computing the hash value of the latest state of the stream.

Also see [[dabric index authentication]]

# using signatures instead of API

If there is no API that could provide the hash values corresponding to stream states, digital signatures could be used instead. The stream segments or even individual changes in the stream could have attached signatures. The authenticity could then be validated by validating the signature instead of retrieving a hash from an API.