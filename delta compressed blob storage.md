Dali needs a blob storage with delta compression and content based addressing.

There should be these file types in the blob storage:

- base: the actual content as is, named by hash of the contents
- delta: a change to another delta or a base. Named by hash of the change and references.
- compound: a sequence of references to base and one or more deltas. Addressed by hash of the contents of the resulting value when the deltas are applied.

This structure makes all of the files cacheable as they have stable content based names.

It allows optimizing the storage without changing the names: a compound can be replaced with a base or different sequence of deltas without changing it's name.

Compound lists all the required deltas so that the client can figure out which deltas it does not yet have and retrieve them parallerly or using a singe api call.

# How to differentiate compounds from bases?

When a client asks for content corresponding to a hash, it must know if it got a compound or a base.

If the fiels are served from S3 bucket or some other non customized http server then there are two options:
- the url does not differentiate between compounds and bases, but the files start with a byte that tells the type of the contents.
- compound and base urls differ and the client has to first query one of them and if it does not exist, query the other.

If a customized Dali server is used it can return either compound or a base in a single api call and also mark the content type using response headers.

# Splitting large files

Large files could be split to deltas if that makes sense for a p2p protocol. This could be handled by the p2p protocol without being addressed on the blob storage level though.