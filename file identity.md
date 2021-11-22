For synchronizing files between disks each file must have a stable identity.

From the file systems perspective a files identity is defined by it's serial number stored in the files inode. Even if the file is moved or it's contents are changed it's serial number is kept untouched. The same file can have multiple paths and names on the folder hierarchy.

# maintaining files identity over multiple inodes
The file agent may not be watching a folder tree while a user renames a file by first creating a new file, then copying the contents af the old file to the new file and then deleting the old file. The [[file management system]] could maintain the files identity over such changes.

The files identity is thus preserved even if the serial number and the contents change if the path stays untouched. Also when the serial number and path can change if contents are kept untouched.

There could be a treshold on how much the contents can change at the same time as the path and serial number changes. For example [Git](https://git-scm.com/)'s log command's parameter `--find-renames` let's the user  adjust the treshold by which a change is threated as a rename.

If two or more copies is made of a file and the original file is deleted, the file management system can not tell to which duplicate it should transfer the identity.