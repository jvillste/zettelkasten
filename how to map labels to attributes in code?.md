When programming application one needs to model the domain by introducing attributes. If the data model is EDN or JSON, the attributes do not need to be declared beforehand. They can just be used in the data.

The attribute ids are specific to each dabric stream. The same program could store data in multiple dabric streams using the same attributes. Thus there must be a mapping from the labels to attribute ids for each stream. This is similar how names in a Terraform file are mapped to resource ids when an existing infrastructure is imported to Terraform state.

Intoducing attribute entities in dabric stream is done in serialized transactions, so there can be no conflicts.
