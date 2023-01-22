#Deleted_Items_File_Existence 
### Description  
The recycle bin collects items soft-deleted by each user and  
associated metadata—only relevant for recycle-bin aware  
applications.

### Location  
Hidden System Folder  
• Win XP: C:\Recycler  
• Win7+: C:\$Recycle.Bin

### Interpretation  
• Each user is assigned a SID sub-folder that can be mapped to a  
user via the Registry  
• XP: INFO2 database contains deletion times and original filenames  
• Win7+: Files preceded by $I###### contain original filename and  
deletion date/time  
• Win7+: Files preceded by $R###### contain original deleted file  
contents
