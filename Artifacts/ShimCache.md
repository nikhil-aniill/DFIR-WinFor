#Application_Execution 
#Deleted_Items_File_Existence 
###### Information
The Windows Application Compatibility Database is used by Windows to  
identify possible application compatibility challenges with executables. It  
tracks the executable file path and binary last modified time.

Not all executables in the above screenshot are executed but might be just browsed through in the file explorer

The Shimcache stores any executables showed in the Explorer window(Even a sliver) through a USB on any network location. Even if the file is deleted the ShimCache still gets populated

Shimcache also stores last modified time of executables executed by the CMD

###### Location
It's located in the HKLM\\SYSTEM\\CurrentControlSet\\Control\\Session Manager\\AppCombatCache

###### Interpretation
Any executable present in the file system could be found in this key. Data  
can be particularly useful to identify the presence of malware on devices  
where other application execution data is missing (such as Windows  
servers).  
• Full path of executable  
• Windows 7+ contains up to 1,024 entries (96 entries in WinXP)  
• Post-WinXP no execution time is available
  Windows 7/8/8.1 had an execution flag that would indicate if the program ran.
  Windows 10 doesn't have that flag and doesn't show execution
• Executables can be preemptively added to the database prior to execution.  
The existence of an executable in this key does not prove actual execution.
- Only the modified time of the executable is stored on the shimcache, not the time it was added to the shimcache

**The Shimcache is only flushed to the disk on reboot or shutdown**

![[Pasted image 20230118092347.png]]