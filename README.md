# FAT-32 (File System)

This code file allocates table, endieness as well as file access and implements a user space shell application that is capable of interpreting a FAT-32 file system image. <br />

## To run the code:

gcc mfs.c <br />
./a.out <br />

## How To Use

Once you are into the file system: <br />

open filename: <br />
This command shall open a fat32 image. Filenames of fat32 images shall not contain spaces and shall be limited to 100 characters.<br />
close: This command closes the fat32 image. If the file system is not currently open your program shall output: “Error: File system not open.” <br />
info: This command prints out the information about the file system in both hexadecimal and base 10 format. <br />

• BPB_BytesPerSec <br />
• BPB_SecPerClus <br />
• BPB_RsvdSecCnt <br />
• BPB_NumFATS <br />
• BPB_FATSz32 <br />

stat filename or directory name:
This command shall print the attributes and starting cluster number of the file or directory name.
If the parameter is a directory name then the size shall be 0.

get filename:
This command shall retrieve the file from the FAT 32 image and place it in your current working directory.

error:
Prints if the file or directory does not exist then your program shall output “Error: File not found”.

cd directory
This command changes the current working directory to the given directory.
Your program shall support relative paths, e.g cd ../name and absolute paths.

ls
Lists the directory contents. Supports listing "." and ".."

read filename, position, number of bytes
Reads from the given file at the position, in bytes, specified by the position parameter and output the number of bytes specified.

del filename
Deletes the file from the file system.

undel filename
Un-deletes the file from the file system.

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
