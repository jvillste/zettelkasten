Origins must be identified so that each entity descrbied by the origin has short but globaly unique identifier. It must also be possible to cryptographically identify the data that belongs to a given origin.

DNS and TLS provide a readily established way of reserving a global identity and proofing what data originates from a given identity.

Origins are thus identified with a domain name and UUID pair. The transaction log segments must be signed with a TLS certificate of the domain. The first transaction must specify the UUID and domain. Further transactions may specify a new domain to be used for signing, but the origin is always identified by the original domain and uuid pair.