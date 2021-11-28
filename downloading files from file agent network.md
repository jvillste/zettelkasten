A usage scenario for the [[file management system]]:

A user could search for recent photos and see that an interesting photo is stored in a disk that is currently not mounted on any file agent in the network. His file agent knows this because it has downloaded the metadata of all folder trees in the network.

He knows that the disk is at his friends home and asks the friend to mount the disk on one of his computers. When the disk is mounted the user can download the file on his computer using the file agent running on his friends computer.

He does not have to synchronize a whole folder tree to get the file. The file is downloaded to a file name corresponding to the files stable, i.e. version independnet ID in the network. If he later synchronizes a folder tree containing that file, a new hard link is created pointing to the file, but the file does not have to be copied anymore.

If the file gets updated on one of the disks in the network, it get's synchronized to other disks in the network as agents connect to the network. There may be conflicts that need to be resolved by the users. The whole file does not have to be transfered since the file agents can transfer file versions as patches to other versions. The latest version is always kept in a specific inode and older versions are stored in other indoes as patches.