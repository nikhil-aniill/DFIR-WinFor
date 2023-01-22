#Disk Refers to Modification, Access, MFT Record Change and Birth

Read about the MFT and the $STD_INFO and $FILE_NAME from Notion. There is a detailed description about the $MFT Record and it's structure consisting of Record Header, $STD_INFO, $FILE_NAME and $DATA (If the file is small)

Time stomping happens when changes are made to the $STD_INFO, and is changed to an ancient time and is behind the $FILE_NAME MACB time stamps. **SI<FN**

$FILE_NAME macb time stamps can only be changed by the Windows Kernel

**When a file is deleted, none of the MACB values are changed**

###### Why doesn't Access change the macb
	This is because of the key in HKLM hive called the HKLM/SYSTEM/CurrentControlSet/Control/FileSystem/NtfsDisableLastAccessUpdate