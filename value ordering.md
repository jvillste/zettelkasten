Values are ordered by their byte representation. Earlier bytes have higher precedence. Shorter values come before longer values.

When values of different types are compared, their type entity ids are compared instead of the values.

Order of fields in structs and records define struct and record ordering. By default fields are ordered by their attributes entity id. Attributes may have a weight value that is used instead of entity id if both compared attributes have it. Attributes with the same weight are ordered by their entity id.