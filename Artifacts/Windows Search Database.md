#Deleted_Items_File_Existence 
### Description  
Windows Search indexes more than 900 file types, including  
email and file metadata, allowing users to search based on  
keywords.  

### Location  
• Win XP: C:\Documents and Settings\All Users\Application Data\ Microsoft\Search\Data\  
Applications\Windows\Windows.edb  
• Win7+: C:\ProgramData\Microsoft\Search\Data\Applications\Windows\Windows.edb  
• Win7+: C:\ProgramData\Microsoft\Search\Data\Applications\Windows\GatherLogs\  
SystemIndex  

### Interpretation  
• Database in Extensible Storage Engine format  
• Gather logs contain a candidate list for files to be indexed over  
each 24 hour period  
• Extensive file metadata and even partial content can be present
