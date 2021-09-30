# Requirements

* Branching / merging
* Live editing the same DB by multiple people
* Inter database references
  * Globaly unique ids
* Merging databses
* Read scalability
* ACID transactions

# Solution

Datomic like databse that can be branced and merged like git repositories.

The database is an asyclic graph of transactions. Each transaction points to one or more parent transactions. One transaction is the root transaction that has no parents.

Transactions specify statements that specify changes to the edges of a graph of `[entity attribute value]` -tuples.

# Statement

* a statement is `[command entity attribute value]` -tuple
* a command is one of
  * add
  * retract
  * set ( sets the new value as the only value of the attribute

# Transaction

* consists of:
  * ordered list of parent transaction hashes
      * Parent branches are applied in the specified order when the transactions are threated as description of a graph.
  * A set of statements
  * Depth: the distance to the root transaction when all of the parent transactions are listed in the specified order. Used in the indexes to order statements.
  * hash of all other fields
* Transaction can be refered to by it's hash to add metadata in another transaction
* A special entity id "transaction" can be used to add metadata about the transaction in the same transaction

Example:

~~~
  [[set 1 name foo]
   [add transaction transact-time 12345]]
~~~

# Root

* A transaction with no parents.

# Leaf

* A transaction with no children.

# Edge

* `[entity attribute value]` -tuple

# Path

* An ordered list of transactions between two transactions.

# Fork

* A transaction that has more than one children.

# Merge

* a transaction that has more than one parent.

# Parent ordering

* The order of parents of a merge.

# Trunk

* The transactions on a path where only the first parent are traversed for each merge.

# Branch

* A path from a non first parent of a merge to the first fork.

# Full path

* A path that spans all of the parent transactions from a transaction to the root transaction. The parents of a merge are traversed in reversed parent ordering.

# Depth

* The length of a full path of a transaction.

# Full path depth

* The distance to the root from a transaction on some full path.

# Graph

* a set of edges that are specified by applying all of the statements in all of the transactions of a full path.


## EATVC index

