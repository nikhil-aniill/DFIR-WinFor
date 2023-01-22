[[Disk]]
[[Memory]]
Get evidence of both volatile and non-volatile data.
**Always Grab Memory first**

###### Memory
Click on the memory button on the top left corner and choose the attached storage device to dump the memory. 

###### Disk
Click on collect evidence item and choose physical disk. 
![[Pasted image 20230118160054.png]]
The root has the MFT records 

#### Creating Custom Image from the directories above
Added $Extend, $RecylcleBin, Users, $LogFile, $MFT, pagefile.sys, swapfile.sys, Windows.edb(Any windows search records), Amcache.hve(App Execution), setupapi.dev.log(USB), Hives - DEFAULT, SAM, SECURITY, SOFTWARE and SYSTEM, RegBack(backup of 5 hives), system32/LogFiles, /sru, NTUSER.dat, UsrClass.dat, *.evtx*, LNK(Using New in the Bottom Left Corner)Files, $I30. 

Click on Create Image in Bottom Left Corner