`volatility -f <memdump> imageinfo`
See the Profile of the Windows 

`volatility -f <memdump> --profile=<profile> pslist`

`volatility -f <memdump> --profile=<profile> psscan`

`volatility -f <memdump --profile=<profile> procdump -p <PID> --dump-dir=./>

`volatility -f <memdump --profile=<profile> memdump -p <PID> --dump-dir=./>`

`volatility -f <memdump --profile=<profile> modscan -p <PID>

`volatility -f <memdump --profile=<profile> netscan -p <PID>
``

- **modscan** is used to find prewviously unloaded drivers and drivers that have been hidden/unlinked by rootkits. 
- **svchost.exe** should always have a parent  services.exe
- **lsass.exe** should have a parent of wininit.exe
- **netscan** can find the connection to a C2 server or data exfiltration
- malfind finds hidden or injected code/DLLs in user mode memory
- **hollowfind** find evidence of process hollowing

## VAD and PEB

VAD is Virtual Address Descriptor and PEB is Process Environment Block. Vad lives in the kernel memory and PEB lives in the process memory.

VADs (Virtual Address Descriptors) are used by the memory manager to track ALL memory allocated on the system. Malware and rootkits can hide from a lot of different OS components, but hiding from the memory manager is unwise. If it can’t see your memory, it will give it away!

### Tools
Procdump to dump malicious processes(.exe)
cmdscan is a plugin built into volatility to find the command ran by the attacker and it's output

[[Memory]]
