Examples of files are:
- photos
- drawings
- text files
- spreadsheets
- source code files
- saved games
- application settings
- TLS certificates
- cad models

Files are stored on disks. The same file may need to be stored on multiple disks to be shared between people.

Disks have folder structure. The same file may be stored on multiple folders on the same disk. Organizing files by tags may be more efficient than folders.

Accessing recently read or modified files should be easy. No mater on what disk they are stored or how they are organized with folders or tags.

Files may get modified over time and old versions should be kept accessible. This is because a file may get
- corrupted by a software bug
- accidentailly deleted by a user
- encrypted by ransomware

Files may get renamed or moved in the folder structure and that should not make it impossible to find old versions of the files.

Only changed parts of large douments should be stored when multiple versions of the same file are stored. See [[delta compressed blob storage]]

Finding files from multiple disks by their name, folder, tags or content should be fast.

The same file may be stored on multiple folders on the same disk by accident. Hash values of the file contents should be maintained to facilitate finding unneeded file duplicates.

Files should have copies on multiple disks so that no files are lost due to disk failure. Disks should be distributed over multiple apartments so that they can not be lost all at once by fire, water or theft.

It should be possible to filter out from backups downloadable files such as source code libraries or applications.

At any time a disk may be attached to a computer or it may be unmounted. Each computer may have multiple disks mounted. The computers could compare each others files and make copies to maintain redundant store of files. A user could search for a file and load it from a disk that is closest to the computer in use.

Changes to the files on a disk are monitored and metadata indexes updated in realtime. That way each disk can be compared and synced effieicently. Also indexes for finding files based on their modification time, file name and content are maintained.
