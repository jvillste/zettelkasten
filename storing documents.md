Examples of documents are:
- photos
- drawings
- text files
- spreadsheets
- source code files
- saved games
- application settings
- TLS certificates
- cad models

Documents are stored on disks. The same document may need to be stored on multiple disks to be shared between people. 

Disks have folder structure. The same document may be stored on multiple folders on the same disk. Organizing files by tags may be more efficient than folders.

Accessing recently read or modified documents should be easy. No mater on what disk they are stored or how they are organized with folders or tags.

Documents may get modified over time and old versions should be kept accessible. This is because a document may get 
- corrupted by a software bug
- accidentailly deleted by a user
- encrypted by ransomware

Documents may get renamed or moved in the folder structure and that should not make it impossible to find old versions of the documents.

Only changed parts of large douments should be stored when multiple versions of the same document are stored. See [[delta compressed blob storage]]

Finding documents from multiple disks by their name, folder, tags or content should be fast.

Documents should have copies on multiple disks so that no documents are lost due to disk failure. Disks should be distributed over multiple apartments so that they can not be lost all at once by fire, water or theft.

It should be possible to easily filter out from backups easily downloadable files such as source code libraries or applications.