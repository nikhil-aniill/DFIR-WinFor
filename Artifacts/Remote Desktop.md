#Acount_Usage
https://www.youtube.com/watch?v=myzG11BP3Sk&list=PLlv3b9B16ZadqDQH0lTRO4kqn2P1g9Mve&index=13
The Remote Desktop is launched by the client **mstsc.exe**
RDP is a protocol to connect to other windows PC over a GUI. In layman's terms, what this essentially does, is store bitmap sized images of your RDP sessions into a file so that your session reuses these images and reduces the potential lag.

### Bit Map Cache
C:\\Users\\UserName\\AppData\\Local\\Microsoft\\Terminal Server Client \\Cache



### Tools Used

BMC Tools - BitMap Cache Extractor
After running the tool, puzzle like pieces of the RDP session will be revealed. We can put together the commands run or windows open by the user connected to the session.

### Scenarios
https://www.13cubed.com/downloads/rdp_flowchart.pdf

###### A successful RDP logon 

1149 -> 4624->21->22
Logon Type 10 usually for successfully authenticated user. 
![[Pasted image 20230119101747.png]]


###### An RDP logon attempt that was unsuccessful 
![[Pasted image 20230119103022.png]]
1149 shows authentication succeeded because of the sucessful network connection and not the user authentication.

###### An RDP session disconnect via someone closing the window without clicking Start, Disconnect 
![[Pasted image 20230119103148.png]]

###### An RDP session disconnect via someone clicking Start, Disconnect 
![[Pasted image 20230119103247.png]]

###### An RDP session reconnect 
![[Pasted image 20230119103528.png]]

Event 40 can be related to session disconnect ot reconnect

###### An RDP session logoff

![[Pasted image 20230119105039.png]]Event 9009 is found in the System log