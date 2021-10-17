For many applications the full history of the data is irrelevant. In such cases the indexes stored on disk can be nontemporal. Thus index segments on disk correspond to only single point in time. The in memory indexes must be temporal to make it posible to have consistent reads while the indexes are changing during query execution.

If there are indexes that depend on history of other indexes, then there might be need to store some history in the indexes on disk.

Also transaction log can be truncated after on disk index segments are written if the history is irrelevant. If transaction log is truncated then there must be an index that stores all statements to allow forming of new indexes without transaction log. Usually the entity attribute value -index serves that purpose.