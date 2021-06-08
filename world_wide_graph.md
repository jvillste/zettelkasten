# World Wide Graph

## File web

Git repositories served over http or simpler protocol.

## Data web

Datomic databases in file web.

Text documents as graph. Code as graph.

Graph databases represented as sorted sets of quads:
  * subject
  * predicate
  * object
  * transaction
  
Each graph has a globaly unique id.
Graphs have versions that are identified by a hash of the contents.
Graphs can refer to each other by graph id and entity id.
