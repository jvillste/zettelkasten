Shifted integer is a parameterized type for storing integers that all must be offsetted by some value.

These could be used to efficiently store transaction numbers in truncated index segments even if the transaction numbers are big. Only the offset from the first stored transaction must be stored in the datoms.

Other usecase would be epoch timestamps in a file. See: [[using custom offset for millisecond precision unix epoch is not worth it]]

