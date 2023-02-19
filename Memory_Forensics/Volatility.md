```shell
volatility -f <memdump> imageinfo
```
See the Profile of the Windows 

`volatility -f <memdump> --profile=<profile> pslist`

`volatility -f <memdump> --profile=<profile> psscan`

`volatility -f <memdump --profile=<profile> procdump -p <PID> --dump-dir=./>

`volatility -f <memdump --profile=<profile> memdump -p <PID> --dump-dir=./>`

`volatility -f <memdump --profile=<profile> modscan -p <PID>

`volatility -f <memdump --profile=<profile> netscan -p <PID>

`python2 volatility/vol.py -f memory.raw --profile=Win7SP1x86_23418 consoles`
``

- **modscan** is used to find prewviously unloaded drivers and drivers that have been hidden/unlinked by rootkits. 
- **svchost.exe** should always have a parent  services.exe
- **lsass.exe** should have a parent of wininit.exe
- **netscan** plugin can find the connection to a C2 server or data exfiltration
- **malfind** plugin finds hidden or injected code/DLLs in user mode memory
- **hollowfind** plugin find evidence of process hollowing

## VAD and PEB

VAD is Virtual Address Descriptor and PEB is Process Environment Block. Vad lives in the kernel memory and PEB lives in the process memory.

VADs (Virtual Address Descriptors) are used by the memory manager to track ALL memory allocated on the system. Malware and rootkits can hide from a lot of different OS components, but hiding from the memory manager is unwise. If it can’t see your memory, it will give it away!

### Tools
Procdump to dump malicious processes(.exe)
cmdscan is a plugin built into volatility to find the command ran by the attacker and it's output

#### To access a file used in the memory

To access the script, we will use the filescan plugin to locate the physical address of the file's **_FILE_OBJECT** structure and then use the dumpfiles plugin to extract its content to disk. Here, we need to note that the file may still not exist in memory.
```bash
python2 volatility/vol.py -f memory.raw --profile=Win7SP1x86_23418 filescan |grep "update.ps1"
```


```bash
python2 volatility/vol.py -f memory.raw --profile=Win7SP1x86_23418 dumpfiles -Q 0x000000003f4551c0 -D ./dumps
```
cat the contents of the file to view what's inside
[[Process Genealogy]]

