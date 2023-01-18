#Application_Execution 
-   Prefetch files are great artifacts for forensic investigators trying to analyze applications that have been run on a system. Windows creates a prefetch file when an application is run from a particular location for the very first time. **This is used to help speed up the loading of applications**. For investigators, these files contain some valuable data on a user’s application history on a computer.
-   Located in C:\Windows\Prefetch\*.pf
-   Why are Prefetch Files Important to Your Digital Forensics Investigation?
-   Evidence of program execution can be a valuable resource for forensic investigators. They can prove that a suspect ran a program like CCleaner to cover up any potential wrongdoing. If the program has since been deleted, a prefetch file may still exist on the system to provide evidence of execution. Another valuable use for prefetch files is in malware investigations which can assist examiners in determining when a malicious program was run. Combining this with some basic timeline analysis, investigators can identify any additional malicious files that were downloaded or created on the system, and help determine the root cause of an incident.

#### From SANS Poster 
C:\\Windows\\Prefetch  
Naming format: (exename)-(hash).pf  
• SYSTEM\\CurrentControlSet\\Control\\Session Manager\\Memory Management\\PrefetchParameters  
EnablePrefetcher value  
(0 = disabled; 3 = application launch and boot enabled

#### From 13 cubed 
filename-hash(xxxxxxxx).pf

Example: CALC.EXE-AC08706A.pf  
The hash is a hash of the file’s path. In this example, CALC.EXE is located in C:\Windows\System32. If it were copied to another location (like the Desktop) and executed, a new .pf file would be created reflecting a hash of the new path.