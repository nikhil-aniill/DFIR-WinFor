#Disk
[[$STD_INFO]]

Journaling is a NTFS specific feature for file system integrity done in event of a crash. In the NTFS meta files in the image in FTKImager, there are two important journals - One being the $Logfile (tracks changes in the NFT and metadata) and the other one being the USNJournal

### USNJournal
- Updates sequence number or tracking change journal at a higher level
- The information might only last days to weeks on busy system
### LogFile
- Located in volume root
- Tracks detailed low level changes to NTFS
- May last only hours to days on a primary boot drive
![[Pasted image 20230118181900.png]]

in `$Extend→$UsnJrnl`
```
$Max

$J
```
In the $j parsed csv output, deleteme file was created and deleted. The timestamps are shown in the output

the usnjournal will have data that goes for a few weeks or days depending upon the usage of the machine.

### Tools to Parse
TRIFORCE ANJP
-  Export the journals with FTKImager
-  On cmd run `attrib` and you'll see that it's hidden
-  `attrib -s -h <FileName>`
- Load the file paths into ANJP and Hit parse
- In the Reports Tab, Hit connect and review the reports

The same can be carried out with Kape and MFTEcmd by the using the File System Module