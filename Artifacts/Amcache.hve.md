#Application_Execution 
#Windows 
### Description  
Amcache tracks installed applications, programs executed (or present),  
drivers loaded, and more. What sets this artifact apart is it also tracks the  
SHA1 hash for executables and drivers. (Available in Win7+)

### Location  
C:\Windows\AppCompat\Programs\Amcache.hve

### Interpretation  
• A complete registry hive, with multiple sub-keys  
• Full path, file size, file modification time, compilation time, and publisher  
metadata  
• **SHA1 hash of executables and drivers**  
• Amcache should be used as an indication of executable and driver  
presence on the system, but not to prove actual execution
