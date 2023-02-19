#System_Information
System Boot and Autostart Programs are lists of programs that will run  
on system boot or at user login.
The Task manager startup tab has the list of programs that will run on system boot at user login

• NTUSER.DAT\\Software\\Microsoft\\Windows\\CurrentVersion\\Run  
• NTUSER.DAT\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce  
• HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce  
• HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\Explorer\\Run  
• HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run  
• HKLM\\SYSTEM\\CurrentControlSet\\Services
• Useful to find malware and to audit installed software  
• This is not an exhaustive list of autorun locations

###### Tools 
Autorun by Windows - https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns
Tool is also used in Windows Priv esc - TCM course x