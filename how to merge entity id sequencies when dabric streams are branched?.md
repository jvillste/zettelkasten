If dabric streams can be branched and merged, there must be some way of merging the entity id sequencies also.

Each branch keeps track what was the last entity id before forking the branch. All allocated entity ids after that are concidered temporary ids and are assigned the actual ids when the branch is merged back to the parent stream.