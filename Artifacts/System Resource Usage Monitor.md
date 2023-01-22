#Application_Execution 

### Description  
SRUM records 30 to 60 days of historical system performance including  
applications run, user accounts responsible, network connections, and  
bytes sent/received per application per hour.

### Location  
Win8+: C:\Windows\System32\SRU\SRUDB.dat

### Interpretation  
• SRUDB.dat is an Extensible Storage Engine database  
• Three tables in SRUDB.dat are particularly important:  
- {973F5D5C-1D90-4944-BE8E-24B94231A174} = Network Data Usage  
- {d10ca2fe-6fcf-4f6d-848e-b2e99266fa89} = Application Resource Usage  
- {DD6636C4-8929-4683-974E-22C046A43763} = Network Connectivity Usage