A user could search for recent photos and see that an interesting photo is stored in a disk that is currently not mounted on any file agent in the network. Hes file agent knows this because it has downloaded the metadata of all folder trees in the network.

He knows that the disk is at his friends home and asks the friend to mount the disk on one of his computers. When the disk is mounted the user can download the file on his computer using the file agent running on his firends computer.

He does not have to synchronize a whole folder tree to get the file. The file is downloaded to a generic folder structure based on the hash value of the file contents. If he later synchronizes a folder tree containing that file a new hard link is created pointing to the file, but the file does not have to be copied anymore.

If the file gets updated on one of the disks in the network, it get's synchronized to other disks in the network as agents connecto to the network. There may be conflicts that need to be resolved by the users. The hole file does not have to be transfered since file verions are stored as patches to the previous version.