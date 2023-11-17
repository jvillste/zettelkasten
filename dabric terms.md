* value: a single literal value such as a number, a string or a keyword
* row: a finite ordered sequence of values
* statement: a row consisting of entity id, attribute and value
* operator: "add" or "remove"
* index: ordered set of rows. All rows in an index are of the same length.
* change: a row and an operator. The operator tells wether the row should be added or removed from the index.
* datom: a row that ends with a transaction number and an operator
* temporal index: ordered set of datoms
* column: all values in a certain position in rows in an index
* column name: an identifier that uniquely identifies a column in an index

# indexes
* source indexes are written directly
* derived indexes are defined by source indexes
* statement index has columns :entity, :attribute and :value
* relation index has arbitrary columns

# transactions
* transaction: transaction number and a set of changes consering a specific index
* transaction log: a sequence of transactions consering a specific index
* monotonic transaction log: a transaction log where all the changes contain only adds and no removals.
