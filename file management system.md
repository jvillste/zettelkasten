File management system is a set of software tools that help [[managing files]]

It allows incremental storage of files which means that no data is deleted unless otherwise requested. Deleted files and previous file versions are kept on disks and synchronized between multiple local and remote disks to maintain high durability.

Finding files based on their metadata from multiple computers and disks is made easy. Visualizing the state of the files such as used storage space and amount of file duplicates is provided so that the user can get confidence that the files are kept safe.

Sharing files over a network is not in the scope of the file management system. File sharing systems such as [Samba](https://www.samba.org/) and web servers like Apache may be used for that. File management system focuses on organizing the files and keeping them backed up on multiple disks.

# terms
- **file** has these attributes inode id, path, creation time, modification time, contents as a sequence of bytes
- **folder** is a container of folders and files. It has a path.
- **folder tree** is all the folders and files under a given folder
- **file agent** is a service that manages folder trees on disks mounted on a computer. It may be run as a background process that runs constantly or it may be used as a command line tool for running one of commands such as comparing or synchronizing two folder trees. It
	- maintains metadata indexes for a folder tree
	- serves metadata indexes through an API
	- keeps files encrypted on disk if requested
	- maintains old file versions that are stored outside of the folder tree
	- sends files to other file agents to keep folder trees syncronized if requested by the user
	- receives files from other file agents
	- file agents must securelly identify each other and users and encrypt all communication
- **metadata indexes** are files that allow efficient queries on the metadata of files and folders in a folder tree for the purpose of finding files and synchronizing folder trees.
	- The indexes may be implemented as a Dabric stream
	- The indexes can be updated in real time by listening to changes in the tree or by enumerating the whole tree at once. Making changes to a folder tree without an angent watching it must be supported.
- **file agent network** comprises of all file agents that syncronize files among each other
- **file client** is a program that lets a user to
	- find files by their metadata
	- add new folder trees to be watched by a file agent
	- specify how much verison history is maintained for files
	- specify what folder trees should be kept synchronized