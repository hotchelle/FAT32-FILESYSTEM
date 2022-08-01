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

## Commands to try
| Command | Description |
| ----------- | ----------- |
| open &lt;FAT32 image name&gt; | Opens the inputted FAT32 disk image |
| close | Closes the currently open FAT32 disk image |
| info | Prints out information about the loaded file system in both decimal and hexadecimal |
| stat &lt;file name / directory name&gt; | Prints out attributes and starting cluster number of inputted folder/directory |
| get &lt;file name&gt; | Retrieves file from FAT32 image and places it in current working directory  |
| cd &lt;directory path&gt; | Change directory  |
| ls | Lists files in current directory |
| read &lt;file name&gt; &lt;position&gt; &lt;# of bytes&gt; | Prints out n bytes of the inputted file to console from the inputted starting position |
| del &lt;file name&gt; | Deletes inputted file name from current directory |
| undel | Undeletes last deleted file |
