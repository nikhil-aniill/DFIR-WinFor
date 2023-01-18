Registry key tracking the last files and folders opened(.LNK files). Used to populate  
data in places like the “Recent” menus present in some Start menus.

###### Location
This located in the NTUSER.DAT\\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\RecentDocs

#### Interpretation
• RecentDocs – Rollup key tracking the overall order of the last 150 files or  
folders opened. MRU list tracks the temporal order in which each file/  
folder was opened.  
• .??? – These subkeys store the last 20 files opened by the user of each  
extension type. MRU list tracks the temporal order in which each file was  
opened. The most recently used (MRU) item is associated with the last  
write time of the key, providing one timestamp of file opening for each file  
extension type.  
• Folder – This subkey stores the last 30 folders opened by the user. The  
most recently used (MRU) item in this key is associated with the last write  
time of the key, providing the time of opening for that folder.

#File_Folder_Opening