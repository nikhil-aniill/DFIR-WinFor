#Disk MFT or $MFT can be considered one of the most important files in the NTFS file system. It keeps records of all files in a volume, the files' location in the directory, the physical location of the files in on the drive, and file metadata. The metadata includes file and folder create dates, entry modified dates, access dates, last written dates, physical and logical file size, and ACLs of the files. The file and directory metadata is stored as an MFT entry that is **1024 bytes in size**.

Record header consists of a number for each file and flags to show if the file is in use or has been not in use. MFTs are not deleted but just overwritten.

$DATA contains the fragments of the file (if it’s small) or if the file is large, consists of pointers to the allocated spaces on the disk.

Records begin with ASCII string "FILE" and bad records start with ASCII "BAAD"

![[Pasted image 20230118150257.png]]
The Red highlighted line is encoded in Windows 64-bit FILETIME structure 
[[$FILE_NAME]]
[[$STD_INFO]]