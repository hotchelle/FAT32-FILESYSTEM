# FAT-32 (File System)

This code file allocates table, endieness as well as file access and implements a user space shell application that is capable of interpreting a FAT-32 file system image. <br />

## To run the code:

gcc mfs.c <br />
./a.out <br />

## Commands List
| Command | Description |
| ----------- | ----------- |
| open &lt;FAT32 image name&gt; | This command shall open a fat32 image. |
| close | Closes the opened FAT32 disk image |
| info | Prints out information about the file system |
| stat &lt;file name / directory name&gt; | This command shall print the attributes and starting cluster number of the file or directory name.|
| get &lt;file name&gt; | This command shall retrieve the file from the FAT 32 image and place it in your current working directory.|
| cd &lt;directory path&gt; | This command changes the current working directory to the given directory.|
| ls | Lists the directory contents. Supports listing "." and ".."|
| read &lt;file name&gt; &lt;position&gt; &lt;# of bytes&gt; | Reads from the given file at the position, in bytes, specified by the position parameter and output the number of bytes specified. |
| del &lt;file name&gt; | Deletes the file from the file system. |
| undel | Un-deletes the file from the file system. |
