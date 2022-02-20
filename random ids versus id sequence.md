Should Dabric entity ids be big random numbers or numbers from a sequence?

If a single sequence is used and the branch shares the stream id of it's upstream, the branch's transaction log has to be rewritten when rebasing to shift new ids so that they start from the last upstream id. Random ids could be used as is.

Each branch could use different stream id and different entity id sequence.

Random ids must be big so that there is no collision between branches. Often used ids could be compressed away in the files. 

Reading and writing big numers would not be as ergonomic as with smaller numbers. In practice it would be sufficient to use a prefix of the whole number like when using git hashes. See [[identifier number size does not matter for storage space and readability]]

See [[how to maintain id sequences?]]