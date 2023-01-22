#File_Folder_Opening 
#Deleted_Items_File_Existence 
Shell bags identifies which folders were accessed on the local machine, via  
the network, and on removable devices, per user. It also shows evidence of  
previously existing folders still **present after deletion/overwrite**.

It also shows if a USB connected and copied over a anti-forensics tool

**The BagMRU key stores folder names and records folder paths by creating the similar tree  
structure.
The Bags key stores the view preferences such as the window size, location and  
view mode.**

###### Primary Data:
• USRCLASS.DAT\\Local Settings\\Software\\Microsoft\\Windows\\Shell\Bags  
• USRCLASS.DAT\\Local Settings\\Software\\Microsoft\\Windows\\Shell\\BagMRU

###### Residual Desktop Items and Network Shares:
• NTUSER.DAT\\Software\\Microsoft\\Windows\\Shell\BagMRU  
• NTUSER.DAT\\Software\\Microsoft\\Windows\\Shell\Bags

### **Interpretation**  
• Massive collection of data on folders accessed by each user  
• Folder file system timestamps are archived in addition to first and last  
interaction times  
• “Exotic” items recorded like mobile device info, control panel access, and  
**Zip archive** access

![[Pasted image 20230117111133.png]]

### Use Case
ShellBag information is crucial when forensicators need to know when and which  
folder a user accessed. For instance, when a company suspects an employee leaked a  
confidential document stored on the network, that employee’s computer may have the  
ShellBag information that demonstrates the folder containing that document was accessed  
shortly before the document was leaked. Furthermore, ShellBags may also show the  
folders or servers that employee should not access. Those findings are critical to the  
investigation. Or, when a company suspects an employee maliciously deleted the  
important files on the network, ShellBag information may demonstrate the employee’s  
computer accessed the folder before the incident happened.