At first it seems that it would be worth to start a new id sequence for identifying entities child entities. If for example a document has entity id `[12345]`, then a paragraph in the document would have for example id `[12345, 3]`.

To make this work, whe would have to maintain separate id sequences for each entity that has child entities. This could mean for example that each transaction log file would include the next available id numbers for each parent entity.

For example if each one of the six million english wikipedia pages had it's paragraphs as child entities of the page, there would have to be the six million next available child id numbers in each transaction log file.

Having small child entity id's would thus have a high price in complexity and space efficiency. It also turns out that smalle numbers are not that valuable: [[identifier number size does not matter for storage space and readability]]